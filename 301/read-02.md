##React lifecycle

1-Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
Answer: `componentDidMount` will only be called once after the first render.

2-What is the very first thing to happen in the lifecycle of React?
Answer:`getDerivedStateFromProps()`  is the first React lifecycle method.

3-Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`.

Answer: `constructor`,`render`, `React Updates`,`componentWillUnmount` ,`componentDidMount`.


4-What does `componentDidMount` do?

Answer:it is called once in the component life cycle and it signals that the component and all its sub-components have rendered properly.



##React State Vs Props

1-What types of things can you pass in the props?
Answer: function or component

2-What is the big difference between props and state?

Answer:inside the component we use state and outside the component we use props.

3-When do we re-render our application?

Answer:When the state changes in the parent component.


4-What are some examples of things that we could store in state?
Answer : when we need to update the component depend in user input.