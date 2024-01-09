# *LifeCycle process 와 각 메서드에 대해 설명*

###### React 클래스 컴포넌트에서 라이프사이클(LifeCycle)은 컴포넌트가 생성되고 소멸될 때까지의 단계를 의미합니다. React 16.3 이전에는 라이프사이클이 다양한 메서드로 구성되어 있었지만, React 16.3부터는 몇 가지 메서드가 변경되거나 추가되었습니다. 아래는 주요한 라이프사이클 메서드와 그에 대한 설명입니다.
***
## 1. 마운트(Mounting) 단계:
- *constructor*: 컴포넌트의 생성자 메서드로, 초기 상태 설정 및 메서드 바인딩 등을 수행합니다.
- *static getDerivedStateFromProps(props, state)*: props나 state가 변경될 때마다 호출되는 메서드로, 새로운 상태를 반환하여 업데이트될 상태를 결정합니다. 리액트 16.3 이후에 추가된 메서드입니다.
- *render*: 컴포넌트를 렌더링하는 메서드로, 화면에 보여질 JSX나 React 엘리먼트를 반환합니다.
- *componentDidMount*: 컴포넌트가 화면에 마운트된 후 호출되는 메서드로, 초기 데이터 로딩이나 외부 데이터 가져오기 등의 작업을 수행합니다.

***

## 2. 업데이트(Updating) 단계:
- *static getDerivedStateFromProps(props, state)*: 마운트 단계에서와 마찬가지로, 업데이트가 발생할 때마다 호출되며 업데이트될 상태를 반환합니다.
- *shouldComponentUpdate(nextProps, nextState)*: 업데이트를 할지 말지를 결정하는 메서드로, 성능 최적화를 위해 사용됩니다. true를 반환하면 업데이트를 진행하고, false를 반환하면 업데이트를 취소합니다.
- *render*: 마운트 단계에서와 마찬가지로, 컴포넌트를 렌더링하는 메서드입니다.
- *getSnapshotBeforeUpdate(prevProps, prevState)*: 리액트 엘리먼트가 실제 DOM에 반영되기 직전에 호출되는 메서드로, 현재 스크롤 위치나 컴포넌트 내부의 정보를 저장하여 업데이트 후에 복원하는데 사용됩니다.
- *componentDidUpdate(prevProps, prevState, snapshot)*: 컴포넌트가 업데이트를 완료한 후 호출되는 메서드로, 업데이트 이후의 작업을 수행합니다.

***

## 3. 언마운트(Unmounting) 단계:
- *componentWillUnmount*: 컴포넌트가 언마운트되기 직전에 호출되는 메서드로, 리소스 해제나 타이머 취소와 같은 정리 작업을 수행합니다.

***

## 5. 에러 처리(Error Handling) 단계:
- *static getDerivedStateFromError(error)*: 하위 컴포넌트에서 에러가 발생할 때 호출되는 메서드로, 에러 상태를 업데이트합니다.
- *componentDidCatch(error, info)*: 하위 컴포넌트에서 발생한 에러를 처리하고 로깅하는 메서드입니다. 에러를 캐치하고 에러 메시지를 기록하거나 사용자에게 알릴 수 있습니다.
리액트 16.3 이후에는 클래스 컴포넌트보다 함수형 컴포넌트와 훅을 사용하는 것이 권장되고 있습니다. 함수형 컴포넌트에서는 useEffect 훅과 다른 훅들을 사용하여 라이프사이클과 유사한 동작을 구현할 수 있습니다.






