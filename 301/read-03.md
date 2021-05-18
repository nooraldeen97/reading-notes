


## lists:
*Usually we render lists inside a component.*<br>
*When you run this code, you’ll be given a warning that a key should be provided for list items. A “key” is a special string attribute you need to include when creating lists of elements*



## Keys:
**help React identify which items have changed, are added, or are removed.**
**Keys should be given to the elements inside the array to give the elements a stable identity.**

*The best practice using indexes for keys if the order of items may change.*


What does .map() return?<br>
**Answer:** We return a `<li>`element for each item.

If I want to loop through an array and display each value in JSX, how do I do that in React?<br>
**Answer:**
we loop through the numbers array using the JavaScript `map()` function.<br>

Each list item needs a unique ____.<br>
**Answer:** key.

What is the purpose of a key?<br>
**Answer:**
Keys help React identify which items have changed, are added, or are removed.



## Spread Operator

What is the spread operator?<br>
**Answer:** The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

List 4 things that the spread operator can do.<br>
**Answer:**  Copying an array , Adding an item to a list , Adding to state in React,
Combining objects

Give an example of using the spread operator to combine two arrays.<br>
**Answer:**
`const objectOne = {hello: "🤪"}`
`const objectTwo = {world: "🐻"}`
`const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}`
`console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }`
`const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}`
`objectFour.laugh() // 😂😂😂😂😂`

Give an example of using the spread operator to add a new item to an array.<br>
**Answer:**
`const fewFruit = ['🍏','🍊','🍌']`
`const fewMoreFruit = ['🍉', '🍍', ...fewFruit]`
`console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]`

Give an example of using the spread operator to combine two objects into one.<br>
**Answer:**

`const myArray = [`🤪`,`🐻`,`🎌`]`
`const yourArray = [`🙂`,`🤗`,`🤩`]`
`const ourArray = [...myArray,...yourArray]`
`console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩`