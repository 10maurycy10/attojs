# attoJS

The smallest high preformance JS framework.

## Features

tinyJS allows you to use multiple common disign patterns in your code, these include:

- data hiding

- function composition

- lambda functios

## Examples

- data hiding (parameters)

```js
$ = require("attojs")

let cat = (name)=>{return {meow: ()=>console.log(`${name} meows`)}}

let my_cat = $(cat,"bob")

// we dont have accses to the name data
my_cat.meow()
```

- data hiding (state)

```js
$ = require("attojs")

let id = $(()=>{
	let id = 0
	return {
		getid: ()=>(id++)
	}
})

// this will print 0
console.log(id.getid());
// this will print 1
console.log(id.getid());

// we dont have acces to the inner state of id
```

- function composition

```js
$ = require("attojs")

function makelog(id) {
	return `this is log ${id}`
}

let logid = (id)=>console.log(makelog(id))

$(logid,1)
```

- lambda functios

```js
((x) => {x + 1})(1) // 2
```
