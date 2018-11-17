# canvas

## 시작하기
```html
<canvas id="myCanvas"></canvas>
```

```javascript
let canvas = document.getElementById('myCanvas');
let context = canvas.getContext('2d');

context.fillStyle = 원하는 색;
context.fillRect(x, y, width, height);

```
> 값의 단위는 px이다.

## 이미지 그리기
```html
<canvas id="myCanvas"></canvas>
```
```javascript
let canvas = document.getElementById('myCanvas');
let context = canvas.getContext('2d');

context.fillStyle = 원하는 색;
context.fillRect(x, y, width, height);
context.drawImage(src, x, y, width, height);
```
> drawImage function에 첫 번째 인자로 경로가 들어가고 두 번째 인자로 x축 좌표, y축 좌표를 지정하여 위치를 잡는다. 세 번째 인자와 네 번째 인자를 이용해 리사이징이 가능하다.
