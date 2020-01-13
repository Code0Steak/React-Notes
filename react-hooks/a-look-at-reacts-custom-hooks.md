---
description: "\U0001F9D0"
---

# A look at React's Hooks

1. _useState_ Hook:

Helps us to use **local state in a functional component**. React preserves this state between re-renders.

```typescript
import React from 'React'

const App: React.FC = () => {

    const [name, setName] = setState('Ameya')
    const [complete, setComplete] = setState(true)
    const [rating, setRating] = setState(5)
    const [todo, setTodo] = setState([{title: '',complete: false}])

}
```

_useState_ returns a pair - a **current state value**\( which we set by passing an argument in _useState_\) and a **function to change that value**. 

**Unlike** _**setState**_ it 

* **doesn't merge** the **old** and the **new** state
* **the state doesn't have to be an object**

Multiple states can be declared in the same function. 

The **array destructuring** helps us give different names\(not part of the API🤞🏻\) to state variables.

2. _useEffect_ Hook:

It helps to **perform side effects**\(such as data fetching, subscriptions to an API etc.\), from a functional component. It can be considered as all the lifecycle methods unified into a single API.

It is used inside a functional component so that it has access to it's props. By default, **React runs the useEffect after every render**, including the initial render.

There are 2 common types of side-effects:

* effects without cleanup: network request / manual DOM mutations 
* effects with cleanup: subscriptions to an API and unsubscribing while dismounting, to prevent memory leaks. This provides consistency out-of-the-box 🎁\(no need to use componentDidUpdate to maintain consistency\)

Just like the useState there can be multiple _useEffect_'s in a functional component.

The useEffect may lead to performance issues if it re-renders the same part of the component, even if it has not changed. For this you can pass the value as a second parameter to the useEffect as:

```typescript
useEffect(() => {
  document.title = `You clicked ${count} times`;
}, [count]); // Only re-run the effect if count changes
```



 Building our own Hooks:

This is done to share logic between two JS functions! This can be an alternative to render props and HOC's. 

A custom Hook is a JS function whose name starts with 'use' and that may call other Hooks. 

