# React Custom Hooks

- When we want to share logic between two JavaScript functions, we extract it to a third function. Both components and Hooks are functions, so this works for them too!

- A custom Hook is a JavaScript function whose name starts with ”use” and that may call other Hooks.

- Since Hooks are functions, we can pass information between them.

# Hook Rules

- Only Call Hooks at the Top Level
- Don’t call Hooks inside loops, conditions, or nested functions. Instead, always use Hooks at the top level of your React function.

- Only Call Hooks from React Functions
Don’t call Hooks from regular JavaScript functions. Instead, you can:

✅ Call Hooks from React function components.  
✅ Call Hooks from custom Hooks (we’ll learn about them on the next page).

- We released an ESLint plugin called eslint-plugin-react-hooks that enforces these two rules. You can add this plugin to your project if you’d like to try it:

This plugin is included by default in Create React App.

```
npm install eslint-plugin-react-hooks --save-dev
```

# Custom Hooks - All you need to know

- Hooks bring to functional components the things we once were only able to do with classes, like being able to work with React local state, effects and context through useState, useEffect and useContext.

- Additional Hooks include: useReducer, useCallback, useMemo, useRef, useImperativeHandle, useLayoutEffect and useDebugValue. 

- The easiest way to describe Hooks is to show side-by-side examples of a class component that needs to have access to state and lifecycle methods, and another example where we achieve the same thing with a functional component.


1. Never call Hooks from inside a loop, condition or nested function
1. Hooks should sit at the top-level of your component
1. Only call Hooks from React functional components
1. Never call a Hook from a regular function
1. Hooks can call other Hooks

# 10 Essential React Hooks

1. useArray
1. react-use-form-state
1. react-fetch
1. useMedia
1. react-useportal
1. react-firebase
1. use-onClickOutside
1. useIntersectionObserver
1. use-location
1. use-redux