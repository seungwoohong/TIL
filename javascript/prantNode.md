### parentNode

부모 Element 에 접근 하기

class 를 이용한 접근
```
document.querySelector('.class').parentNode
```

id를 이용한 접근
```
 document.getElementById('id').parentNode
```

현재 객체의 부모 객체의 자식 객체 가져오기
```
 document.querySelector(.class).parentNode.querySelectorAll(.class)
```

* querySelector - selector 지정한 그룹과 일치하는 document 내의 첫 번째 element를 반환한다

* querySelectorAll - selector 지정한 그룹과 일치하는 document 내의 모든 element를 반환한다. type은 object