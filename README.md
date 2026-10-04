# Week 5 JavaScript CRUD

## Deployment

- Vercel URL: (https://oss5-murex.vercel.app/)

## Key Learning

1. JavaScript를 이용하여 화면에 기능을 추가하는 방법을 배웠다.
2. JavaScript Array와 객체를 사용하여 데이터를 저장하고 관리하는 방법을 배웠다.
3. 수정 버튼을 누르면 기존 데이터를 Form에 다시 표시하고 수정하는 과정을 배웠다.

## CRUD Service

### 주제

영화 관리 프로그램

### 데이터 Field

- id: 영화 고유 번호
- title: 영화 제목
- director: 감독
- year: 개봉년도
- genre: 장르
- rating: 평점

### CRUD 구현

- Create: Form의 입력값으로 객체를 만들고 `push()`로 배열에 추가했다.
- Read: `forEach()`로 배열의 영화를 하나씩 꺼내 Table에 출력했다.
- Update: `find()`로 ID가 같은 영화를 찾아 값을 변경했다.
- Delete: `filter()`로 삭제할 영화를 제외한 새로운 배열을 만들었다.

## JavaScript

### querySelector()

CSS 선택자를 이용하여 HTML 요소를 찾을 때 사용했다.

```javascript
const form = document.querySelector("#movie_form");
```

### addEventListener()

Form 제출 이벤트와 페이지 load 이벤트를 연결할 때 사용했다.

```javascript
form.addEventListener("submit", addMovie);
```

### createElement()

Table에 새로운 행을 만들 때 사용했다.

```javascript
const row = document.createElement("tr");
```

### Array

영화 데이터를 객체 형태로 저장하기 위해 사용했다.

```javascript
let movies = [];
```

### render()

배열에 저장된 영화 데이터를 Table에 출력하는 함수이다. 영화를 추가, 수정, 삭제한 후 `render()`를 호출하여 화면을 다시 표시했다.

## AI / Search Usage

- Tool: ChatGPT
- Purpose: 배열의 기능과 HTML Table 구조를 공부하기 위해 사용했다.
- Used: `filter()`, `find()` 등의 Array 함수와 `th`, `td`를 사용하는 Table 구조를 CRUD 기능에 적용했다.
- Used: CSS를 작성할 때 Form과 Table을 구분하는 기본적인 디자인 아이디어를 참고했다.
- Used: README.md를 작성할 때 Markdown 문법과 기본 구성을 참고한 후 직접 수정했다.
- Used: 직접 함수를 작성한 뒤 문제가 발생했을 때 원인을 확인하고 디버깅하는 데 사용했다.
- What I Learned: `find()`는 조건에 맞는 첫 번째 데이터를 반환하고, `filter()`는 조건에 맞는 데이터로 새로운 배열을 만든다는 것을 이해했다.

## Problem & Solution

처음 `addEventListener()`를 사용할 때 실행할 함수 자리에 `addFruit()`를 작성하여 페이지가 열릴 때 함수가 바로 실행되는 문제가 있었다. 괄호를 제거하고 `addFruit`를 전달하여 클릭할 때 함수가 실행되도록 해결했다.

## Reflection

JavaScript Array만으로도 간단한 CRUD 서비스를 만들 수 있다는 것을 알게 되었다. 처음에는 배열의 내용과 화면의 HTML을 같이 변경해야 한다고 생각했지만, 배열을 먼저 변경하고 `render()`를 호출하면 화면을 다시 만들 수 있다는 것을 이해했다. Event 함수에 함수를 전달할 때 함수 이름과 함수 실행 결과의 차이도 알게 되었다.