# setState Explained

- setState() is the only legitimate way to update state after the initial state setup.

- When building React applications, there are times when you’ll want to calculate state based the component’s previous state. You cannot always trust this.state to hold the correct state immediately after calling setState(), as it is always equal to the state rendered on the screen.

# Lists and Keys

- Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.

- The best way to pick a key is to use a string that uniquely identifies a list item among its siblings.

- Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique.

# Typechecking Props

- You can catch a lot of bugs with typechecking. For some applications, you can use JavaScript extensions like Flow or TypeScript to typecheck your whole application. But even if you don’t use those, React has some built-in typechecking abilities. To run typechecking on the props for a component, you can assign the special propTypes property:

```JS
import PropTypes from 'prop-types';

class Greeting extends React.Component {
  render() {
    return (
      <h1>Hello, {this.props.name}</h1>
    );
  }
}

Greeting.propTypes = {
  name: PropTypes.string
};
```

- PropTypes exports a range of validators that can be used to make sure the data you receive is valid.

- With PropTypes.element you can specify that only a single child can be passed to a component as children.

- The defaultProps will be used to ensure that this.props.name will have a value if it was not specified by the parent component. The propTypes typechecking happens after defaultProps are resolved, so typechecking will also apply to the defaultProps.

# Components and Props

- When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.

- Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

- Whether you declare a component as a function or a class, it must never modify its own props. Consider this sum function:

```JS
function sum(a, b) {
  return a + b;
}
```

- Such functions are called “pure” because they do not attempt to change their inputs, and always return the same result for the same inputs.

# Handling Events

- Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.
With JSX you pass a function as the event handler, rather than a string.

- When using React, you generally don’t need to call addEventListener to add listeners to a DOM element after it is created. Instead, just provide a listener when the element is initially rendered.

# Snapshot Testing

- Snapshot tests are a very useful tool whenever you want to make sure your UI does not change unexpectedly.

- A typical snapshot test case renders a UI component, takes a snapshot, then compares it to a reference snapshot file stored alongside the test. The test will fail if the two snapshots do not match: either the change is unexpected, or the reference snapshot needs to be updated to the new version of the UI component.

- The snapshot artifact should be committed alongside code changes, and reviewed as part of your code review process. Jest uses pretty-format to make snapshots human-readable during code review.

- Failed snapshots can also be updated interactively in watch mode

# React Testing Library

- The react-testing-library is a very light-weight solution for testing React components.

- Rather than dealing with instances of rendered react components, your tests will work with actual DOM nodes.

