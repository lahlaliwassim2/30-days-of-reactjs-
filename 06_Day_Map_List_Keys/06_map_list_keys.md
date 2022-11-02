<div align="center">
  <h1> 30 Days Of React: Mapping Arrays </h1>
 

<sub>Author:
<a href="https://www.linkedin.com/in/wassim-lahlali-080894211/" target="_blank">Lahlali Wassim</a><br>
<small> 02/11/2022</small>
</sub>

</div>

[<< Day 5](./../05_Day_Props/05_props.md) | [Day 7 >>](../07_Day_Class_Components/07_class_components.md)

![30 Days of React banner](../images/30_days_of_react_banner_day_6.jpg)

- [Mapping arrays](#mapping-arrays)
  - [Mapping and rendering arrays](#mapping-and-rendering-arrays)
    - [Mapping array of numbers](#mapping-array-of-numbers)
    - [Mapping array of arrays](#mapping-array-of-arrays)
    - [Mapping array of objects](#mapping-array-of-objects)
    - [Key in mapping arrays](#key-in-mapping-arrays)
- [Exercises](#exercises)
  - [Exercises: Level 1](#exercises-level-1)
  - [Exercises: Level 2](#exercises-level-2)
  - [Exercises: Level 3](#exercises-level-3)

# Mapping arrays

An array is the most frequently used data structure to handle many kinds of problems. In React, we use map to modify an array to list of JSX by adding a certain HTML elements to each element of an array.

## Mapping and rendering arrays

Most of the time data is in the form of an array or an array of objects. To render this array or array of objects most of the time we modify the data using _map_. In the previous section, we have rendered the techs list using a map method. In this section, we will see more examples.

In the following examples, you will see how we render an array of numbers, an array of strings, an array of countries and an array of skills on the browser.

```js
import React from 'react'
import ReactDOM from 'react-dom'
const App = () => {
  return (
    <div className='container'>
      <div>
        <h1>Numbers List</h1>
        {[1, 2, 3, 4, 5]}
      </div>
    </div>
  )
}

const rootElement = document.getElementById('root')
ReactDOM.render(<App />, rootElement)
```

If you check the browser, you will see the numbers are attached together in one line. To avoid this, we modify the array and change the array elements to JSX element. See the example below, the array has been modified to a list of JSX elements.


