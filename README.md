# StudyNote
studyNote

# 용어정리
<br>

#### 객체지향 프로그래밍(OOP)
문제를 여러 개의 객체 단위로 나눠 작업하는 방식<br>
> 객체란? <br>
> 처리부분(함수)과 데이터 부분(변수)를 하나로 묶어 객체(인스턴스)라 한다.
> 물리적 또는 추상적인 것 중에서 자신의 속성과 동작을 가지는 모든것을 말한다.

* 객체지향 프로그래밍이 갖는 4가지 특징
  - 추상화
  자세한 내부정보는 숨기고 핵심적인 기능만 간추려 보여주는 것을 추상화라고 한다.
  - 캡슐화
  연관이 있는 데이터들을 묶는 작업
  - 상속
  부모와 자식으로 나뉘며 자식은 부모의 기능을 재사용 할 수 있다.
  - 다형성
  같은 명령이지만 기능이 다르게 작용하게 할 수 있다.

#### 라이브러리(Library)
프로그램을 개발하는데 있어 일종의 도구 역할, 하나의 기능을 개발하는데 있어 다양한 라이브러리를 사용할 수 있다. 어떠한 방식으로 해도 자유이다.<br>
예를 들면 무엇을 만들 때 맨손으로 만들어도 되고, 다른사람에게 만들어 달라고 부탁을해도 되고, 편의를 위한 도구를 사용해도 된다.<br>

#### 프레임워크(Frameword)
특정 프로그램을 개발하기 위한 여러 요소들과 메뉴얼인 룰을 제공하는 프로그램
 \- 틀을 안에서 일을 처리할 수 있게 하여 생산성을 높혀준다.
 \- 어떠한 규약을 지키면서 사용하여야 한다.

#### java의 대표 Collection
자바의 대표 Collection에는 List, Map, Set, Stack, Queue와 같은 것들이 있다.<br>
이 추상화된 Collection에는 인터페이스 아래, 특정한 기법으로 구현된 자료구조가 들어간다.<br>
예를 들어 List라는 인터페이스에는 구현법에 따라 ArrayList가 들어갈 수도, LinkedList가 들어갈 수도 있다.


1. List(리스트)
리스트는 배열과 비슷한 자바의 자료형으로 배열보다 편리한 기능을 많이 가지고 있다.<br>
리스트에는 대표적으로 ArrayList와 LinkedList가 있다.

    * ArrayList
자바의 Vector를 개선한, 배열로 구현된 List이다.<br>
배열과 같은 자료구조이기 때문에, 리스트 연산 수행시간 속도는 배열과 같다.

    * LinkedList
다음 노드의 주소를 기억하고 있는 List로, 배열에 비해 삽입과 삭제가 간단하다는 장점이 있다.<br>
하지만 탐색의 경우에는 첫번째 노드부터 탐색해 나가야 하기 때문에 느리다는 단점이 있다.

2. Map(맵)
Map에는 HashMap, TreeMap, LinkedHashMap이 있다<br>
    * HashMap은 일반적으로 사용하는 Map이다.
      HahTable을 사용하여 Key값에 해시함수를 적용하여 나온 index에 value를 저장하는 식이다.
      중복을 허용하지 않으며, 순서가 없다는 것이 특징이다.

    * TreeMap은Red-Black Tree 자료구조를 이용한 Map이고 Tree 구조 이기 때문에 어느정도 순서를 보장한다.

    * LinkedHashMap은 LinkedList로 구현된 HashMap이다. List로 구현되어있기 때문에 순서가 보장된다.
    하지만 LinkedList 특성상 랜덤으로 접근해서 느릴 수 있다.

3. Set(셋)
Set에는 HashSet, TresSet, LinkedHashSet이 있다.

      * HashSet은 HashMap에서 Key 값이 없는 자료형이고 집합이라고 생각해보 무방하다.
        값이 포함되어 있는지 아닌지에만 관심이 있고 순서를 보장핮디 않으며, 중복값을 허용하지 않는다
        Set중에서 가장 많이 사용된다.
      * TreeSet은 Red-Black Tree 자료구조를 사용한 Set이다.
      * LinkedHashSet은 LinkedList로 구현된 HashSet으로 순서를 보장한다.

