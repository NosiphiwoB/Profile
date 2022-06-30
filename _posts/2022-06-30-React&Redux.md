---
Layout:
Title: "React and Redux"
Date: "2022 06 30"
---

# Introduction
Today I was busy with React and Redux,I also did few katas on codewars.

# Body
The mapDispatchToProps() function is used to provide specific action creators to your React components so they can dispatch actions against the Redux store. It's similar in structure to the mapStateToProps() function you wrote in the last challenge. It returns an object that maps dispatch actions to property names, which become component props. However, instead of returning a piece of state, each property returns a function that calls dispatch with an action creator and any relevant action data. You have access to this dispatch because it's passed in to mapDispatchToProps() as a parameter when you define the function, just like you passed state to mapStateToProps(). Behind the scenes, React Redux is using Redux's store.dispatch() to conduct these dispatches with mapDispatchToProps(). This is similar to how it uses store.subscribe() for components that are mapped to state.For example, you have a loginUser() action creator that takes a username as an action payload. The object returned from mapDispatchToProps() for this action creator would look something like:

{
    
  submitLoginUser: function(username) {

    dispatch(loginUser(username));

  }

}

e.g 
const addMessage = (message) => {

  return {

    type: 'ADD',

    message: message

  }

};

// Change code below this line

const mapDispatchToProps = dispatch => {

  return {

    submitNewMessage: function(message){

      dispatch(addMessage(message))

    }

  }

}

Now that you've written both the mapStateToProps() and the mapDispatchToProps() functions, you can use them to map state and dispatch to the props of one of your React components. The connect method from React Redux can handle this task. This method takes two optional arguments, mapStateToProps() and mapDispatchToProps(). They are optional because you may have a component that only needs access to state but doesn't need to dispatch any actions, or vice versa.To use this method, pass in the functions as arguments, and immediately call the result with your component. This syntax is a little unusual and looks like:
connect(mapStateToProps, mapDispatchToProps)(MyComponent)

e.g 

const addMessage = (message) => {

  return {

    type: 'ADD',

    message: message

  }

};

const mapStateToProps = (state) => {

  return {

    messages: state

  }

};

const mapDispatchToProps = (dispatch) => {

  return {

    submitNewMessage: (message) => {

      dispatch(addMessage(message));

    }

  }

};

class Presentational extends React.Component {

  constructor(props) {

    super(props);

  }

  render() {

    return <h3>This is a Presentational Component</h3>

  }

};

const connect = ReactRedux.connect;

// Change code below this line

const ConnectedComponent=connect(mapStateToProps, mapDispatchToProps)(Presentational)

# Conclusion
Tomorrow I will do the remaining challenges on React and Redux.