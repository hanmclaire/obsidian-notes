---
title: Quick Start
date: 2025-02-08
---
> Creating and nesting components
- The `export default` keywords specify the main component in the file.

> Writing markup with JSX
- JSX is stricter than HTML. You have to close tags like `<br />`. Your component also can’t return multiple JSX tags. You have to wrap them into a shared parent, like a `<div>...</div>` or an empty `<>...</>` wrapper:
```
function AboutPage() {  
	return (  
		<>  
			<h1>About</h1>  
			<p>Hello there.<br />How do you do?</p>  
		</>  
	);  
	}
```
- ==A JSX element is a combination of JavaScript code and HTML tags that describes what you’d like to display.==

> Adding styles
- ==In React, you specify a CSS class with `className`==. It works the same way as the HTML `class` attribute
- ==React does not prescribe how you add CSS files==. In the simplest case, you’ll add a `<link>` tag to your HTML. If you use a build tool or a framework, consult its documentation to learn how to add a CSS file to your project.

> Displaying data
- JSX lets you put markup into JavaScript. Curly braces let you “escape back” into JavaScript so that you can embed some variable from your code and display it to the user.
```
return (  
	<h1>  
		{user.name}  
	</h1>  
);
```

> Responding to events
- You can respond to events by declaring event handler functions inside your components:
```
function MyButton() {  
	function handleClick() {  
		alert('You clicked me!');  
	}  

	return (  
		<button onClick={handleClick}>  
			Click me  
		</button>  
	);  
}
```
- Notice how `onClick={handleClick}` has no parentheses at the end! ==Do not call the event handler function: you only need to pass it down. React will call your event handler when the user clicks the button.==

> Updating the screen
- Often, you’ll want your component to “remember” some information and display it. 
	- For example, maybe you want to count the number of times a button is clicked. To do this, add state to your component.
```
import { useState } from 'react';

function MyButton() {  
	const [count, setCount] = useState(0);

function MyButton() {  
	const [count, setCount] = useState(0);  

	function handleClick() {  
		setCount(count + 1);  
	}  

	return (  
		<button onClick={handleClick}>  
			Clicked {count} times  
		</button>  
	);  
}
```
- ==Notice how each button “remembers” its own count state and doesn’t affect other buttons.==

> Using hooks
- ==Functions starting with `use` are called Hooks.== 
	- useState is a built-in Hook provided by React. 
	- ==You can also write your own Hooks by combining the existing ones.==
- Hooks are more restrictive than other functions. 
	- You can only call Hooks at the top of your components (or other Hooks). 
	- ==If you want to use useState in a condition or a loop, extract a new component and put it there.==

> Sharing data between components 
- Often you’ll need components to share data and always update together. 
	- To make both MyButton components display the same count and update together, you need to move the state from the individual buttons “upwards” to the ==closest component containing all of them.==

> Why immutability is important 
- There are generally two approaches to changing data. The first approach is to mutate the data by directly changing the data’s values. The second approach is to replace the data with a new copy which has the desired changes. Here is what it would look like if you mutated the `squares` array:
```
const squares = [null, null, null, null, null, null, null, null, null];  
squares[0] = 'X';  
// Now `squares` is ["X", null, null, null, null, null, null, null, null];
```
- And here is what it would look like if you changed data without mutating the `squares` array:
```
const squares = [null, null, null, null, null, null, null, null, null];  
const nextSquares = ['X', null, null, null, null, null, null, null, null];  
// Now `squares` is unchanged, but `nextSquares` first element is 'X' rather than `null`
```
- The result is the same but by not mutating (changing the underlying data) directly, you gain several benefits.
	- Immutability makes complex features much easier to implement. Later in this tutorial, you will implement a “time travel” feature that lets you review the game’s history and “jump back” to past moves. ==This functionality isn’t specific to games—an ability to undo and redo certain actions is a common requirement for apps. Avoiding direct data mutation lets you keep previous versions of the data intact, and reuse them later.==


> Render and commit 
- Before your components are displayed on the screen, they must be rendered by React.
- React is the waiter who puts in requests from customers and brings them their orders. This process of requesting and serving UI has three steps: 
	- Triggering a render (delivering the diner’s order to the kitchen)
	- Rendering the component (preparing the order in the kitchen)
	- Committing to the DOM (placing the order on the table)![[React rendering and committing.png]]

> Referencing Values with Refs
- ==When you want a component to “remember” some information, but you don’t want that information to trigger new renders, you can use a ref.==
- Unlike state, ref is a plain JavaScript object with the current property `ref.current` property  that you can read and modify.
- Note that the component doesn’t re-render with every increment. Like state, refs are retained by React between re-renders. ==However, setting state re-renders a component. Changing a ref does not!==
![[Refs vs. State.png]]
- ==Because the count value is displayed, it makes sense to use a state value for it.== 
	- When the counter’s value is set with setCount(), React re-renders the component and the screen updates to reflect the new count.
	- If you tried to implement this with a ref, React would never re-render the component, so you’d never see the count change! See how clicking this button does not update its text

> When to use refs
- Typically, you will use a ref when your component needs to “step outside” React and communicate with external APIs—often a browser API that won’t impact the appearance of the component. 
- Here are a few of these rare situations:
	- Storing timeout IDs
	- Storing and manipulating DOM elements, which we cover on the next page
	- Storing other objects that aren’t necessary to calculate the JSX. 
- ==If your component needs to store some value, but it doesn’t impact the rendering logic, choose refs.==
