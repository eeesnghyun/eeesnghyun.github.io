---
layout: post
title: Interview
date: 2023-06-25 14:03:36 +0530
---

<!---------------------------------- Spring ---------------------------------->
# ◼Spring
<details markdown="1">
  <summary>IoC & DI</summary>
* IoC(제어의 역전)
  * 프로그램의 제어 흐름 구조가 뒤바뀌는 것
  * 객체에 대한 제어권이 개발자가 아닌 컨테이너에 넘어가면서 객체의 생성부터 생명주기 관리까지 모든 것을 컨테이너가 맡아서 하게되는데 이를 제어권의 흐름이 바뀌었다고 하여 제어의 역전, IoC라고 한다.
* DI(의존성 주입)
  * 어떤 객체가 사용하는 의존 객체를 직접 만들어 사용하지 않고 주입 받아 사용하는 방법
  * 의존성 주입 방식
    * **Field Injection** : 필드에 @Autowired 어노테이션을 붙여 의존 관계를 주입하는 방법
    * **Setter based Injection** : setter 메소드에 @Autowired 어노테이션을 붙여 의존 관계를 주입하는 방법
    * **Constructor based Injection** : 생성자를 통해 의존 관계를 주입하는 방법. 주입받는 객체가 변하지 않도록 강제할 수 있으며, 의존성의 <u>순환 참조</u>에 대한 예방이 가능하다.(순환 참조 : A가 B에 의존하고 B가 A에 의존하는 형태)
</details>

<details markdown="1">
  <summary>AOP</summary>
* 관점 지향 프로그래밍으로 어플리케이션을 관점이라는 논리적인 단위로 분리해 관리하는 개념이다. <u>소스 코드 상에서 다른 부분에 반복해서 사용되는 코드들을 모듈화</u>하여 비즈니스 로직에서 분리해 재사용하는 것이 AOP의 핵심이다. 로깅, 트랜잭션과 같은 기능 구현에 적합하다.
* 실행 시점 - @Aspect
  * **@Before** : 메소드의 호출전 기능 구행
  * **@After** : 메소드 결과에 관계없이 완료가 되면 기능 수행
  * **@AfterReturning** : 메소드가 성공적으로 결과값을 반환한 후 기능 수행
  * **@AfterThrowing** : 메소드의 예외 발생시 기능 수행
  * **@Around** : 메소드 실행 전후 기능 수행
</details>

<details markdown="1">
  <summary>Spring Boot</summary>
스프링 프레임워크의 생산성을 향상시키기 위해 만들어진 것으로 자동 구성을 통해 기본적인 설정들을 자동으로 처리해준다. 내장형 서버를 제공하기 때문에 웹 어플리케이션을 쉽게 실행/배포할 수 있다.
</details>

<details markdown="1">
  <summary>Spring Security</summary>
* 인증과 권한으로 어플리케이션 보안을 구성하여 보안에 관련된 많은 옵션을 제공해준다.
* 스프링 시큐리티는 filter 기반으로 동작한다.
</details>

<details markdown="1">
  <summary>Filter & Interceptor</summary>
