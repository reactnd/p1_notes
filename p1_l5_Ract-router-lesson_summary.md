https://udacity-react.slack.com/archives/C9850EAA3/p1540631265001100

Luca [11:07 AM]
*_Lesson 2.5.7 Challenge_*

*1) What is the difference between Link and Route?*

The `Route` component renders the UI returned by the associated component when the browser location matches exactly or contains the route's path.

The `Link` component triggers new Routes by changing the browser location.

*2) What is the difference between match.path and match.url?*
*Give a use case for each.*

The `match.path` is the path pattern used by the Route to match the browser location, and it's useful to create nested Routes.

The `match.url` is the matched portions of the browser location, and it's useful to create nested Links.

```// example:

function Item ({ match }) {
    console.log(match.path);    // prints "/item/:itemId"
    console.log(match.url);    //  prints "/item/foo"

    return "itemId: "+match.params.itemId;
}

<Route path="/item/:itemId" component={Item} />
<Link to='/item/foo'>foo</Link>```

*3) Create a code example where you (1) pass props to a component that's rendered by React Router and (2) use nested routes*

https://codesandbox.io/s/github/luca-borrione/reactnd-lesson2.5.7-personal-router
CodeSandbox
react-router-excercise - CodeSandbox
CodeSandbox is an online editor tailored for web applications.
