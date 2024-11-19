# vuedongsan

# 11/ 18 vuejs 공부 시작

<h2>11/19(화)</h2>

<h3>조건식</h3>

- v-if="조건식" 조건식이 참일때만 HTML에 보여줌

```
// react에선 state

  data() {
    return {
      모달창열렸니: false,
      신고수: [0, 0, 0],
      메뉴들: ["HOME", "Shop", "About"],
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },

```

<h3>이벤트 핸들러 </h3>

```
    // 자바스크립트 onclick="" 와 문화충격
    <button @click="신고수++">허위매물신고</button>
    <span>신고수: {{ 신고수 }}</span>

```

<h3> 함수 </h3>

```
 <button @click="increase">허위매물신고</button>

  methods ; {
    increase() {
    this.함수명() : 함수의 호출
    }
  }
```

<h2>11/18(월)</h2>
<h3>데이터바인딩 </h3>
<h4>하는 이유</h4>

- HTML에 하드코딩 해놓으면 나중에 변경 어려움

- Vue의 실시간 자동 렌더링

```

:속성="데이터이름"
<h4>:style="스타일">XX 원룸</h4>

```

<h3>반복문</h3>

```
  <a v-for="menu in 메뉴들" :key="menu">{{ menu }}</a>
// 반복문 쓸때 꼭 써야함
  :key="" 의 용도


```
