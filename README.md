# Building a Star Rating Component

 -  ``` npm i react-icons ```

First, we’ll need a star,
and we can get one from **react-icons**. **react-icons** is an npm library that contains hundreds of SVG icons
that are distributed as React components.


- ``` javascript
       import React from "react";
       import { FaStar } from "react-icons/fa";
       
       export default function StarRating() {
        return [
         <FaStar color="red" />,
         <FaStar color="red" />,
         <FaStar color="red" />,
         <FaStar color="grey" />,
         <FaStar color="grey" />
        ];}

Here, we’ve created a **StarRating** component that renders five SVG
stars that we’ve imported from react-icons. The first three stars are
filled in with red, and the last two are grey.

- Create a component that automatically files the stars based upon the selected property
   ```javascript
      const Star = ({ selected = false }) => (
      <FaStar color={selected ? "red" : "grey"} />
      );

- Now we should give some styles, because we can have different kind of components with different styles...
    ```javascript
      export default function App() {
      return <StarRating style={{ backgroundColor: "lightblue" }} />;
      }
      ///////////////////////////////////////
     <div style={{ padding: "5px", ...style }}>

- 