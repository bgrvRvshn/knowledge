### Что будет выведено в консоль ?

```javascript
function test() {
	a = 10;
	console.log(a + c)
}

c = 5;
var c = 3;
a = 12;

test();
console.log(a + c);
```
Варианты:
1. 13 15
2. 13 13
3. 15 13
4. 15 15

>  2

### Что будет выведено в консоль ?

```javascript
if (true) {
	test = function () {
		console.log(1);
	}
} else {
	test = function () {
		console.log(2);
	}
}
test();
```

Варианты:
1. 1
2. 2
3. Произойдет ошибка

> 1

### Что будет находиться в this (выведено в консоль)?
```javascript
var fnTest = function() {
	console.log(this);
}

var obj = { Prop: 1 };
obj.test = fnTest;

fnTest();
obj.test();
```
Варианты:
1. obj window
2. obj obj
3. window obj
4. window window

> 3

### Что будет выведено в консоль?
```javascript
function Count() {
	var counter = 0;

	return function() {
		console.log(counter++);
	}
}

var c = new Count();

c();
c();

c.counter = 0;

c();

var b = new Count();

b();
````
Варианты:
1. 0 1 0 1
2. 0 1 0 0
3. 0 1 2 3
4. 0 1 2 0

> 4

### Через какое время в консоли выведется 'done'?
```javascript
var i; var foo;
i = 0;
function foo() {
	i++;
	if (i < 100) {
		setTimeout(foo, i);
	} else {
		console.log('done');
	}
}
foo();
```

> ~4950
