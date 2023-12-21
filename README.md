**This repository contains a custom implementation of a Promise class in JavaScript, named ```MyPromise```. This class replicates the basic functionality of the native Promise class, including features like then, catch, finally, resolve, reject, all.**

### Table of Contents

1. States of Promise
2. MyPromise Class
3. Usage
4. Methods
   1. then
   2. catch
   3. finally
   4. resolve
   5. reject
   6. all

### 1. States of  Promise
A promise can be in one of the following states:

- Resolved (resolved): The promise has been successfully resolved with a value.
- Rejected (rejected): The promise has been rejected with a reason.
- Pending (pending): The promise is neither resolved nor rejected; its outcome is still pending.

### 2. MyPromise Class
This is the custom JS class that works exactly like a standard Promise class in JS

### 3. Usage
To use MyPromise, import the class and create a new instance by passing a callback function with resolve and reject parameters. The callback function will contain the asynchronous operation you want to perform.

```
const MyPromise = require('./MyPromise');

const promise = new MyPromise((resolve, reject) => {
  
});

promise.then((value) => {

}).catch((reason) => {

}).finally(() => {

});

```

### 4. Mathods
Internal Methods : 

`#onSuccess(value)` and `#onFail(value)`: These methods are used internally to handle the resolution and rejection of the promise. They also handle cases where the resolved or rejected value is another promise.

`#run()`: This method checks the current state of the promise and executes the corresponding callback functions (then or catch) when the promise is resolved or rejected.

1. then Method

The then method is used to attach callbacks for the resolution and/or rejection of the promise.
`onResolved`: A function called when the promise is resolved.

`onRejected`: A function called when the promise is rejected.

2. catch Method
   
The catch method is used to attach a callback for the rejection of the promise.

`onRejected`: A function called when the promise is rejected.

3. finally Method
   
The finally method is used to attach a callback that is executed when the promise is settled, whether it's resolved or rejected.

`onFinally`: A function called when the promise is settled.



