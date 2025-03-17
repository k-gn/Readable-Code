# Readable Code

## 중요하게 생각해야 할 개념

1. 추상
2. 논리, 사고의 흐름
3. 객체 지향 패러다임

> 도메인 : 해결하고자 하는 문제 영역

> 도메인 지식 : 도메인을 이해하고 해결하는 데 필요한 지식

# 클린코드를 추구하는 이유?
- 좋은 가독성
- 유지보수 수월
- 시간과 자원의 절약 => 우리가 짠 코드가 잘 읽히도록 작성하는 것이 굉장히 중요!

> 프로그램 : 데이터 + 코드

# 추상과 구체
- 추상 : 중요한 정보는 가려내어 남기고, 덜 중요한 정보는 생략하여 버린다.
- 정보 함축, 제거 = 추상화
- 적절한 추상화는 복잡한 데이터와 복잡한 로직을 단순화하여 이해하기 쉽도록 돕는다
  - 읽기가 좋다.
  - 적절한 추상화는 해당 도메인 문맥 안에서 가장 중요한 핵심 개념만 남겨 표현하는 것

- 추상화 레벨이 높다 = 고수준
- 추상화 레벨이 낮다 = 저수준

- 추상으로부터 구체를 유추하지 못하는 경우
  - 추상화 과정에서 중요한 정보를 부각시키지 못함
    - 상대적으로 덜 중요한 정보를 남기고 중요한 정보는 제거한 경우
  - 해석자가 동일하게 공유하는 문백이 없는 경우
    - 중요한 정보의 기준이 다를 수 있다.
    - 도메인 영역 별 추상화 기준(도메인 지식)이 다를 수 있다.

---

## 이름 짓기

1. 단수와 복수를 구분하기
2. 이름 줄이지 않기
3. 은어/방언 쓰지 않기 (도메인 용어 사용하기)
4. 아무 의미없는 이름 쓰지 않기 (ex. a, c1)

## 추상화

1. 전체 맥락을 포괄하는 의미를 가진 함수명을 주어야 한다.
2. 한 메서드의 주제는 반드시 하나이다.
3. 메서드 선언부
  - 추상화된 구체를 유추할 수 있는 적절한 의미가 담긴 이름
  - 파라미터와 연결지어 더 풍부한 이름 전달
    - 파라미터의 타입, 개수, 순서를 통해 의미 전달
    - 파라미터는 외부와 소통하는 창구
  
4. 메서드 시그니처에 납득이 가는 적절한 반환값 돌려주기
5. 항상 고민해야 할 것
  - 정확한 의미로 메서드 명이 추출되었나?
  - 메서드가 2가지 이상의 일을 하고있진 않을까?
  - 파라미터는 이게 맞을까?
  - 반환타입은 이게 맞을까?

6. 추상화 레벨을 주변과 동등하게 한다.
7. 매직넘버, 매직스트링
  - 의미를 갖고 있으나, 상수로 추출되지 않은 숫자나 문자열
  - 상수 추출로 이름을 짓고 의미를 부여함으로써 가독성 및 유지보수성 증가

---

## 논리, 사고의 흐름

- 뇌 메모리에 적은 정보를 올리도록 코드를 작성할수록 읽기 쉬운 코드가 된다.

1. Early Return
  - else if 또는 else 를 지양하자  (switch-case 문도 동일)
  - 일찍 return 할 수 있으면 빠르게 하자

2. depth 줄이기
  - 중첩 반복문, 중첩 분기문 줄이기
  - 무조건 depth 를 줄이는데 급급한 것이 아니다.
    - 사고 과정의 depth 를 줄이는 것이 중요.
    - 때로는 메서드를 추출하는 것이 더 혼선을 줄 수 있다.
  - 사용할 변수는 가깝게 선언하자

