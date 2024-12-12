# React State Update Bug
This repository demonstrates a common error in React: directly modifying the state object without using `this.setState()`. Directly modifying state leads to unexpected behavior because React doesn't detect the change and re-render the component.

## Bug Description
The bug is in the way the component's state is updated.  The line `this.state.count++;` attempts to directly modify the state object.  This does not trigger a re-render in React, resulting in the UI not updating to reflect the change in state. 

## Solution
The solution is to use the `this.setState()` method to update the state object.  This method notifies React of the change, which triggers a re-render of the component. 