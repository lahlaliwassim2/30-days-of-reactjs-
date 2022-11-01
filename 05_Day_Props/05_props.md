<div align="center">
  <h1> 30 Days Of React: Props </h1>

<sub>Author:
<a href="https://www.linkedin.com/in/wassim-lahlali/" target="_blank">Lahlali Wassim</a><br>
<small> 01/11/2022</small>
</sub>

</div>

[<< Day 4](../04_Day_Component/04_components.md) | [Day 6 >>](../06_Day_Map_List_Keys/06_map_list_keys.md)

![30 Days of React banner](../images/30_days_of_react_banner_day_5.jpg)

- [Props](#props)
  - [Props in Functional Component](#props-in-functional-component)
  - [What is props?](#what-is-props)
  - [Props object](#props-object)
    - [Different data type props](#different-data-type-props)
    - [String props type](#string-props-type)
    - [Number props type](#number-props-type)
    - [Boolean props type](#boolean-props-type)
    - [Array props type](#array-props-type)
    - [Object props type](#object-props-type)
    - [Function prop types](#function-prop-types)
  - [Destructuring props](#destructuring-props)
  - [propTypes](#proptypes)
  - [defaultProps](#defaultprops)
- [Exercises: Components and Props](#exercises-components-and-props)
  - [Exercises: Level 1](#exercises-level-1)
  - [Exercises: Level 2](#exercises-level-2)
  - [Exercises: Level 3](#exercises-level-3)

# Props 

## Props in Functional Component

In the previous day, we saw how to inject different data types to React component JSX. Now, let us see how we use it in component and also how to pass different data as props.

## What is props?

Props is a special keyword in React that stands for properties and is being used to pass data from one component to another and mostly from parent component to child component. We can say props is a data carrier or a means to transport data.

I hope you are familiar with the JavaScript function. Most of the time, functions with parameters are smart and they can take dynamic data likewise props is a way we pass data or parameter to a component. Let's see the difference between a function and a component.

```js
// function syntax

const getUserInfo = (firstName, lastName, country) => {
  return `${firstName} ${lastName}. Lives in ${country}.`
}

// calling a functons

getUserInfo('Asabeneh', 'Yeteyeh', 'Finland')

//component syntax

// User component, component should start with an uppercase
const User = (props) => {
  return (
    <div>
      <h1>
        {props.firstName}
        {props.lastName}
      </h1>
      <small>{props.country}</small>
    </div>
  )
}
// calling or instantiating a component, this component has three properties and we call them props:firstName, lastName, country
<User firstName = 'Asabeneh', lastName='Yetayeh' country = 'Finland' />
```

In the previous section, we injected data as follows and today we will change these data to props.

```js
const welcome = 'Welcome to 30 Days Of React'
const title = 'Getting Started React'
const subtitle = 'JavaScript Library'
const author = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
}
const date = 'Oct 4, 2020'

// Header Component
const Header = () => (
  <header>
    <div className='header-wrapper'>
      <h1>{welcome}</h1>
      <h2>{title}</h2>
      <h3>{subtitle}</h3>
      <p>
        {author.firstName} {author.lastName}
      </p>
      <small>{date}</small>
    </div>
  </header>
)
```

Instead of injecting data we can also pass the data as props. React props are similar to parameters in functions.

