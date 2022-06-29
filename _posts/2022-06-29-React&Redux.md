---
Layout:
Title: "React and Redux"
Date: "2022 06 29"
---

# Introduction
Today I was busy with React and Redux.

# Body
The code editor now shows all your Redux and React code from the past several challenges. It includes the Redux store, actions, and the DisplayMessages component. The only new piece is the AppWrapper component at the bottom. Use this top level component to render the Provider from ReactRedux, and pass the Redux store as a prop. Then render the DisplayMessages component as a child. Once you are finished, you should see your React component rendered to the page.React Redux is available as a global variable here, so you can access the Provider with dot notation. The code in the editor takes advantage of this and sets it to a constant Provider for you to use in the AppWrapper render method:

// Redux:

const ADD = 'ADD';

const addMessage = (message) => {

  return {

    type: ADD,

    message

  }

};

const messageReducer = (state = [], action) => {

  switch (action.type) {

    case ADD:

      return [...state,action.message];

    default:

      return state;

  }

};

const store = Redux.createStore(messageReducer);

// React:

class DisplayMessages extends React.Component {

  constructor(props) {

    super(props);

    this.state = {

      input: '',

      messages: []

    }

    this.handleChange = this.handleChange.bind(this);

    this.submitMessage = this.submitMessage.bind(this);

  }

  handleChange(event) {

    this.setState({

      input: event.target.value

    });

  }

  submitMessage() {  

    this.setState((state) => {

      const currentMessage = state.input;

      return {

        input: '',

        messages: state.messages.concat(currentMessage)

      };

    });

  }

  render() {

    return (

      <div>

        <h2>Type in a new Message:</h2>

        <input value={this.state.input} onChange={this.handleChange}/><br/>

        <button onClick={this.submitMessage}>Submit</button>

        <ul>

          {this.state.messages.map( (message, idx) => {

              return (

                 <li key={idx}>{message}</li>

              )

            })

          }

        </ul>

      </div>

    );

  }

};

const Provider = ReactRedux.Provider;

class AppWrapper extends React.Component {

  // Render the Provider below this line

render() {

  return(

  <Provider store={store}>

  <DisplayMessages/>

  </Provider>

  )

}

  // Change code above this line

};


Map State to Props- The Provider component allows you to provide state and dispatch to your React components, but you must specify exactly what state and actions you want. This way, you make sure that each component only has access to the state it needs. You accomplish this by creating two functions: mapStateToProps() and mapDispatchToProps().In these functions, you declare what pieces of state you want to have access to and which action creators you need to be able to dispatch. Once these functions are in place, you'll see how to use the React Redux connect method to connect them to your components in another challenge.Behind the scenes, React Redux uses the store.subscribe() method to implement mapStateToProps():

const state = [];

// Change code below this line

const mapStateToProps = state => {

  return {

    messages: state

  }

}

# Conclusion
For this week I will be busy with React and Redux.