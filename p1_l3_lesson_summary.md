

https://udacity-react.slack.com/archives/C9850EAA3/p1540028794000100
Luca [11:46 AM] October 20th 2018
Lesson 2.3.15 Challenge

*1) What is the difference between Stateless Functional Components and class components?*
Stateless Functional Components are components created by simply using a function declaration. This is the preferable way to create a component, if it just needs to render some UI.
Stateless refers to the fact that the component is not using any state (mutable data over time).
Class Components are components created using a class declaration (or the react API createClass). Normally they need to contain more than just a render method, such as asynchronous handlers and state.
As a side note, also class components can be free of state, and similarly they will be named Stateless  in this case

*2) Describe the reasoning behind Controlled Components.*
Controlled Components are components that render form elements,
storing internally their state and controlling how they are rendered and what they show.
In this way the 'source of truth' lives in the component state, rather than in the DOM.
The benefits of this approach are several, such as:
- instant input validation
- instant modification of the UI based on the input value (for example disabling / enabling fields)
- control the input format

*3) What is the correct way to modify state? Make sure to explain what role a child component like “Add User” can have in the app.*
The correct way to modify a component state is by using its setState method, which is triggering a re-rendering of the component itself after the state has changed.
In fact, modifying the state property directly won't notify react of the change.
For instance:
- an AddUser child component could notify its parent component via a callback function about the data associated with a new user
- the parent component can then store the new user data internally using the setState method
- ultimately the setState method will invoke a re-render against all the parent component children that need to be re-rendered according to the Diffing Algorithm or the shouldComponentUpdate method (edited) 