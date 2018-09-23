# Java의 구성

## 1. Java Platform
- 자바 프로그램 실행할 수 있게 하는 '하드웨어적 프로그램'으로 자바 API와 자바 가상 머신으로 구성
<div>
<img src="https://www.oracle.com/ocom/groups/public/@otn/documents/digitalasset/1891610.png">
</div>

- 자바 API
  - 유용한 클래스, 사용 방법 문서화하여 제공
  - [JAVA SE 10 API Dcoumentation](https://docs.oracle.com/javase/10/docs/api/overview-summary.html)

- JVM(자바 가상 머신)
  - 추상적인 장치
  - 클래스 파일 => 실행할 수 있는 기계어 파일
  - 4가지 영역으로 구성
    - 클래스 영역: 실행에 필요한 클래스 로드 및 저장, 멤버 메소드 => 메소드 영역, 상수 => 상수 영역, 사용자가 작성한 클래스 코드 저장 영역
    - 자바 스택 영역: 자바 프로그램 수행하면서 발생하는 메소드 호출과 복귀에 대한 정보 생성 저장 관리
    - 힙 영역: 객체 생성 시 동적 공간 할당 객체 저장 공간. 가비지 컬렉션 기능으로 사용 끝난 객체 공간 관리되는 공간
    - 네이티브 메소드 스택 영역(Java Native Interface): 하드웨어 제어해야 할 경우 C언어와 같은 다른 언어의 기능 잠시 빌림. 네이티브 메소드 바이트 코드 변환되면서 사용하고 기록하는 영역

# Java의 데이터 타입

## 1. Java Data Type
- Primitive Type(기본 타입)
  - Numerica Type(수치 타입)
    - Integer Type(정수 타입): byte, short, int, long, char
    - Floating Point Type(부동소수점 타입): float, double
  - Boolean Type(불리언 타입): boolean
- Reference Type(참조 타입)
  - Array Type(배열 타입)
  - Class Type(클래스 타입)
  - Interface Type(인터페이스 타입)
  - Enum Type(열거 타입)

