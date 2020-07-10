# JSX

- 두개 이상의 태그는 무조건 하나의 태그로 감싸져 있어야 한다.

  ```react
  // 틀린 코드
  import React from 'react';
  import Hello from './Hello';
  
  function App() {
    return (
      <Hello />
      <div>안녕히계세요.</div>
    );
  }
  
  export default App;
  ```

  ```react
  // 옳은 코드
  import React from 'react';
  import Hello from './Hello';
  
  function App() {
    return (
      <div>
        <Hello />
        <div>안녕히계세요.</div>
      </div>
    );
  }
  
  export default App;
  ```

  ```react
  // 프레그먼트
  import React from 'react';
  import Hello from './Hello';
  
  function App() {
    return (
      <>
      	<Hello />
      	<div>안녕히계세요.</div>
      <>
    );
  }
  
  export default App;
  ```

  

### JSX 안에서 자바스크립트 값 사용

`{}` 으로 변수를 감싸서 사용

```react
import React from 'react';
import Hello from './Hello';

function App() {
  const name = 'react';
  return (
    <>
      <Hello />
      <div>{name}</div>
    </>
  );
}

export default App;
```









### 참고 링크

[벨로퍼트와 함께하는 모던 리액트](https://react.vlpt.us/basic/04-jsx.html)

```
// nums is passed in by reference. (i.e., without making a copy)
int len = removeDuplicates(nums);

// any modification to nums in your function would be known by the caller.
// using the length returned by your function, it prints the first len elements.
for (int i = 0; i < len; i++) {
    print(nums[i]);
}
```