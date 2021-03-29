when we creat a web page we write tags known as markup , and it devided into two :
**1- strucral markup :**the elements that you can use to describe both headings and paragraphs 
**2- semantic markup :**which provides extra information; such as where emphasis is placed in a sentence,
that something you have written is a quotation (and who said it).

HTML has six level of headings the most imoprtant one h1 to less important one h6 and h1 bigger in size than h2 
and so on . 
**p tag:** to create a parghragh on your web page it has start tag and end tag .
**b tag:** to make the font Bold and i to make the font italic they have start tag and end tag .
**sub and sup tags :** you need them in order to write some expression like H2O it is written like H <sub>2</sub>O
and 4 to the power 2 it is wriiten like 4<sup>2</sup> .
**br :** line break tag .
**hr :** horizental line.
**em tag :** By default browsers will show the contents of an <em> element in italic.
** strong tag :** By default browsers will show the contents of an <em> element in bold .
**address tag :** to contain contact details for the author of the page.
** blockqoute :** it is used for longer quotes that take up an entire paragraph.
**cite tag:** it can be used to indicate where the citation is from.
**dfn tag :** element is used to indicate the defining instance of a new term.



***Css*** makes your website attractive , generally how does your website appear , for example it does font size ,font type , color 
background color , example make the first heading blue , bold and italic , its super important before you start coding your website
make a wireframe for it like put the (headings ,paragraphs ,and the whole stuff in your website) in boxes , that make it easier for
 you when you start coding and formatting by Css .

## use external Css by create a file and its extension should be (fileName.css) and you have to write a link tag in html 
in order to cannect them ,the link tag include href which is the css file link , type and it should be "text/css" and 
rel it should be "stylesheet", you can also include the css rules whithin the html pages by using <style> tag which 
usually sits inside the head, Css declarations sit inside curly brackets and each made of two parts a property and 
the value , seperated by semicolon.
example for extrnal Css : h3 {font-family: Arial;color: yellow;} here the values are font-size and color 
and the values are Arial and yellow .

comments in javescript is written by // or /*  */ :You should write comments to explain what your code does.
declaring a variable variable key word and then the name of it like ( var area;) to assign a value (area = 25;).
data types : 
-NUMERIC DATA TYPE like 7.8
-STRING DATA TYPE like "hello world"
-BOOLEAN DATA TYPE like true and false 
***you can store a number or string or boolaean inside the variable.***

**STRING OPERATOR :** for example var cost l = '7';
var cost2 = '9 ' ;
var total = costl + cost2 ; You would end up with a string saying '79'.

**ARITHMETIC OPERATORS :** ADDITION + ,SUBTRACTION -, divison / , INCREMENT ++ , DECREMENT -- .
**for example :**var subtotal (13 + 1) * 5;

by comparion operators you can  compare and evaluate the situation , and the result will be in boolean .
we have many camparison operators : (is equal to == and != ) it just compares the values , 
( strict equal to === and strict not equal to !===) it compares the values and the data types , greater than > and less than < 
greater than or equal >= and less than or equal to <= ,examples : '3' == 3 is true , but '3' === 3 is false because the data type 
is not the same .

logical operatores allow you comare the results of more one comarison operator , we have three logical operators 
**1- (logical and  && this operator tests more than one condition )**  both statement should be true in order the result is true .
**2 - lodical or :**this operator tests more than one condition as well, at least one statement should be true in order the result is true .
**3- logical not !** it reverses the result . if the result true it will convert it to false .

### you can excute the loops by (for , while , do while ) 
1 -for loop has three parts ( initialization , condition , update ) it makes loops with limited count .
2- while loop has a condition and it loops until the conndition is false .
3- do while loop , same of while loops but the difference it loops the first time whatever the condition is false or true .