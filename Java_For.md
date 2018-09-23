# Java For 반복문 사용법, 예시 코드

```java
class Ex3_13{
  public static void main(String args[]){
    int arr[] = new int[5];
    for(int i=0; i<arr.length; i++)
      arr[i] = i*10;
      
    for(int value : arr)
      System.out.println(value);
  }
}
```