4. Array와 ArrayList
     * Array는 길이에 대해서 Length 변수를 쓰고, ArrayList는 Size()메서드를 사용한다.
     * Array는 크기가 고정되어있지만, ArrayList는 사이즈가 동적인 배열이다.
     * Array는 int, byte, char 등과 같은 Primitive type과 Object 모두 담을 수 있지만 ArrayList는 Object만 담을 수 있다.
5. Stack과 Queue
     * 데이터를 기록하는 자료구조이며, Deque(덱)은 Stack과 Queue를 합친 형태이다. 
### 자료구조
#### Stack 
메모리 안 데이터들을 더 효율적으로 다루기 위해 만들어지 데이터 참조 방식 마지막에 들어온 데이터가 먼저 나간다.(LIFO)<br>
 \- 동전을 쌓았을 때 동전을 하나씩 꺼내려면 맨 위에 있는 동전먼저 꺼내야 한다.
  * pop() : 스택에서 가장 위 항목을 제거한다(삭제)
  * push(item) : item 하나를 스택 가장 윗 부분에 추가한다.(추가)
  * peek() : 스택의 가장 위에 있는 항목을 반환한다.(읽기)
  * isEmpty() : 스택이 비어있을 때 true 를 리턴한다.
  
#### Queue 
먼저 들어온 데이터가 먼저 나간다.(FIFO)<br>
 \-1차원 배열을 이용한 순차표현이다.<br>
 \-인덱스를 값으로 가지는 front, rear 라는 두개의 변수와 큐의 사이즈를 나타내는 n이라는 변수를 사용한다.<br>
 \-front, rear를 -1로 초기화 하여 큐가 empty임을 나타낸다.(front == rear 일 때 큐는 공백)<br>
 \-rear에서 삽입 되므로 rear가 점차 증가하여 rear==n-1 인 경우 큐는 full 인 상태.<
 * empty : front, rear를 0으로 초기화 한다.(공백)
 * enqueue : 원소을 넣을때 큐가 full인 상태인지 확인 한 후 rear를 1증가 시키고 item을 넣는다.(추가)
 * full : full의 상태를 검사하기위해 rear를 증가시켰을 때 front와 같게 된다면(rear+1 == front) full이다. (만원)
 * dequeue : 삭제하기전 큐가 empty 인지 확인하여야 하고 empty가 아니면 front를 1증가 시킨 후 그 자리의 원소를 삭제한다. (삭제)
 
