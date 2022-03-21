# Understanding Questions:

1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code executes for each step.

- The user presses the 1 button.
- The onClick function is then executed for that specific CalcButton component.
- oneClickHandler is executed, which dispatches the addOne action creator function.
- In the /actions/index.js, the addOne creator function is executed, which returns an action object with a type key that has a value of ADD_ONE
- Then, in the /reducers/index.js file, the reducer function is executed, passing in the current state, and that action object.
- The function executes the ADD_ONE case of the switch statement and returns a copy of the current state, where the total key has a value of its current total plus 1.
- The state.total key is changed to that value and then passed into the TotalDisplay component.
- TotalDisplay shows the total plus 1.
