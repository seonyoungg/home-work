# 5주차 회고🍎

## 과제를 하면서💬

- 그리드를 사용해서 카드컴포넌트를 구현하는데 익숙한 방식이 아니라 애를 조금 먹었다.  
  이전에 그리드를 배웠을 당시 `grid-area`, `gird-column`, `grid-row` 는 어렵게도 느껴졌고, 이후 편한 방식으로 하다보니 잊고 있었던 것이었다....(부끄럽네😭)  
  사실 일반적인 레이아웃(모바일->데스크탑) 잡는 `grid-template-column` 은 익숙한 편이라 어렵지 않게 구현할 수 있었던 걸 보면 ㅋㅋㅋㅋ..

- 간단히 정리하면 이렇다.  
  grid 유용한 기능 다 빼먹고 진짜 입맛에 맞춰만 쓴 나! 반성합니다!
  - 슬비쌤의 만나기 전 나 : Grid 활용도 20%
  - 슬비쌤을 만나고 후의 나 : Grid 활용도 70-80%
  - 100%가 아닌 이유!? : `subgrid` 아직 마스터못했다... 연습해서 마스터하면 100%라고 할게요...🫡

```css
/*auto-fit/minmax로 간편하게 작성 가능한 코드였는데!!!*/
grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));

/*이전에는 바보같이 이렇게 다 나눴었음 ㅋㅋㅋㅋㅋㅋㅋ(부끄럽구만)*/
grid-tempate-columns: repeat(1, 1fr);
media (min-width:768px) {
  grid-tempate-columns: repeat(2, 1fr);
}
media (min-width:1024px) {
  grid-tempate-columns: repeat(4, 1fr);
}
```

## 과제 결과

<video src="./img/apple-md.mp4" width="500" autoplay controls></video>

<img src="./img/apple-md.gif" alt="" width=600 />