------------------------------------------
### 알고리즘
#### 버블 정렬 알고리즘 (Bubble Sort)
서로 인접한 두 원소를 검사하여 순서에 맞지 않은 경우 위치를 바꾼다. <Br>
시간복잡도 : O(n^2) // 2중 반복문 <br>
 ![캡처](https://user-images.githubusercontent.com/80230648/129305607-640ae80d-8b9a-4b4e-bfd6-7013b782dcde.PNG)

 ![111](https://user-images.githubusercontent.com/80230648/129305580-3cae1525-9456-46ea-bb0f-a898bbfcd194.PNG)

 - 1회전에서 가장 큰 숫자를 맨 뒤로 밀려난다.
 - 2회전에서는 마지막숫자와는 비교하지 않는다.
 - 즉 전 회전의 마지막 자리와는 비교하지 않는다.
 - 원소가 6개면 총 5회전, 10개면 9회전
  ```
 int bubble_sort(int arr[], int n){
   int i,  j , temp;
   for(i = n-1; i>0;i--){
     for(j = 0; j > i; j++){
      if(arr[j] > arr[k+1]){
       temp = arr[j];
       arr[j] = arr[j+1];
       arr[j+1] = temp;
    }
   }
  }
}
 ```
#### 선택 정렬 알고리즘 (Selection Sort)
가장 작은 원소를 선택하여 순차적으로 배치하는 알고리즘 <Br>
시간복잡도 : O(n^2) <br>
![캡처](https://user-images.githubusercontent.com/80230648/129306706-6499975f-b93d-4cde-8787-cddc41567e1e.PNG)
![캡처](https://user-images.githubusercontent.com/80230648/129306726-b0191bc6-a50a-4b00-86a5-c13465e8c606.PNG)
- 일반적으로 첫번째 index를 min_index에 저장하여 나머지 배열들과 비교하여 더 작은 수를 맞나면 자리를 바꿔준다.
- arr[0] 부터 작은 값으로 채워 나간다.
```
 int selection_sort(int arr, int n){
  int i, j, temp, min_index;
  for(i= 0 ; i < n; i++){
   min_index = i;
   for(j = i+1; j<n; j++){
    if(arr[j] < arr[min_index){
       min_index = j;
     }
    }
    temp = arr[min_index];
    arr[min_index] = arr[i];
    arr[i] = temp;
   }
 }
```
#### 삽입 정렬 알고리즘(Insertion Sort)
앞의 원소부터 차례대로 진행하여 원소 앞의 이미 정렬된 배열에 자신의 위치를 삽입하는 알고리즘 <br>
시간복잡도: O(n^2)
 ![캡처](https://user-images.githubusercontent.com/80230648/129307541-d18327bf-343c-4817-ad35-914ec6962bb4.PNG)
- 시작할 때 arr[1] 기준으로 시작하여 앞의 배열과 크기를 비교하여 작은 순서데로 앞으로 간다.
 - 순서 위치가 맞을 경우 while문 전체를 실행하지 않기 때문에 빠르다.
```
 void insert_sort(int arr[], int n){
  int i, j, remember;
 for(i=1; i<n; i++){
     remember = arr[(j=i)];
     while(--j >= 0 && remember < arr[j]){
         arr[j+1] = arr[j];
         arr[j] = remember;
  }
  }
 }
```
##### 속도를 비교했을 때 삽입정렬알고리즘 > 선택정렬알고리즘 > 버블정렬알고리즘 순서이다.
 
 ----------------------------------------------------------
 
### 웹개발
#### WAS DB 조회나 다양한 로직 처리를 요구하는 동적인 컨텐츠를 제공하기 위해 만들어진 Application Server
  
#### DNS xxxx.xxx 형식의 주소와 IP 주소를 갖고 xxxxx.xxx형식의 주소를 받았을때 IP를 리턴해줌
#### DNS 서버란 도메인과 서버를 연결해주는 중간 서버로, 도메인 이름을 인터넷상의 주서로 변환시켜 원하는 컴퓨터를 찾아갈 수 있도록 해준다.
 \- 클라이언트 -> dns 서버 -> 서버

#### http  보안되지 않고 정보가 넘어와 공격에 취약함 일반적인 데이터는 암호화 필요없음<br>
#### https 보안되어 정보가 넘어옴 암호화를 해야함, 인증이 필요하기 때문에 접속이 끊어졌을 시 재인증을 거쳐야함<br>
#### 캐시 처리속도 향상을 위해 이미 가져온 데이터나 계산된 결과값의 복사본을 저장하여 재사용한다.
#### 디자인패턴  서비스를 편리하게 하기 위해 구조화하는 것, 틀을 만드는 것
#### 리팩토링  결과값에 변화가 없으나 코드의 구조를 재조정하여 새로운 기능을 추가하거나 유지보수 하는 행위
#### 정규화  중복된 데이터를 최소화하여 공간낭비를 최소화 하는것
#### Rest(ful) API HTTP를 더 유연하게 사용하며 자원을 추가, 수정, 삭제, 조회할 수 있도록 하는 것이며 하나의 URI가 고유한 리소스를 처리하는 공통 방식
#### 스프링과 스프링부트
 스프링 프레임워크는 자바의 대중적인 응용프로그램 개발 프레임워크이다. 의존성 주입(DI)와 제어의 역전(IOC) 스프링에서 가장 중요한 특징이다.<br>
 * 의존성 주입(DI)
   * 객체 사이에 필요한 의존 관계에 대해서 스프링 컨테이너가 자동으로 연결해 주는 것을 말한다.
   * 스프링 컨테이너는 DI를 이용하여 빈(bean) 객체를 관리하며, 스프링 컨테이너에 클래스를 등록하면 스프링이 클래스의 인스턴스를 관리해준다. 
   * 의존성이란?
     - A를 사용하기 위해서는 B가 필요하다. 그렇다면 A는 B에게 의존한다고 볼 수 있다.
 * 제어의 역전(IOC)
   * 스프링이 객체를 읽어서 heap 메모리에 올려서 갖고있는 것
 
--------------------------------------
#### cookie 와 session
 * 공통점
   * 웹 통신간 유지하려는 정보를 저장하기 위해 사용한다.
 * 차이점
   * 저장위치, 저장형식, 용량제한, 만료시점 등
   * 쿠키 : 개인 PC에 저장됨
   * 세션 : 웹 서버에 저장됨

* 쿠키와 세션을 사용하는 이유
   * HTTP의 특징이자 약점을 보안하기 위해 사용
     * Connectionless 프로토콜(비연결지향)
       - 클라이언트가 서버에 요청하였을 때 그 요청에 대해 응답을 하고 요청을 끊는 방식을 사용한다.
     * Stateless 프로토콜(상태정보 유지 안함)
       - 클라이언트의 상태 정보를 가지지 않는 서버 처리 방식이다.
       - 클라이언트와 첫번째 통신에서 데이터를 주고 받았다 하여도, 두번째 통신에서 이전 데이터를 유지 하지 않는다.
따라서 클라이언트가 요청을 보냈을 때 서버는 누구인지 계속 인증을 해줘야 한다. 이러한 일은 매우 번거로운 일이고 속도를 느리게 만드는 요인이기도 하다. <br>
그래서 사용하는 것이 쿠키와 세션이다. 클라이언트와 서버간의 정보를 유지하기 위해 사용하는 것이다.
 
 세션과 쿠키 둘 다 사용하는 이유
 > 세션은 쿠키에 비해 보안이 높으나 서버에 저장되어야 하고 서버의 자원을 사용해야 하기 때문에 세션과 쿠키를 적절하게 나누어 사용여야 한다.
 
 ##### 쿠키(Cookie) 동작 순서
 1. 클라이언트가 페이지에 접근
 2. 웹 서버는 쿠키를 생성한다.
 3. 생성한 쿠키에 정보를 담아 HTTP 화면을 돌려줄 때, 클라이언트에게 전달해 준다.
 4. 넘겨 받은 쿠키는 클라이언트가 가지고 있다가(개인 PC에 저장) 다시 서버에 요청할 때 쿠키를 전송한다.
 5. 동일 사이트 재방문시 클라이언트의 PC에 해당 쿠키가 있을 경우, 요청페이지와 함께 쿠키를 전송한다.
 ex) 아이디 비밀번호 자동입력, 팝업창을 통해 "오늘 하루 팝업 끄기" 
 
 ##### 세션(session) 동작 순서
 1. 클라이언트가 페이지 접근
 2. 서버는 접근한 클라이언트의 Reqeust-Header 필드인 cookie를 확인하여, 클라이언트가 해당 session-id를 보냈는지 확인한다.
 3. session-id 가 존재하지 않다면 서버는 session-id를 생성해 클라이언트에게 돌려준다.
 4. 서버에서 클라이언트로 돌려준 session-id를 쿠키를 사용해 서버에 저장한다.
 5. 클라이언트는 재접속 시 이 쿠키를 이용하여 session-id  값을 서버에 전달한다.
-------------------------------------------
### Node JS
  JavaScript를 백엔드에서도 사용할 수 있도록 해주는 실행 환경, 싱글스레드 비동기 기반이며 성능이 좋다. 또한 I/O가 좋으며 쉽게 코딩이 가능하다.<br>
  단, 싱글스레드이므로 복잡한 연산이 들어가는 서비스에서는 속도가 느리다.
  * 일반적으로 빠르다.
  * 거의 차단하지 않는다.
  * 통합 프로그래밍 언어 및 데이터 유형을 제공한다.
  * 모든 것이 비동기 적이다.
  * 뛰어난 동시성을 제공한다.
  #### var, let, const
    
  * var 함수 스코프를 갖는다. 변수를 한번 더 선언해도 에러가 발생하지 않는다.
  * let 블록 스코프를 갖는다. 예를 들어 {}안에서 let으로 변수 선언시 {}안에서 생성되고 사라진다.
  * const 블록 스코프를 갖는다. 상수를 선언할 때 사용하며, 선언과 동시에 할당 되어야 한다. 다른 값으로 재할당 시에 오류가 발생한다.(재할당 불가)
  
