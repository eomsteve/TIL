# TIL 22.01.28

## 모듈화

api를 가져오는 환경에서 클래스를 이용한 모듈화를 이요했는데 지금같이 api를 이용해 데이터를 요청하고 받는 환경에서는 클래스를 만들어 한번 더 모듈화를 진행하는게 더욱 비효율적이라는것을 알게 되었다. 

## 자바스크립트

자바스크립트를 이용해 싱글톤 디자인 패턴을 설계 해 보았다. 싱글톤이 어떤 곳에서 사용되고, 왜 만들어졌는지에 대해서 알아 볼 수 있는 좋은 기회였다. 내가 만약 큰 프로잭트를 맞아 모듈화를 진행해야 한다면.. 싱긑톤이 필요할것 같다.. 내가 만든 싱글톤 코드가 자바의 싱글톤과 달리 클래스를 사용하지 않고 즉시 실행함수를 사용해 클로저을 이용한다는 것을 이해했다. 물론 js es7부터는 클래스의 constructor를 이용해 쉽게 만들 수 있다. 왜 자바스크립트의 클래스형 문법과 함수형 프로그래밍 문법이 다르게 된지 알아보아야 겠다.