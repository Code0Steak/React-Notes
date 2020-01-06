# What is Redux? Why Redux?

### Redux is a predictable state container for JS Apps. It helps us write applications that behave consistently, run in different environments and are easy to test.

### **Understanding Redux** 🧐 :

📍 The **first principle** of Redux is : **irrespective of the complexity** of the application, the **whole state** of the application should be represented **as a single JS object**, called **the state** or **the state-tree**.

All mutations and state changes in Redux are explicit. It is possible to keep track of all of them.

📍 The **second principle** of Redux is: **the state tree is redundant and read only**. You cannot ✍ to it! Instead, anytime you want to change the state, you need to dispatch an action. Whether **a change** is initiated by a network/db or by a user, any data that gets into Redux app gets there **by actions only**.

An action is a plane JS object describing the change. Just like the state is a minimal representation of the data in your app, an action is a minimum representation of the change to that data. 

The structure of the action object is upto us. The only requirement is that it has a tie property, which is undefined. Using strings is preferable as they are serializable. 

📍 **Pure Functions**: 

          📌 The Pure Functions are the functions whose return value depends solely on the arguments passed to it. 

          📌 They **do not** have observable side-effects, such as **network or database calls**. 

           📌 If the pure function is called with the same set of arguments, it gives the same set of results every-time. So, pure functions are **predictable**.

          📌 Pure functions **do not modify the value** passed to them. 

```javascript
// Pure Functions

 function square(x){
   return x * x;
}

 function squareAll(items){
    return items.map(square)
 }  
  
```

 📍 **Impure Functions**: They may **make database/network calls**, they may have side-effects, they may **operate the DOM**, may **override values** that are passed to them.

**Some functions in Redux have to be pure**.

📍 The UI is more predictable when it is described as a pure function of the application state. Redux compliments this approach by another idea, that the state mutations in your app need to be describrd as a pure function that takes the previous state and the action being dispatched to return the next state of the application. 

The **third principle** of Redux: to **describe** **state mutations**, **write a function that takes the previous state of the app, the action being dispatched and returns the next step of the application.** This function has to pure and is called a **Reducer**.





