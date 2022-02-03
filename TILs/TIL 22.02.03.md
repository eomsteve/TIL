# TIL 22.02.03

## CSS

CSS의 클래스 우선순위에서 한가지 더 알게되었다. 원래 알고있던 순서 말고, 여러 클래스가 하나의 태그에 선언되어있을때 선언된 순서나 그런게 아니라 CSS 파일이나 style 태그안에서 정의된 순서가 우선적용되어 나온다. 가장 늦게 선언된 css가 적용된다.

```html
<style>
  .blue{
    color: blue;
  }
  .green{
    color: green;
  }
</style>
<div class="blue green"> </div>
<div class="green blue"> </div>
```

이런식의 코드가 있을경우 style에서 가장 늦게 선언된 green 이 둘다 적용된다.