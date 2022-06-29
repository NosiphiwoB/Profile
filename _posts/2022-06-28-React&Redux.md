---
Layout:
Title: "React and Redux"
Date: "2022 06 28"
---

# Introduction
Today I was still busy with React and Redux

# Body 
I did few challenges on react and redux.

Managing state locally first-First, in the render() method, have the component render an input element, button element, and ul element. When the input element changes, it should trigger a handleChange() method. Also, the input element should render the value of input that's in the component's state. The button element should trigger a submitMessage() method when it's clicked.Second, write these two methods. The handleChange() method should update the input with what the user is typing. The submitMessage() method should concatenate the current message (stored in input) to the messages array in local state, and clear the value of the input.Finally, use the ul to map over the array of messages and render it to the screen as a list of li elements:

class DisplayMessages extends React.Component {

  constructor(props) {

    super(props);

    this.state = {

      input: '',

      messages: []

    }

  }

  // Add handleChange() and submitMessage() methods here

handleChange(event){

    this.setState({

      input: event.target.value,

      messages: this.state.messages

    })

  }

   submitMessage(){

    this.setState({

      input: '',

      messages: [...this.state.messages, this.state.input]

    })

  }

  render() {

    return (

      <div>

        <h2>Type in a new Message:</h2>

        { /* Render an input, button, and ul below this line */ }

 <input onChange={this.handleChange.bind(this)} value={this.state.input}/>

        <button onClick={this.submitMessage.bind(this)}>Submit</button>

        <ul>

          {this.state.messages.map((x, i)=>{

            return <li key={i}>{x}</li>

          })}

        </ul>

        { /* Change code above this line */ }

      </div>

    );

  }

};


After the react component we need to move the logic it's perfoming locally in its state into Redux.This is the first step to connect the simple React app to Redux:
First, define an action type ADD and set it to a const ADD. Next, define an action creator addMessage() which creates the action to add a message. You'll need to pass a message to this action creator and include the message in the returned action.Then create a reducer called messageReducer() that handles the state for the messages. The initial state should equal an empty array. This reducer should add a message to the array of messages held in state, or return the current state. Finally, create your Redux store and pass it the reducer.

const ADD = "ADD";

const addMessage = message => {

  return{ 

    type:ADD,

     message

  }

}

const messageReducer = (previousState = [], action)=>{

switch (action.type) {

  case ADD:

   return [...previousState, action.message];

      break;

      default:

      return previousState;

}

};

const store = Redux.createStore(messageReducer);

Now that we have created a Redux store to handle the messages array and created an action for adding new messages.We now have to provide React access to the Redux store and action it needs to dispatch updates.React Redux provides a small API with two key features (Provider and connect).The Provider is a wrapper component from React Redux that wraps your React app. This wrapper then allows you to access the Redux store and dispatch functions throughout your component tree.Provider takes two props, the Redux store and the child components of your app. Defining the Provider for an App component might look like this:

<Provider store={store}>

  <App/>
  
</Provider>

# Conclusion
I am going to continue with React and Redux.