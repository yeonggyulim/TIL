# 자료의 정렬

## 1. 정렬
    - Key: 자료 정렬 하는 데 사용하는 기준이 되는 특정 값
    - 정렬 방법의 분류
      - Internal Sort(내부 정렬): 컴퓨터 메모리 내부에서 정렬
        - 교환 방식: 키를 비교하고 교환하여 정렬하는 방식(선택 정렬, 버블 정렬, 퀵 정렬)
        - 삽입 방식: 키를 비교하고 삽입하여 정렬하는 방식(삽입 정렬, 셀 정렬)
        - 병합 방식: 키를 비교하고 병합하여 정렬하는 방식(2-way 병학, n-way 병합)
        - 분배 방식: 키를 구성하는 값을 여러 개의 부분집합에 분배하여 정렬하는 방식(기수 정렬)
        - 선택 방식: 이진 트리를 사용하여 정렬하는 방식(힙 정렬, 트리 정렬)
      - External Sort(외부 정렬): 대용량의 보조 기억 장치 사용, 대용량 자료 정렬 처리

## 2. 선택 정렬(Selection Sort)
    - 전체 원소 중 가장 작은 원소 찾아서 선택하고 첫 번째 원소와 자리 교환 => 이 과정 반복
    - 전체 비교횟수: n-1 + n-2 + ... + 1 = n(n-1)/2
    - 시간 복잡도: O(n^2)
  
## 3. 버블 정렬(Bubble Sort)
    - 인접한 두개의 원소를 비교하여 자리 교환하는 방식
    - 첫 번째 원소부터 마지막 원소까지 반복하면 가장 큰 원소가 마지막 자리로 정렬 => 이 과정 반복
    - 전체 비교횟수: n-1 + n-2 + ... + 1 = n(n-1)/2
    - 시간 복잡도: O(n^2)
    
## 4. 퀵 정렬(Quick Sort)
    - 기준 값(Pivot)을 중심으로 전체 원소들을 왼쪽 부분집합과 오른쪽 부분집합으로 분할(Divide)
    - 2가지 기본 작업을 반복 수행하여 완성
      - 분할(Divide): 정렬할 자료들을 기준 값 중심으로 2개의 부분집합으로 분할
      - 정복(Conquer): 기준값보다 작은 원소 왼쪽, 큰 원소 오른쪽. 순환 호출 이용하여 다시 분할.
    - 평균 시간 복잡도: O(nlog(sub)2(/sub)n)
    - 같은 시간 복잡도 가지는 다른 정렬 방법에 비해 자리 교환 횟수를 줄임으로써 실행 시간 성능 향상시킨 정렬 방법
    
## 5. 삽입 정렬(Insert Sort)
    - 두 개의 부분집합 S(Sorted)와 U(Unsorted)로 나뉘어 있다.
    - U의 원소를 하나씩 꺼내서 S의 마지막 원소부터 비교하면서 위치를 찾아 삽입 => 이 과정 반복
    - 평균 비교 횟수: n(n-1)/4
    - 시간 복잡도: O(n^2)

## 6. 셸 정렬(Shell Sort)
    - 일정한 간격(interval)으로 떨어져 있는 자료들끼리 부분집합 구성하고 각 부분집합에 있는 원소들에 대해 삽입 정렬 수행하는 작업
    - 매개변수 h: 부분집합 만드는 기준이 되는 간격, 한 단계 수행될 때 마다 h값 감소, 셸 정렬 순환 호출 => h가 1이 될 때 까지 반복
    - 보통 h값은 원소의 개수 1/2, 한 단계 수행시 마다 h 값을 반으로 감소 => 이 과정 반복
    - 일반적인 시간 복잡도: O(n^1.25)
    
## 7. 병합 정렬(Merge Sort)
    - 분할 정복(Divide and Conquer) 기법 사용
    - n-way 병합: n개의 정렬된 자료의 집합을 결합하여 하나의 집합으로 만드는 병합 방법
    - 2-way 병합 정렬 과정
      (1) 분할(divide): 입력 자료를 같은 크기의 부분집합 2개로 분할
      (2) 정복(conquer): 부분집합의 원소들을 정렬, 부분집합의 크기 충분히 작지 않으면 순환 호출 이용, 다시 분할 정복 기법 적용
      (3) 결합(combine): 정렬된 부분집합들을 하나의 집합으로 통합
    - 메모리 공간: 2*n개 사용
    - 시간 복잡도: O(nlog(sub)2(/sub)n)
   
## 8. 기수 정렬(Radix Sort)
    - 분배 방식의 정렬 방법
    - 정렬할 원소의 키 값에 해당하는 버킷(bucket)에 원소를 분배하였다가 버킷의 순서대로 원소를 꺼내는 방법 반복
    - 원소의 키를 표현하는 값의 기수(radix)만큼의 버킷이 필요, 키 값의 자릿수만큼 기수 정렬 반복
    - 정렬할 원소의 수 n과 키 값의 자릿수 d와 버킷의 수를 결정하는 기수 r에 따라 수행시간 달라짐
    - 수행시간: d(n+r). 정렬할 원소 n개를 r개의 버킷에 분배하는 작업 n+r와 이작업을 자릿수 d 만큼 반복
    - 시간 복잡도: O(d(n+r))

## 9. 힙 정렬(Heap Sort)
    - 최대 힙에 대해 원소의 개수만큼 삭제 연산 수행하면 내림차순 정렬 원소 얻음
    - 최소 힙에 대해 원소의 개수만큼 삭제 연산 수행하면 오름차순 정렬 원소 얻음
    - n개의 노드에 대해 완전 이진 트리는 log(sub)2(/sub)(n+1)의 레벨을 가짐
    - 평균 시간: O(log(sub)2(/sub)n) + n개의 노드에 대해 삭제 연산
    - 시간 복잡도: O(nlog(sub)2(/sub)n)
    
## 10. 트리 정렬(Tree Sort)
    - 정렬할 원소들을 이진 탐색 트리로 구성하고 중위 순회 방법을 사용하여 원소들을 꺼내면 오름차순 정렬
    - 이진 탐색 트리 구성하는 시간 O(log(sub)2(/sub)n) 이므로 n개의 노드에 대해 이진 탐색 트리 구성
    - 시간 복잡도: O(nlog(sub)2(/sub)n)
