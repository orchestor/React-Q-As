## React Primer 

![](http://blog-assets.risingstack.com/2016/Jan/react_best_practices-1453211146748.png)

> A primer which contains important O&As which you may or may not need to know but you may find it useful while learning react. Inspired by the teachings of [Tyler Mcginnis](), [Dan Abramov]() and [Wes Bos]() these questions may help you while applying for [React]() jobs.


### Status

This is a work in progress. This guide will be updated with different questions and important points which will be important for every **React Developer**.

- [x] React Primer
- [ ] Fiber Architecture
<hr/>

### Authors Note

I decided to write this primer because I believe in giving back to the community. The goal of this primer is to help developers remember the important concepts related to the framework while building the applications in React. This by no means serves as a guide for learning React. It may help you a lot while you are preparing for jobs in React. You can help improve this document further and I hope you will share this in the community. 

This primer is dedicated to all the React Developers. The community is super awesome and very friendly! 🍻

### Preface
#### React Documentation
The react documentation is a good place to start learning react. You can learn the important concepts in this primer and read further about them in the official documentation. Here is the [link](https://facebook.github.io/react/)

#### Awesome resources
* [Awesome React](https://github.com/nitin42/awesome-react)
* [Awesome React Components](https://github.com/nitin42/awesome-react-components)
* [Redux](https://github.com/nitin42/redux)
* [React-Redux](https://github.com/nitin42/react-redux-links)
* [React Ecosystem](https://github.com/nitin42/redux-ecosystem-links)
* [Awesome Redux](https://github.com/nitin42/awesome-redux)

<hr/>

**Let's get started !**

#### A1.  What's the difference between an Element and a Component in React?
> Creating a React element describes the object representation of some UI. It simply means that what you actually want to see in your document.


#### A2. I know what is a Functional component and a Class Component but when should I use either of them?
> Well, you should use Functional components when you want your components to act like they are dumb as if they know nothing about the states and the lifecycle methods. Use them when you don't have any states or any method. Whereas Class Components are composed of states and lifecyle methods. It passes down the props to the other components(child components).

#### A3. Why refs are so important in React?
> When I was learning react from [this](https://reacttraining.com/online) awesome course, this is what I learned about the refs. Refs are small escapes which allows us to get direct access to a DOM instance of a component. To use them just add a ref attribute to your component whose value is a callback function which receives the value of the underlying DOM instance of your component.

#### A4.  I am using this.setState() inside my methods but what actually goes behind the scene?
> When we use this.setState() in an underlying method in our Class Components, it will merge the object passed to it into the current state of our component. Due to this React performs a reconciliation of our component in the most efficient way and updates our UI on the basis of our new state. React does all this stuff by creating a new tree of React elements and comparing it with the previous tree by using its [Diffing Algorithm](Reconciliation).

#### A5. Okay. We keep using keys in our react components and we get errors when they are not unique. Why it happens?
> Unique keys of a components helps React to keep track of what items have changed, added or removed from a list. Using unique keys helps React in the process of reconciliation (Diffing Algorithm).

#### A6. How to use render callback pattern while declaring your components ?
> In this pattern, a component receives a function as its child component. So instead of a component our child is now a function. So we treat **props.children as a function**.

#### A7. I want to fetch some data using AJAX or superagent in my component. Which lifecycle hook should I use?
> You must be thinking of using **componentWillMount()**. Well it may seem right at first to use it but React's research team is working on a  architecture named [Fiber](https://github.com/acdlite/react-fiber-architecture). This architecture will change the reconciliation process as React may start calling and executing the componentWillMount() method any time and any AJAX requests made inside this method will cause an error. We will be trying to update the state of our component which is unmounted and it won't work.

#### A8. What better things we can do with this.setState() ?
> Well this question is a bit awkard to anyone who is familiar with React but I am going to tell you one interesting thing about the setState(). We normally pass our object to it so that it updates the current state but we can also pass a callback function to it. Yes, this.setState() is async in nature and will execute the call after our component is done with the process of re-rendering.

#### A9. What is SyntheticEvent ?
> It is React's cross browser wrapper around the browser's native client which solves the compatibility issues. React doesn't keep the track of all the events instead it listens to  all the events using a top level API which is good for the performance.

#### A10. What's the easiest way or best tool one could use to set up the environment and build apps with React?
> Haha! Its a bonus for everyone. We all know that there is a popular tool build by the creators of React called [create-react-app](https://github.com/facebookincubator/create-react-app) with no build configuration which lessens the burden of developing the app from scratch. 

<br/>
If you are building apps with React and are familiar with above concepts, then you hold yourself in a good position to land a job or contribute to a project which uses React.

### Contribute

Add or remove content for any changes.

### License

GNU
