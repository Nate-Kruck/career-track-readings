# Architectural Styles

- The purpose of Architectural Patterns is to understand how the major parts of the system fit together and how messages and data flow through the system.

- Idiom is also a term that we can regularly meet. An Idiom is a low-level pattern specific to a programming language. It describes how to implement particular aspects of the components or the relationships between them using the features of a given language.

- we have four layers:

1. Presentation layer or UI layer
1. Application layer or Service layer
1. Business logic layer or Domain layer
1. Data access layer or Persistence layer

# Container and Presentation

- The container and presentation pattern splits code into two distinct places:

containers : are stateful components that contain your business login
presentations : are stateless components that present your data

# Container Details

- When the Container/Presentation pattern first became popular all containers were class based components. At that time state and lifecycle methods were only available within class components. Since containers are responsible for managing state and fetching data (lifecycle methods) they were exclusively written as class components. This helped highlight the dichotomy between container components (classes) and presentational components (functions)

# Presentation Details

- Presentation components are responsible for specifying how a section of our page looks. They create DOM and styles.

- When we pass props into our component we should use the prop-types package to specify the props our component receives. This gives us convenient warning messages if we forget to pass a prop or pass a prop with the wrong type.

# Functional vs Class Components

- The most obvious one difference is the syntax. A functional component is just a plain JavaScript function which accepts props as an argument and returns a React element.

- A class component requires you to extend from React.Component and create a render function which returns a React element.

# Conditional Rendering

- Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.