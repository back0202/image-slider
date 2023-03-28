# Image Slider
npm install 한후 package.json에 입력된 scripts를 참고하여 dev server를 실행하거나 build 하면 됩니다.

# 로직
1. 좌 우 버튼 클릭시 슬라이더 이동
- 슬라이더 이동을 위해 현재 position과 ui의 길이를 구해서 버튼클릭스 position*ui길이 만큼 ui를 왼쪽으로 이동.
- position이 슬라이더의 길이와 같다면 position은 0으로, 해서 첫 번째 슬라이더로 이동
- position이 -1이면 position을 슬라이더 길이-1로 해서 마지막 슬라이더로 이동
2. 인디케이털
- 슬라이더 길이만큼 인디케이털 생성
- 현재 position과 인디케이털의 속성 index가 같다면 .active클래서 생성.
- 인디케이털 클릭시 속성 index로 현재 position변경, 변경이 되면 슬라이더를 현재 position으로 이동.
3. auto play
- 3초마다 오른쪽으로 이동 구현
- 좌 우 버튼 클릭시 auto play가 있다면 clear interval해서 없애 주고 다시 3초마다 오른쪽 이동 설정.
