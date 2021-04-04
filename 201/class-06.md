**Objects:** a set of variables and functions to create a model of a something you would recognize from the real world,
If a variable is part of an object, it is called a property, and If a function is part of an object, it is called a method, 
and it has a key and it set inside curly braces , there are a several ways to create objects , but the easiest way literal notation
for example : var hotel = {
name: 'Quay',
rooms : 40,
booked: 25,
checkAvailability: function() {
return this.rooms - this.booked;
}
} ;


**The Document Object Model (DOM)** specifieshow browsers should create a model of an HTML page and how JavaScript can access and update the
contents of a web page while it is in the browser window ,the Dom could be a part of html or a part of javascript , DOM queries may return 
one element, or they may return a Nodelist, which is a collection of nodes.


getElementByld( 1 id 1) Selects an individual element given the value of its i d attribute ,The HTML must have an id attribute in order for 
it to be selectable. querySelector('1css selector')Uses CSS selector syntax that would select one or more elements ,This method returns only 
the first of the matching elements, you can select one element or more than one elements and you can loop through them .


there are two methods to change the Html content ,the innerHTML property and DOM mainaplation ,You can choose different techniques depending 
on the task (and keep in mind how the site might be developed in the future).