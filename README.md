Qs 1. Given an integer n, return a counter function. This counter function initially returns n and then returns 1 more than the previous value every subsequent time it is called (n, n + 1, n + 2, etc).

** ( Solution 1 ) :**
=> var createCounter = function (n) {
    let counter = -1;
    return function () {
        counter++;
        return n + counter;
    };
};

let data = createCounter(10);
console.log(data()); // 10
console.log(data()); // 11
console.log(data()); // 12
console.log(data()); // 13

**Output:**
=> 10 ,11 ,12 ,13 , so on.....


** ( Solution 2 ) :**
=>  var createCounter = function(n) {
  return function() {
     console.log("value of n before n++ : ",n) 
    return [n++],[ `value of n after n++ ${n}`];      
  };
};

let data = createCounter(10);
console.log(data()); // 10
console.log(data()); // 11
console.log(data()); // 12
console.log(data()); // 13

**Output:**

value of n before n++ :  10
[ 'value of n after n++ 11' ]
value of n before n++ :  11
[ 'value of n after n++ 12' ]
value of n before n++ :  12
[ 'value of n after n++ 13' ]
value of n before n++ :  13
[ 'value of n after n++ 14' ]
