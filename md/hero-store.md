# html 구조

- section안에 figure안에 img가 포함 되도록 컴포넌트를 짰습니다.
  그렇게 이미지 1 이미지 2를 넣었고 백터이미지를 넣어 이미지 총 3개를 포함하도록 하였습니다
- ul요소 안에 h1요소를 넣었습니다. '카페 W를 가까이에서 경험해보세요.'라는 문구가 제일 두껍고 커 보였기 때문입니다. 또한 다른 문구와는 이어져 보이지 않았기에 따로 마크업 하였습니다
- li 요소 안에 span으로 묶고 두꺼운 글씨에는 strong을 주어 두껍게 표현 하였습니다.
- li 요소에 a태그를 넣어 매장찾기를 적어보았습니다.

<img src="./../src/assets/img/markup01.jpg" />

# CSS 구조

- img요소에 텍스트는 .sr-only로 가려주었습니다.
- section에는 block-size로 주어 배경을 만들었습니다
- 피그마상에 이미지 사이즈는 너무 커서 임의 값을 넣었습니다.
- 이미지는 position: absolut;를 주어 위치를 지정하였고 이미지의 부모인 section에 relative를 주어 기준을 잡았습니다.
- 이미지 요소에 border-radius를 주어 둥굴게 만들었습니다. 그리고 border-shdow값을 주어 그림자를 표현했습니다.
- a요소에는 text-decoration을 none;으로 주어 밑줄을 없앴습니다. a태그에 border와 border-radius를 주어 각진 부분을 동그랗게 처리했습니다
