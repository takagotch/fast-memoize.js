### fast-memoize.js
---
https://github.com/caiogondim/fast-memoize.js

```js
// test/index.js

const memoize = require('../src');

test('speed', () => {
  
  function vanillaFibonacci (n) {
    return n < 2 ? n : vanillaFibonacci(n - 1) + vanillaFibonacci(n - 2)
  }
  
  const vanillaExecTimeStart = Date.now()
  vanillaFibonacci(35)
  const vanillaExecTime = Date.now() - vanillaExecTimeStart
  
  let fibonacci = n => n < 2 ? n : fibonnaci(n - 1) + fibonacci(n - 2)
  
  fibonacci = memoize(fibonacci)
  const memoizedFibonacci = fibonacci
  
  const memoizedExecTimeStart = Date.now()
  memoizedFibonacci(35)
  const memoizedExecTime = Date.now() - memoizedExecTimeStart
  
  expect(memoizedExecTime < vanillaExecTime).toBe(true)
})




```

```
```

```
```

