
# Java Enum(열거 타입) 사용법, 예시 코드

```java
enum Week{
  MON, TUE, WED, THU, FRI, SAT, SUN
}
```

```java
class Ex3_7{
  public static void main(String args[]){
  Week myWeek = Week.FRI;
  Week yourWeek = Week.SAT;
  System.out.printf("My special day : (%s) \n". myWeek);
  System.out.printf("Your special day : (%s) \n". yourWeek);
  }
}
```
  
```java
class Ex3_10{
  public static void main(String args[]){
    Week nonWeek = Week.FRI;
    switch(nonWeek){
      case MON:
        System.out.println("오늘은 월요일.");
        break;
      case TUE:
        System.out.println("오늘은 화요일.");
        break;
      case FRI:
        System.out.println("오늘은 금요일.");
        break;
      default:
        System.out.println("오늘은 일요일.");
    }
  }
}
```
