# Java Inheritance(상속) 사용법. 예시 코드

```java
class StudentInfo{
  protected String dept, stdNo, name;
  StudentInfo(String dept, String stdNo, String name){
    this.dept = dept;
    this.stdNo = stdNo;
    this.name = name;
  }
  public void getStdInfo(){
    System.out.println("** 학생 정보 출력 **");
    System.out.println("학과 : " + dept);
    System.out.println("학번 : " + stdNo);
    System.out.println("이름 : " + name);
  }
}
```

```java
class StudentScore extends StudentInfo{
  private int kor, eng, math, sum;
  private double ave;
  StudentScore(String dept, String stdNo, String name, int kor, int eng, int match){
    super(dept, stdNo, name);
    this.kor = kor;
    this.eng = eng;
    this.math = math;
    this.sum = 0;
    this.ave = 0.0;
  }
  public int getSum(){
    sum = kor + eng + match;
    return sum;
  }
  public double getAve(){
    ave = sum/3.0;
    return ave;
  }
  public void getStdInfo(){
    super.getStdInfo();
  }
  public void getStdScore(){
    System.out.println("** 학생 점수 출력 **");
    System.out.println("국어 : " + kor);
    System.out.println("영어 : " + eng);
    System.out.println("수학 : " + math);
    System.out.println("총점 : " + getSum());
    System.out.println("평균 : " + getAve());
  }
}
```
