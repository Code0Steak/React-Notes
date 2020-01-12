# Intro to Hooks

Hooks are a new feature added to React\(16.8 onwards\), they provide a more direct API towards the usage of props, state, context, lifecycle methods, etc. in a functional component. They, in a way promote the use of a functional component 💁🏻‍♂️

### Motivation

{% tabs %}
{% tab title="1" %}
It is **hard to reuse stateful logic between state components**. Higher Order Components\(HOC's\) and Render Props are used to solve this. But in a complex component wrapped with HOC's or render props or other abstractions, the method of wrapping may result into a '**wrapper hell**' - proving difficult for maintainance and debugging. Many a times we need to refactor a component to wrap it around a HOC 😪

Hooks provide a better primitive to reuse stateful logic between components.
{% endtab %}

{% tab title="2" %}
**Complex components are hard to understand**. Mainly those using the lifecycle methods for data fetching - this is not suitable for component reuse.

Hooks let's us split components based upon related terms, rather than forcing a split based upon lifecycle methods. 
{% endtab %}

{% tab title="3" %}
Class components have presented issues with latest tools\( module bundlers like Webpack\) - they don't minify very well, they may lead to slower hot reloads.
{% endtab %}
{% endtabs %}

So,

> Hooks are functions that help us _hook into_ React state and lifecycle methods, from functional components.
>
> They let us use React without classes.



