How would you break a mock into a component heirarchy?<br>
**Answer:** 
`FilterableProductTable `<br> 
`SearchBar`<br> 
`ProductTable`<br> 
`ProductCategoryRow`<br> 
`ProductRow`<br> 

What is the single responsibility principle and how does it apply to components?<br>
**Answer:** a component should ideally only do one thing. If it ends up growing, it should be decomposed into <br>smaller subcomponents.

What does it mean to build a ‘static’ version of your application?<br>
**Answer:** State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it

Once you have a static application, what do you need to add?<br>
**Answer:** adding interactivity requires a lot of thinking and not a lot of typing.

What are the three questions you can ask to determine if something is state?<br>
**Answer:**
Is it passed in from a parent via props? If so, it probably isn’t state.<br>
Does it remain unchanged over time? If so, it probably isn’t state.<br>
Can you compute it based on any other state or props in your component? If so, it isn’t state.<br>

How can you identify where state needs to live?<br>
**Answer:** decided that our state lives in FilterableProductTable. First, add an instance property this.state = <br>{filterText: '', inStockOnly: false} to FilterableProductTable’s constructor to reflect the initial state <br>of your application. Then, pass filterText and inStockOnly to ProductTable and SearchBar as a prop. <br>Finally, use these props to filter the rows in ProductTable and set the values of the form fields in SearchBar.
