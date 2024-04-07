# 싱글톤 패턴

날짜: 2024년 4월 1일
사람: yul2
상태: 완료
선택: 디자인 패턴과 프로그래밍 패러다임
Tag: 디자인 패턴

## 📖 요약

<aside>
📌 **디자인 패턴**

→ 프로그램을 설계할 때 발생했던 문제점들을 객체 간의 강호 관계 등을 이용하여 해결할 수 있도록 하나의 규약 형태로 만들어 놓은 것을 의미함.

</aside>

## 🫐 싱글톤 패턴(Singleton pattern)

하나의 클래스에 **하나의 인스턴스**만 가지는 패턴

인스턴스가 필요할 때, 똑같은 인스턴스를 만들지 않고 기존에 만들어 놓은 인스턴스를 다른 모듈들이 공유하며 사용

<aside>
➕ 인스턴스
객체 지향 프로그래밍에서 클래스로부터 생성된 구체적인 개체를 가리킨다.

</aside>

## 🫐 싱글톤 패턴 장점과 단점

**장점** 

- 메모리 낭비 방지
사용자가 1초에 10번 똑같은 요청을 보내면 요청을 처리하기 위한 똑같은 객체를 1초에 10번 생성하고 소멸되는 메모리 낭비 문제가 발생하게 된다.
- 속도 이득
- 데이터 공유 쉬움

**단점**

- 의존성이 높아진다.
싱글톤 패턴은 클래스의 객체를 미리 생성한 뒤에 필요한 경우 정적 메서드를 이용하기 때문에
싱글톤의 인스턴스가 변경 되면 해당 인스턴스를 참조하는 **모든 클래스들을 수정**해야 하는 문제가 발생
- private 생성자 때문에 상속이 어렵다
기본 생성자를 private로 만들었기 때문에 상속을 통한 자식 클래스를 만들 수 없다는 문제점이 있다. 즉, 자바의 객체지향 언어의 장점 중 하나인 **다형성을 적용하지 못한다**는 문제로 이어진다
- TTD(Test Driven Development)할 때 걸림돌.
싱글톤 패턴은 미리 생성된 하나의 인스턴스를 기반으로 구현하는 패턴이므로 각 테스트마다 ‘독립적인’인스턴스를 만들기 어렵다. 이는 서로 독립적이어야 하는 **단위 테스트를 하는데 문제**가 된다.

<aside>
➕ 위 같은 문제점들 때문에 싱글톤 패턴은 안티패턴이라고 불리기도 한다.

따라서 싱글톤 패턴을 직접 구현하기 보다는 **스프링**의 도움을 받아 위와 같은 문제점을 보완하면서도 싱글톤 패턴의 장점을 누릴 수 있도록 이용하고 있다.

</aside>