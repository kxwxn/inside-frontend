# *effectHook이 도입된 이유와 useEffect의 효과*

###### useEffect 훅은 React 함수 컴포넌트에서 부수 효과를 수행하도록 도와주는 훅 중 하나입니다. 부수 효과란 주로 데이터 가져오기, 구독 설정, 수동으로 DOM 조작 등과 같이 순수하지 않은 작업을 의미합니다.

useEffect 훅이 도입된 이유는 여러 가지입니다:

- 라이프사이클 관리의 통일성:클래스 컴포넌트에서는 라이프사이클 메서드 (componentDidMount, componentDidUpdate, componentWillUnmount)를 사용하여 부수 효과를 처리했습니다. useEffect는 이러한 라이프사이클 메서드를 통합하여 편리하게 관리할 수 있도록 도와줍니다.

- 코드의 일관성:useEffect를 사용하면 컴포넌트의 다양한 생명주기에서 비동기 동작이나 부수 효과를 일관된 방식으로 처리할 수 있습니다. 이는 코드의 가독성을 높이고 유지보수를 용이하게 만듭니다.

- 컴포넌트 분리와 재사용:useEffect를 사용하면 부수 효과 로직을 컴포넌트에서 분리하여 독립적인 모듈로 만들기 쉽습니다. 이로써 코드의 재사용성을 높이고 로직을 명확하게 유지할 수 있습니다.

- 비동기 코드 처리:useEffect는 비동기 코드를 효과적으로 처리할 수 있는데, 이는 데이터 가져오기, API 호출 등과 같은 비동기 작업을 쉽게 수행할 수 있게 합니다.

- 클린업 로직 제공:useEffect는 컴포넌트가 언마운트 되거나 업데이트 되기 전에 클린업 로직을 수행할 수 있는 기능을 제공합니다. 이를 통해 메모리 누수나 예상치 못한 부작용을 방지할 수 있습니다.
예를 들어, 다음은 useEffect를 사용하여 컴포넌트가 마운트될 때와 언마운트될 때의 부수 효과를 처리하는 예시입니다:

```javascript
Copy code
import React, { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    // 컴포넌트가 마운트될 때 실행되는 코드
    console.log('Component mounted');

    // 컴포넌트가 언마운트될 때 실행되는 클린업 코드
    return () => {
      console.log('Component will unmount');
    };
  }, []); // 빈 배열을 전달하면 컴포넌트가 마운트될 때 한 번만 실행됨

  return <div>Hello, World!</div>;
}

export default MyComponent;
```
###### 이렇게 useEffect를 사용하면 컴포넌트의 생명주기와 관련된 작업을 효과적으로 처리할 수 있습니다.
