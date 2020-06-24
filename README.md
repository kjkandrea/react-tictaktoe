# 작업 일지

작업을 테스크 단위로 기록합니다.

## 앱 생성

```
npx create-react-app react-tictaktoe
```

```
npm start
```

## 스카폴딩

* src내에 기존 소스파일 삭제
* [자습서](https://ko.reactjs.org/tutorial/tutorial.html#setup-for-the-tutorial)에서 제공하는 `index.css`, `index.js` 코드 추가

## Props를 통해 데이터 전달하기

부모 Board 컴포넌트에서 자식 Square 컴포넌트로 “prop을 전달”

Board : renderSquare 에서 숫자를 i라는 인자로 받아 **부모(Board)에서 자식(Square)으로 데이터를 넘겨줌**

## 선행 연습 : 클릭 이벤트 심기

onClick 이벤트를 Square 컴포넌트에 심기

```
class Square extends React.Component {
  render() {
    return (
      <button
        className="square"
        onClick={() => alert('click')}
      >
        {this.props.value}
      </button>
    );
  }
}
```

코드 작성 후 Square를 클릭하면 얼럿이 출력됨.

`onClick={() => alert('click')}`이 어떻게 동작하는지 살펴보면 `onClick` prop으로 함수를 전달하고 있습니다. React는 클릭했을 때에만 이 함수를 호출할 것입니다. `() =>`을 잊어버리고 `onClick={alert('click')}`이라고 작성하는 것은 자주 발생하는 실수이며 컴포넌트가 다시 렌더링할 때마다 경고 창을 띄울 것입니다

## state

### props와 state 개념 정리

* `props`는 *함수 매개변수처럼* 컴포넌트에 전달되는 반면 
* `state`는 *함수 내에 선언된 변수처럼* 컴포넌트 안에서 관리됩니다.

### state 초기화 

Square 컴포넌트에 생성자(constructor)를 추가하여 state 초기화

### state 렌더링 및 클릭 이벤트 추가

setState로 클릭 시 Square를 다시 렌더링하ㅕ value : 'X' 할당