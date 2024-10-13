## 목차

1. [마크업](#마크업)
2. [스타일링](#스타일링)
3. [결론과 회고](#결론과-회고)

## 마크업

### section

> hero-store를 하나의 섹션으로 분류하고 최상위 컨테이너로 설정
>
> ### div class="hero-store\_\_search"
>
> > 매장 찾기 역할을 하는 텍스트와 링크를 div로 묶었다.
> >
> > ### hgroup
> >
> > > h2 태그와 p 속성을 사용하여 <카페 W를 경험해봅시다- 고객님과 가까운 매장을 찾으세요> 문장. 즉 섹션의 목적을 설명하고 있는 그룹을 제목 그룹으로 설정하였다.
> >
> > ### p
> >
> > > 그 외 매장의 소개들은 p 태그로 작성하고, 매장의 종류를 강조하는 부분은 strong 태그를 사용했다.
> >
> > ### a
> >
> > > '매장찾기' 박스가 form으로 본 페이지에서 정보를 보내지 않고, 단순히 매장 찾기 페이지로 넘어갈 것 같아 a 태그를 사용했다.
>
> ### ul class="hero-store\_\_photo"
>
> 부가컨텐츠인 포토들의 목록을 ul 리스트로 작성했다. 화면상에서는 왼쪽(읽는 방향)에 위치해있지만, 부가컨텐츠이니 접근성과 SEO 측면을 고려하여 HTML 구조 상 뒤쪽에 배치했다.
>
> > ### li
> >
> > span 태그로 지정할 사진의 설명을 포함했다.
>
> ### svg - 매장 아이콘 이미지
>
> > 부가 컨텐츠 그룹으로 묶어 아이콘을 지정할까 고민을 하다가, 어떤 의미값을 가지고 있지 않은 꾸밈 요소라 스타일링 편의상 role 속성에 img, 타이틀에 매장 아이콘이미지를 부여해주는 것으로 마무리 했다.

## 스타일링

## hero-store

> inline-size: 100%

> margin-top : 120px;
>
> > 화면상 떨어진 뒷배경을 표현

> background 속성 : figma의 radial-gradient 지정

> display: flex;

> flex-flow: row-reverse wrap;
>
> > html 구조와 화면상 컨텐츠 방향이 반대이기에 row-reverse 지정

> justify-content: center;
>
> > 중앙 정렬

> ## .hero-store\_\_search

> > ## hgroup, strong style
> >
> > ## p:nth-of-type(3)
> >
> > > margin-bottom 값을 주어 매장 찾기 박스와 텍스트 사이에 여백을 주었다. 좀 더 좋은 선택자 지정 방법은 없었을까 의문이 든다.

> > ## a
> >
> > > text-decoration: none 지정으로 스타일 삭제, 이후 피그마 디자인 요소를 적용했다.

> ## .hero-store\_\_photo
>
> > list-style 삭제
> >
> > ## .hero-store\_\_item
> >
> > > background: no-repeat 50% / cover;
> > > position: relative;
> > >
> > > ## span
> > >
> > > > 내부 span 태그도 block요소로 지정(추후 width/height값 할당 예정)

> ## .hero-store\_\_item:first-child
>
> > border-radius 속성으로 원모양 구현,
> > inset-block-start로 요소 시작점 계산(calc함수로 음수 구현)
> > background-image 지정

> ## .hero-store\_\_item:last-child
>
> > z-index 상위값 지정하여 사진을 위에 중첩

> ## svg
>
> > 블록요소로 지정

> > flex-shrink: 0;
> >
> > > 해당 flex 항목이 컨테이너의 공간이 부족할 때 축소되지 않도록 설정

## 결론과 회고

- 화면과 비슷한 스타일링을 디자인 파일만 가지고 마크업 해보니 전보다 자신감이 붙어서 좋았다.

- div에 role속성을 어떻게 지정할 지 찾아봐야겠다.

- 직접 마크업을 짜서 스타일링 하다보니, CSS에서 부모의 style을 어떻게 상속 받고 동작하는 지 아직 이해도가 떨어지는 것을 알 수 있었다.
  스타일링을 할 때 이 배치가 **어떻게** 표현되었는지 좀 더 구체적으로 고찰해야겠다.

- CSS 변수 사용이 미숙하고 스타일링 하기 급급하다. 짠 코드를 들여다 보는 것에도 시간을 들여야겠다.
