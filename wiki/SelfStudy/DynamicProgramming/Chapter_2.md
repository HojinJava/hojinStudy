##  Dynamic Programming - Chapter 2
### 링크 : [:link:](https://www.inflearn.com/course/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EA%B0%95%EC%A2%8C/)

---

## 내용 정리

* Chapter1에서 배운 내용을 활용할 수 있는 알고리즘 설명

* DP 진행 방법

  1. 수식 세우기
     1. 문제의 조건이 수식이 된다.
  2. 계산식 구현

* 중복 코드 지우기 복습

  * Memoization 방식

    * 데이터를 저장하는 M(메모리 공간)을 생성 및 초기화
      * 초기화는 무슨 값으로 할 것인가?
    * 연산이 끝난 값은 M에 저장
    * 연산 전에 M의 값이 존재 하는지 체크
      * 존재 한다면 이미 연산 한 값이므로 그 값을 돌려준다.
      * 존재 하지않는다면, 연산후 그 값을 채워준다.

  * Bottom-up 방식

    * 순차적으로 연산을 진행 해야 함(for문을 쓰기 편하기 위해서)
    * 시작점은 조건에 맞도록 설정한다
      * 시작점 : 가장 먼저 연산이 되어야 하는 곳
    * 순차적 처리 방식도 조건에 맞도록 한다.
      * 중요한 것은 모두 1번은 탐색이 되어야 하므로 쉽고 간단한 처리 방식을 기획 한다.*

    * 위 조건을 만족한다면, 순차적인 연산을 하기 때문에 중복 코드가 발생하지 않는다.

* 결론

  * Memoization이 직관적으로 코딩도 쉽고, 코드 읽기도 편하다.
  * Bottom-Up 방식의 키워드는 순차적인 방식을 설계하는 듯 하다. (3차원 이상의 배열일 경우 머리가 복잡 해 질 듯)

## 추가 내용 정리

* 다익스트라 알고리즘 : 음의 가중치가 없는 그래프에서 한 노드에서 다른 모든 노드까지의 최단 거리를 구하는 알고리즘.

## 다른 그룹원에게 질문

1. 아래 코드에서 중복연산이 발생 되는 가?

2. 발생된다면 그렇게 생각되는 이유는 무엇인가?

3. 발생된다면 중복 연산을 해결 하기 위한 방법을 말하시오.

   ~~~java
   int mat(int i, int j){
       if(i == 1 && j == 1) return m[i][j];
       else if(i == 1 ) return mat(1,j-1) + m[i][j];
       else if(j == 1 ) return mat(i-1,1) + m[i][j];
       else return Math.min( mat(i-1,j), mat(i,j-1) ) + mat[i][j]
   }
   ~~~


## 질문의 답



## 필기

* 다익스트라 알고리즘

* 순환식을 세우고 계산하는게 DP라고 할 수 있다.

  ~~~java
  int mat(int i, int j){
      if(i == 1 && j == 1) return m[i][j];
      else if(i == 1 ) return mat(1,j-1) + m[i][j];
      else if(j == 1 ) return mat(i-1,1) + m[i][j];
      else return Math.min( mat(i-1,j), mat(i,j-1) ) + mat[i][j]
  }
  ~~~

  * 위 코드에서 발생되는 중복 횟수는 어떻게 처리 할 것인지..



## 숙제

* 위 예제를 다익스트라 알고리즘으로 풀어 보기 (2018년 12월 2일까지 )


## 숙제 답