* Filter와 Interceptor는 Servlet 단위에서 실행된다.
* 순서로 봤을 때, Filter가 먼저 실행되며 Interceptor가 이후에 실행된다.
  * Filter : Filter로 지정된 자원에 대하여 요청 내용을 체크하거나 응답 정보를 체크한다.
  * Interceptor : Controller 호출하기 전/후로 작업을 가로챈다.

  ![filter](https://user-images.githubusercontent.com/47884586/131785151-cc895c25-52e5-4cbe-aab9-eeceaccc6327.png)
</details>

<br>
<!---------------------------------- ◼Web ---------------------------------->
# ◼Web
<details markdown="1">
  <summary>세션 & 쿠키</summary>
세션과 쿠키는 HTTP의 비연결성(통신 이후 연결을 끊음)과 비상태성(통신 상태를 유지하지 못함)을 보완하기 위한 기술이다.
* 세션
  * 정보를 서버에 저장한다.
  * 정보가 서버에 저장되기 때문에 보안에 좋다.
  * 서버 메모리를 차지하기 때문에 서버 부하의 위험성을 고려해야 한다.
* 쿠키
  * 정보를 클라이언트에 저장한다.
  * 서버의 자원을 사용하지 않기 때무에 속도가 빠르다.
</details>

<details markdown="1">
  <summary>동기 & 비동기</summary>
* 동기 : 순차적으로 테스크를 수행한다. 서버에 응답을 받을 때 까지 대기한다.
* 비동기 : 병렬적으로 테스크를 수행한다. 서버로부터 응답을 대기하지 않고 다음 작업을 실행한다. 응답 대기 시간이 없고 다른 작업을 할 수 있기 때문에 자원을 효율적으로 사용할 수 있다.
</details>

<details markdown="1">
  <summary>CSR & SSR</summary>
* CSR(Client Side Rendering)
  * 클라이언트측에서 <u>렌더링</u>이 일어나는 구조
  * HTML, CSS와 모든 스크립트들을 한 번에 불러오기 때문에 로딩 속도가 SSR에 비해 느리다.
* SSR(Server Side Rendering)
  * 서버측에서 렌더링 작업을 마친 상태로 클라이언트에 전달하는 구조
  * 매번 서버에 요청하기 때문에 서버 자원 사용이 많다.
  
✔ <u>렌더링</u> : HTML 파일을 받아 브라우저에 뿌려주는 과정
</details>

<br>
<!---------------------------------- JAVA ---------------------------------->
# ◼JAVA
<details markdown="1">
  <summary>JAVA8</summary>
* 람다 표현식 : 식별자없이 실행가능한 함수, 익명 함수라고도 불린다. 메소드를 람다 표현식으로 표현하면 클래스를 만들고 객체를 생성하지 않아도 메소드를 사용할 수 있다.
* Stream : 컬렉션, 배열 등에 요소들을 하나씩 참조하며 반복적인 처리를 할 수 있는 기능이다.
* java.time 패키지 : LocalTime, LocalDate, LocalDateTime 클래스
</details>

<details markdown="1">
  <summary>JVM 메모리 영역</summary>
* **Class Loader**
  * 자바 컴파일러에 의해 생성된 클래스 파일을 Runtime Data Area에 로딩한다.
* **Runtime Data Area** : JVM 메모리 영역
  * Method Area : 클래스 파일을 읽어 클래스에 대한 정보를 저장한다.
  * Heap Area : 인스턴스가 생성되는 공간. new 연산자로 생성된 객체와 배열을 저장한다.(전역변수 포함)
  * Stack Area : 기본 자료형(int, float, char, byte, boolean 등)에 해당하는 지역변수 및 매개변수의 데이터 값이 저장된다.
  * PC Register : Thread가 생성될 때마다 생기는 공간
  * Native Method Stack : 자바 이외의 다른 언어에서 제공되는 메소드의 정보가 저장된다.
* **Execution Engine**
  * Class Loader가 Runtime Data Area에 불러온 바이트 코드를 실행한다.
* **Garbage Collector**
  * Heap Area에 생성된 객체 중 참조되지 않는 객체를 제거한다.
  * JVM이 OS에 메모리를 요청할 때 실행된다.
</details>

<details markdown="1">
  <summary>Call By Value & Call By Reference</summary>
* Call By Value : 함수의 인자를 전달할 때 값을 전달하는 방식
* Call By Reference : 함수의 인자를 전달할 때 주소를 전달하는 방식
</details>

<details markdown="1">
  <summary>접근지정자</summary>
* public : 어떠한 클래스에서도 접근이 가능하다.
* private : 같은  클래스 내에서만 접근이 가능하다.
* protected : 상속받은 클래스 또는 같은 패키지에서만 접근이 가능하다.
* default : 같은 패키지에서만 접근이 가능하다.
</details>

<details markdown="1">
  <summary>변수의 기본형/참조형</summary>
* 기본형(Primitive type)
  * 논리형 : boolean
  * 문자형 : char
  * 정수형 : byte, short, int, long
  * 실수형 : float, double
* 참조형(Reference type)
  * 배열(Array)
  * 열거(Enumeration)
  * 클래스(Class)
  * 인터페이스(Interface)
</details>

<br>
<!---------------------------------- CS ---------------------------------->
# ◼CS
## OS
<details markdown="1">
  <summary>멀티스레드</summary>
* 프로그램을 실행하게 되면 하나의 프로세스가 생성된다.
* 프로세스내에는 실제 작업을 수행하는 스레드가 존재한다.
* 모든 프로세스에는 하나 이상의 스레드가 존재하여 작업을 수행한다. 이 때, 하나의 프로세스 내에 두 개 이상의 스레드가 동시에 작업을 수행하는 것을 멀티 스레드라고 한다.
</details>

## 소프트웨어 공학
<details markdown="1">
  <summary>디자인패턴</summary>
소프트웨어 공학에서 객체간 응집도를 높이고 결합도를 낮추는 좋은 코드 설계를 위한 설계 패턴을 말한다. 이를 통해 생산성을 높이고 유지보수 비용을 절감시킬 수 있다.
* 디자인 패턴은 크게 3가지 유형으로 분류된다.
  * 생성 패턴
    * 프로토 타입 패턴 : 미리 만들어진 객체를 복사해서 객체를 생성하는 방식
    * 싱글톤 패턴 : 하나의 클래스 인스턴스만 생성하여 이에 대한 전역 접근을 제공하는 방식
  * 구조 패턴
    * 브릿지 패턴 : 추상화와 구현을 분리해 인터페이스와 구현의 결합도를 약화하는 방식
    * 데코레이터 패턴 : 기존 객체에 새로운 기능을 추가하거나 오버라이드 하는 방식 
  * 행동 패턴
    * 책임 연쇄 패턴 : Request를 바로 처리할 수 없을 경우 여러 객체를 사슬처럼 연결하고 요청을 해결할 객체를 만날 때까지 객체의 사슬을 따라 요청을 전달한다.
</details>

<details markdown="1">
  <summary>방법론</summary>
</details>

<details markdown="1">
  <summary>TDD</summary>
</details>

<details markdown="1">
  <summary>모놀리식 아키텍처(Monolithic Architecture) vs 마이크로서비스 아키텍처(MicroService Architecture)</summary>
* **모놀리식 아키텍처** : 소프트웨어의 모든 구성요소가 한 프로젝트에 통합 되어 있는 형태
  * 장점
    * 소규모 프로젝트에서는 합리적이고, 개발,빌드,배포,테스트가 용이하다.
  * 단점
    * 어플리케이션 구동시간이 늘어나고 빌드,배포 시간이 길어진다.
* **마이크로서비스 아키텍처** : 하나의 큰 애플리케이션이 여러 개의 작은 서비스 유닛으로 쪼개진 형태
  * 장점 
    * 독립적인 서비스로 배포가 빠르고 모놀리식보다 가볍다.
    * 각 서비스에 따라 개별적으로 서버를 나눌 수 있어 메모리 및 cpu 관리에 효율적이다.
  * 단점 
    * 서비스 간 호출 시 REST API 사용으로 인한 통신비용, Latency(지연시간)가 증가한다.
    * 서비스가 분산되어 있어 트랜잭션 관리, 장애 추적 및 테스트 등이 쉽지 않다.
</details>

## 자료구조
<details markdown="1">
  <summary>배열</summary>
</details>

<details markdown="1">
  <summary>리스트</summary>
</details>

## 데이터베이스
<details markdown="1">
  <summary>Index</summary>
* Index는 데이터의 검색 성능을 향상시켜주는 자료 구조이다.
* Index 원리
  * 테이블에는 <u>데이터의 주소</u>를 나타내는 ROWID(오라클 표기법)가 있다.
  * 테이블 A 컬럼의 인덱스를 생성하면 해당 컬럼과 ROWID로 구성된 인덱스 테이블이 생성된다.
  * A 컬럼을 조건으로 테이블을 조회하면 인덱스 테이블에 해당 ROWID를 참조해서 테이블 레코드의 값을 가져온다.
* Index를 사용하기 좋은 기준
  * WHERE 절이나 JOIN 조건시 자주 사용되는 컬럼
</details>

## 네트워크
<details markdown="1">
  <summary>OSI 7계층</summary>
* **물리 계층**
  * 전기, 기계, 기능적인 특성을 이용해 데이터를 전송한다.
  * 데이터 단위 : 0과 1로 이루어진 비트열

* **데이터 링크 계층**
  * 물리적인 연결을 통하여 인접한 두 장치 간의 신뢰성 있는 정보 전송을 담당(Point-To-Point 전송)
  * 데이터 단위 : 프레임(Frame)

* **네트워크 계층**
  * 데이터를 목적지까지 안전하고 빠르게 전달하는 라우팅 기능을 맡고 있다.
  * 데이터 단위 : 패킷(Packet)

* **전송 계층**
  * 종단 간 신뢰성 있고 정확한 데이터 전송을 담당한다.
  * 데이터 단위 : 세그먼트(Segment)

* **세션 계층**
  * 통신 장치 간 상호작용 및 동기화 제공

* **표현 계층**
  * 코드 간의 번역을 담당하여 사용자 시스템에서 데이터의 형식상 차이를 다루는 부담을 응용 계층으로부터 덜어 준다.
  * 인코딩이나 암호화 등의 동작이 이 계층에서 이루어진다.

* **응용 계층**
  * 응용 프로세스 간의 정보 교환을 담당
  * HTTP, FTP, SMTP, POP3, IMAP, Telnet 등과 같은 프로토콜이 있다.
  
</details>



<br>
<!---------------------------------- Algorithm ---------------------------------->
# ◼Algorithm
<details markdown="1">
  <summary>시간복잡도</summary>
* 시간 복잡도는 어떤 문제를 해결하는 알고리즘이 걸리는 시간을 의미한다.
* 시간 복잡도는 Big-O(빅-오) 표기를 이용해 정의할 수 있다.

```
- O(1) : 일정한 복잡도. 입력값이 증가하더라도 시간이 늘어나지 않는다.
- O(n) : 선형 복잡도. 입력값이 증가함에 따라 같은 비율로 증가한다.
- O(log n) : 로그 복잡도. Big-O 표기법중 O(1) 다음으로 빠른 시간 복잡도를 가진다.
- O(n log n) : 선형 로그형. n * log₂ n만큼의 수행 시간을 가진다.
- O(n²) : 2차 복잡도. 입력값이 증가함에 따라 시간이 n의 제곱수로 증가한다.
- O(2ⁿ) : 기하급수적 복잡도. Big-O 표기법 중 가장 느린 시간 복잡도를 가진다.
```

</details>

<details markdown="1">
  <summary>정렬알고리즘</summary>
* **버블 정렬(Bubble Sort)** : 인접한 두 원소를 비교해 서로 위치를 교환하는 방식의 정렬 알고리즘. 
  
  ※ 평균 및 최악의 경우 시간 복잡도 : <u>O(n^2)</u>
  ```

  ```
* **선택 정렬(Selection Sort)** : 주어진 리스트에서 최소값을 찾아 앞에 위치한 값과 교환하는 방식의 정렬 알고리즘. 최소값을 선택하는 과정을 반복해 정렬을 수행한다.

  ※ 평균 및 최악의 경우 시간 복잡도 : <u>O(n^2)</u>
  ```

  ```
* **삽입 정렬(Insertion Sort)** : 리스트를 정렬된 부분과 정렬되지 않은 부분으로 나누고 정렬되지 않은 부분의 값을 정렬된 부분에 삽입하는 방식으로 정렬을 수행한다. 작은 크기의 리스트나 정렬된 상태에서는 효과적이지만 최악의 경우 다른 알고리즘보다 성능이 떨어질 수 있다.

  ※ 평균 및 최악의 경우 시간 복잡도 : <u>O(n^2)</u>
  ```

  ```
* **퀵 정렬(Quick Sort)** : 리스트에서 하나의 요소를 기준으로 잡고, 기준보다 작은 값은 욎쪽으로, 큰 값은 오른쪽으로 분할하여 재귀적으로 정렬을 수행한다. 평균적으로 빠른 속도를 가지는 알고리즘 중 하나이지만 최악의 경우 성능이 떨어질 수 있다.

  ※ 평균 시간 복잡도 : <u>O(n log n)</u> / 최악의 경우 시간 복잡도 : <u>O(n^2)</u>
  ```

  ```
* **병합 정렬(Merge Sort)** : 리스트 절반으로 잘라 정렬하고, 정렬된 두 개의 리스틀 병합해 전체 리스트를 정렬한다. 안정적이면서 효율적인 알고리즘이지만 추가적인 메모리 공간이 필요하다는 단점이 있다.

  ※ 평균 및 최악의 경우 시간 복잡도 : <u>O(n log n)</u>
  ```

  ```
* **힙 정렬(Heap Sort)** : 완전 이진트리 구조를 활용하여 정렬을 수행한다. 주어진 리스트를 힙으로 만들고, 힙에서 최대값(또는 최소값)을 추출해 정렬된 순서로 배열한다.

  ※ 평균 및 최악의 경우 시간 복잡도 : <u>O(n log n)</u>
  ```

  ```
</details>

<details markdown="1">
  <summary>페이지 교체 알고리즘</summary>
* **FIFO(First In First Out)** : 가장 먼저 메모리에 올라온 페이지를 가장 먼저 내보내는 알고리즘
* **OPT(Optimal)** : 앞으로 가장 오랫동안 사용하지 않을 페이지를 교체하는 알고리즘
* **LRU(Least Recently Used)** : 가장 오랫동안 사용하지 않은 페이지를 교체하는 알고리즘
* **LFU(Least Frequently Used)** : 참조 횟수가 가장 적은 페이지를 교체하는 알고리즘
* **MFU(Most Frequently User)** : 참조 횟수가 가장 많은 페이지를 교체하는 알고리즘
</details>

<details markdown="1">
  <summary>탐색 알고리즘</summary>
* 순차 탐색(Sequential Search)
  * 정렬되지 않은 리스트의 항목들을 처음부터 마지막까지 하나씩 순차 검색하는 탐색 방법.
  * 데이터 집합의 크기가 커지면 최악의 경우 모든 원소를 확인해야하므로 효율성이 떨어진다.
  * 시간 복잡도 : O(n)
* 이진 탐색(Binary Search)
  * 정렬된 데이터 집합에서 사용할 수 있는 탐색 방법으로 원하는 값을 찾을 때가지 배열의 반을 쪼개어가며 탐색 범위를 좁혀나간다. 
  * 시간 복잡도 : O(log n)
* 색인 순차 탐색(Indexed Sequential Search)
  * 정렬되어 있는 자료에 대해 인덱스 테이블을 사용해 탐색 효율을 높이는 탐색 방법.
* 보간 탐색 방법
  * 정렬된 리스트에서 찾고자 하는 값의 위치를 예측하여 탐색하는 방법.

</details>