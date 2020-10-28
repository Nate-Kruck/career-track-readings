# Context-API

- Context gives us a way to send data through the component tree w/o having to pass props down manually at every level.

### When To Use Context

- Use context in order to avoid having to pass props through intermediate elements.

### Before You Use Context

- Use context sparingly because it makes component reuse more difficult.

Use
<a href="https://reactjs.org/docs/composition-vs-inheritance.html" target="_blank">Composite Composition</a> for a simpler solution to passing props through many levels.

### API (React.createContext)

```js
const MyContext = React.createContext(defaultValue);
```

- This creates a Context object. The object will read the current context value from the closest matching ```Provider``` above it in the tree.