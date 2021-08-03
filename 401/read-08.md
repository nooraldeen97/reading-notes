## OO Design <br>

### SOLID principles intro <br>

**five object-oriented design (OOD) principles**<br>
- Single-responsibility Principle<br>
- Open-closed Principle<br>
- Liskov Substitution Principle<br>
- Interface Segregation Principle<br>
- Dependency Inversion Principle<br>

***Single-Responsibility Principle**<br>
- A class should have one and only one reason to change, meaning that a class should have only one job.<br>

**Open-Closed Principle**<br>
- Objects or entities should be open for extension but closed for modification.<br>

**Liskov Substitution Principle**<br>
- Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of  type S where S is a subtype of T. This means that every subclass or derived class should be substitutable <br>for their base or parent class.<br>

**Interface Segregation Principle**<br>
- A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced <br>to depend on methods they do not use.<br>

**Dependency Inversion Principle**<br>
- Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend <br>on the low-level module, but they should depend on abstractions.<br>


## OO SOLID principles in real life
**I have learned about:**<br>
- the code that follows SOLID principles is code that's a lot more likely to be maintainable<br>
s is for single responsibility principle<br>
- the single responsibility principle (srp) asserts that a class or module should do one thing only.<br>
Real life example: in your day to day life, picture those "duck" vehicles you see occasionally in some lakeside<br> towns. they're street legal and water-capable, so a duck tour affords you the unique and surreal experience of being in a 'car' that gets to the edge of the water and just keeps going. fun, right? and yet, <br>you don't see a whole lot of them because no one wants to be unable to drive to work because their boat <br>rudder is broken.<br>

**o is for open/closed principle**<br>
- the open/closed principle states that code entities should be open for extension, but closed for modification,<br> you should write a class that does what it needs to flawlessly and not assuming that people should come in<br> and change it later.<br>
- Real life example: all smartphones have app stores and these app stores let you extend the base functionality<br> of the phone which is closed for modification and they open it to an extension.

**l is for liskov substitution principle**<br>
- is the one here that is most unique to object-oriented programming. the lsp says, basically, that any child <br>type of a parent type should be able to stand in for that parent without things blowing up.<br>
- Real life example: to picture this, imagine cooking yourself a stew. if you're anything like me, you'd only put<br> things in there that were edible because you would want to eat the stew without picking through each <br>bite, asking yourself repeatedly, "is this edible?"<br>

**i is for interface segregation principle**<br>
- you should favor many, smaller, client-specific interfaces over one larger, more monolithic interface. in <br>short, you don't want to force clients to depend on things they don't actually need.<br>
- Real life example: to picture this in the real world, think of going down to your local corner restaurant and <br>checking out the menu. you'll see all of the normal menu mainstays, and then something that's just called <br>"soup of the day." why do they do this? because the soup changes a lot and there's no sense reprinting the menus every day.<br>

**d is for dependency inversion**<br>
- write code that depends upon abstractions rather than upon concrete details.<br>
- Real life example: to visualize this in your day to day, go down to your local store and pay for something with <br>a credit card. the clerk doesn't examine your card and get out the "visa machine" after seeing that your <br>card is a visa. he just takes your card, whatever it is, and swipes it. both you and the clerk depend on <br>the credit card abstraction without worrying about specifics.
