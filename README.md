# vue-practice

Vue 연습용 클론코딩 프로젝트

## 1. 데이터 바인딩

js 데이터를 HTML에 넣는 문법 / HTML 속성도 데이터바인딩 가능

**자바스크립트**<br>
document.getElementById().innerHTML = ??

**vue** <br>
data에 object 자료형으로 저장후 {{ 데이터이름 }} :style="스타일"

**데이터바인딩 하는 이유**<br>

1. HTML에 하드코딩하면 나중에 변경이 어려움
2. vue의 실시간 자동 렌더링 사용

## 2. 반복문

<태그 v-for="(a,i) in array/object" :key="i"><br>
:key"" -반복문 쓸떄 필수 -반복문 돌린 요소를 컴퓨터가 구분하기 위해

## 3. 이벤트 핸들러

<태그 v-on> / <태그 @><br>
@click @mouseover ....

## 4. 조건문

<태그 v-if>
