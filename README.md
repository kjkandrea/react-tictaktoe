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
