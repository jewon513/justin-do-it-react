# [두잇!]리액트 프로그래밍 정석

[![두잇 리액트 표지](https://raw.githubusercontent.com/justinpark/justin-do-it-react/master/do-it-react-cover.jpeg?size=300)](http://www.yes24.com/Product/Goods/87631428?scode=032&OzSrank=1)

_여기 코드는 두잇! 리액트 프로그래밍 정석의 예제 및 연습문제 소스를 포함하고 있습니다._

## 작동 데모 주소

https://justin-do-it-react.firebaseapp.com/

## 책 오류 수정

- p.27 nvm으로 노드제이에스 설치하기
  현재 현업에서 가장 많이 사용하는 노드제이에스의 버전이 ~~8~~ 10이기 때문입니다.

  ~~nvm install 8.10.0~~

  `nvm install 10.10.0`

  ~~nvm use 8.10.0~~

```
nvm use 10.10.0
> node -v
10.10.0
```

- p.43 예제 코드 6번 항목

  ~~var args = Array.prototype.slice.call(this, arguments);~~

  var args = Array.prototype.slice.call(arguments);

- p.44 예제 코드 7번 항목

  ~~func(...args) { var [first, ...others] = args; }~~

  **function** func(...args) { var [first, ...others] = args; }

- p.112 정답 코드
  ~~this.setState((count) => {
  ~~ count: count + 1;
  ~~});

  - 중괄호{} 앞뒤로 괄호()가 포함되어야 합니다.

```
  this.setState((count) => ({
    count: count + 1;
  }));
```

- p.200 테스트 코드 실행
  ~~./src/App.test.js 파일을 삭제한 다음 실행하세요.~~

  _(App.test.js파일을 삭제하지 말고 실행하세요.)_

- p.201 <Input> 테스트 코드
  expect 예제 한줄 추가

```
    ...
    ReactDOM.unmountComponentAtNode(div);
    expect(React.isValidElement(<Input />)).toBeTruthy();
```

```
    ...
    ReactDOM.unmountComponentAtNode(div);
    expect(React.isValidElement(<Input name="test_name" />)).toBeTruthy();
```

- p.431
  `import * as serviceWorker from './serviceWorker';` 강조 색상 삭제

## 목차

### 첫째마당. 리액트 기본 익히기

#### 01. 리액트 시작하기

- 01-1 리액트의 정체를 알아보자!
- 01-2 리액트 개발 환경 설치하기
- 01-3 리액트 앱 수정하기

#### 02. 리액트 ES6 문법 액기스

- 02-1 템플릿 문자열
- 02-2 전개 연산자
- 02-3 가변 변수와 불변 변수
- 02-4 클래스
- 02-5 화살표 함수
- 02-6 객체 확장 표현식과 구조 분해 할당
- 02-7 라이브러리 의존성 관리
- 02-8 배열 함수
- 02-9 비동기 함수
- 02-10 디바운스와 스로틀

#### 03. 리액트 컴포넌트

- 03-1 컴포넌트를 표현하는 JSX
- 03-2 컴포넌트와 구성 요소
- 03-3 컴포넌트에 데이터를 전달하는 프로퍼티
- 03-4 컴포넌트 상태 관리하기
- 03-5 컴포넌트의 생명주기
- 03-6 클래스 컴포넌트
- 03-7 함수형 컴포넌트
- 03-8 배열 컴포넌트
- 03-9 컴포넌트에서 콜백 함수와 이벤트 처리하기
- 03-10 Input 컴포넌트 만들면서 복습하기

#### 04. 에어비앤비 디자인 시스템 따라하기

- 04-1 비주얼 테스트로 더 쉽게 개발하기
- 04-2 CSS로 컴포넌트 스타일 적용하기
- 04-3 스타일 컴포넌트 만들기
- 04-4 테스트 위주 개발 방법 사용해 보기
- 04-5 CheckBox 컴포넌트 만들기

### 둘째마당. 리액트 고급 기술 따라하기

#### 05. 하이어오더 컴포넌트

- 05-1 커링과 조합 개념 공부하기
- 05-2 하이어오더 컴포넌트 기초 개념 공부하기
- 05-3 하이어오더 컴포넌트 라이브러리 사용하기
- 05-4 다중 하이어오더 컴포넌트 사용하기
- 05-5 하이어오더 컴포넌트로 필수 입력 항목 표시하기

#### 06. 컨텍스트로 데이터 관리하기

- 06-1 컨텍스트의 기초 개념 알아보기
- 06-2 컨텍스트 제대로 사용하기
- 06-3 리액트 16.3 버전의 컨텍스트 API살펴보기
- 06-4 실습예제: 모달(Modal)컴포넌트 제작하기
- 06-5 입력 데이터를 관리하는 폼(Form) 작성하기

#### 07. 리덕스로 데이터 관리하기

- 07-1 리덕스 기초 알아보기
- 07-2 액션과 리듀서의 관계 알아보기
- 07-3 그래프 데이터베이스 도입하기
- 07-4 데이터를 위한 컴포넌트 알아보기
- 07-5 검색 기능 만들기

### 셋째마당. 리액트 에어비앤비처럼 개발하기

#### 08. 가상 코인 거래소 만들기

- 08-1 가상 코인 거래소 살펴보기
- 08-2 가상 코인 거래소의 공용 컴포넌트 만들기
- 08-3 프로젝트 구성하기

#### 09. 원격 데이터 연결하기

- 09-1 가상 데이터 서버 설정하기
- 09-2 데이터 요청을 위한 axios 라이브러리 도입하기
- 09-3 가상 코인 거래소에 리덕스 적용하기
- 09-4 가상 코인 거래소에 검색 기능 추가하기
- 09-5 비트코인 거래 기능 추가하며 마무리하기

#### 10. 리덕스 고급 기능 활용하기

- 10-1 미들웨어 기초 알아보기
- 10-2 redux-thunk와 비동기 제어
- 10-3 서버 지연 처리와 오류 표시하기
- 10-4 미들웨어로 알림 메시지 띄우기
- 10-5 코인 거래 알림 효과 추가하며 마무리하기

#### 11. 에어비앤비 개발 방식으로 비동기 제어하기

- 11-1 redux-pack 미들웨어로 비동기 제어하기
- 11-2 대용량 데이터 효율적으로 처리하기
- 11-3 셀렉터로 스토어 데이터 변환하기
- 11-4 axios 호출 작업 모듈화하기
- 11-5 회원 가입 기능 추가하며 마무리하기

#### 12. 리액트 라우터

- 12-1 싱글 페이지 애플리케이션
- 12-2 리액트 라우터 구성하기
- 12-3 주소와 리덕스 연결하기

#### 에어비앤비 개발자의 비밀

- 코드 스프릿팅 기법으로 bundle.js크기 줄이기
- 파이어베이스에 가상 코인 거래소 빼포하기
- 서버 사이드 랜더링 도입하기
- next.js 서버 배포하기
- 파이어베이스 DB 연결하기
