# Routing in React

React doesn't have a inbuilt routing. We use the library **'react-router-dom'** to add dynamic routing in webpages built in React.

Here, _dynamic routing_ means, no request is made to the server when a new page is to be rendered\(the page doesn't reload\), also the url is kept updated.

Basic installation steps: [here](https://www.npmjs.com/package/react-router-dom)

### Components of the react-router-dom library

**Routers** 📬

&lt;BrowserRouter&gt; acts as a wrapper component for all the Routes. It gives them\(children\) all the functionality of routing.

&lt;HashRouter&gt; store the current location in the hash portion of the url

**Route Matchers** 

&lt;Route&gt; , takes arguments \(3 most used api's\) 'exact', 'path' and 'component'.

exact takes a default true value and suggests that the url match should be exact.

Path is the url path the Routing procedure should follow.

component is the component which we want to render. 

&lt;Switch&gt;  When a &lt;Switch&gt;  is rendered, it searches through its children &lt;Route&gt; elements to find one whose path matches the current URL. When it finds one, it renders that &lt;Route&gt; and ignores all others. This means that you should put &lt;Routes&gt;s with more specific \(typically longer\) paths before less-specific ones \(alt. use exact\).

**Navigation**

&lt;Link&gt; is generally used to create links in the application. 

History prop can be used for the abv purpose.

For more insight [refer](https://codesandbox.io/s/hidden-dawn-298hg)

**withRouter**  is a higher order component\(\) that takes a component as an argument and returns a modified component



