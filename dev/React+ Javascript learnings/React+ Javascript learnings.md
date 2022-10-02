**JavaScript Learnings**

- **map vs forEach**

Both are used for iterating inside an object – 

1. map return an array(newly created without affecting original array) whereas forEach doesn’t return anything(undefined).

var array = [1, 4, 5, 6];

var map\_array = array.map((ele, idx)=> { return ele\*2});

console.log(array, map\_array);

// [ 1, 4, 5, 6 ] [ 2, 8, 10, 12 ]

![](Aspose.Words.176ade07-df9f-45ab-bd79-f36f55d598ae.001.png)






1. Both accept a function in their callback, and it automatically takes (element, index, array) as a parameter.

Eg map(cb1), forEach(cb2)


- **ERROR : Form data sent is empty**

While sending json post request in express, to get it in body we need to parse it using body-parser or we can use inbuilt express json parser 

Parse meaning - JSON. parse() is **a crucial method for converting JSON data in string form into Javascript objects**

app.use(express.json()); 

- **React component functions**

If a function is to be run when onClick happens, we do it like-

`	`<div onClick = {func}><div>

If it had been func(), the function would have run while rendering only. So, this saves us from that. 

What if we had to pass parameter into the function func? We can’t use func(x) as this will run while rendering.

Solution – 

Define a function there.

`	`<div onClick = {()=>{func(xyz)}></div>

It works!




