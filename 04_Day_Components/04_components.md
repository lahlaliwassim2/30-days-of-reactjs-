<div align="center">
  <h1> 30 Days Of React: Components </h1>


<sub>Author:
<a href="https://www.linkedin.com/in/wassim-lahlali-080894211/" target="_blank">Lahlali Wassim</a><br>
<small> October, 2020</small>
</sub>

</div>

[<< Day 3](../30-Days-Of-React/03_Day_Setting_Up/03_setting_up.md) | [Day 5 >>](../05_Day_Props/05_props.md)

![30 Days of React banner](../images/30_days_of_react_banner_day_4.jpg)

- [Components](#components)
  - [Big picture of components](#big-picture-of-components)
  - [JavaScript function](#javascript-function)
  - [JavaScript Class](#javascript-class)
  - [Creating React Component](#creating-react-component)
    - [Functional Component](#functional-component)
    - [Rendering components](#rendering-components)
    - [Injecting data to JSX in React Component](#injecting-data-to-jsx-in-react-component)
    - [Further on Functional components](#further-on-functional-components)
- [Exercises: Components](#exercises-components)
  - [Exercises: Level 1](#exercises-level-1)
  - [Exercises: Level 2](#exercises-level-2)
  - [Exercises: Level 3](#exercises-level-3)

# Components

A React component is a small, reusable code, which is responsible for one part of the application UI. A React application is an aggregation of components. React can help us to build reusable components. The following diagram shows different components. All the components have different border colors. In React we assemble different components together to create an application. We use JavaScript functions or classes to make components. If we use a function, the component will be a functional component, but if we use a class, the component will be a class-based component.

Components can be:

- Functional Component / Presentational Component / Stateless Component / Dumb Component
- Class Component / Container Component/ Statefull Component / Smart Component

The classification of components above does not work for the latest version of React, but it is good to know the former definition and how the previous versions work.

So, let us change all the JSX to components. Components in React are JavaScript functions or classes, that return a JSX. Component name must start with an uppercase, and if the name is two words, it should be CamelCase - a camel with two humps.

## Big picture of components

In the previous section we agreed, that a website or an application is made of buttons, forms, texts, media objects, header, section, article and footer. If we have a million-dollar button, we can use this button all the time, instead of recreating it all over again, whenever we need a button. The same goes for input fields, forms, header or footer. That is where the power of the component comes. In the following diagram, the header, main and footer are components. Inside the main there is also a user card component and a text section component. All the different colors represent different components. How many colors do you see? Each color represent a single component. We have five components in this diagram.

![Components](../images/components_example.png)

Before we jump into React components, let's do some functions and class refreshers.

## JavaScript function

A JavaScript function could be either a regular function or an arrow function. These functions are not exactly the same there is a slight difference between them.

```js
const getUserInfo = (firstName, lastName, country, title, skills) => {
  return `${firstName} ${lastName},  a ${title} developer based in ${country}. He knows ${skills.join(
    ' '
  )} `
}
// When we call this function we need parameters
const skills = ['HTML', 'CSS', 'JS', 'React']
console.log(
  getUserInfo('Asabeneh', 'Yetayeh', 'Finland', 'FullStack Developer', skills)
)
```


