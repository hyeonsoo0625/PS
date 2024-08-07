# [Gold II] 회의 장소 - 31965 

[문제 링크](https://www.acmicpc.net/problem/31965) 

### 성능 요약

메모리: 5144 KB, 시간: 176 ms

### 분류

이분 탐색, 수학, 누적 합

### 제출 일자

2024년 7월 27일 19:51:37

### 문제 설명

<p>KOI 마을에는 $N$개의 집이 수직선 위에 지어져 있다. 각 집에는 사람들이 한 명씩 살고 있다. 사람들이 살고 있는 집의 좌표를 작은 순서대로 차례대로 나열했을 때, $i$ ($1 ≤ i ≤ N$)번째 집의 좌표는 $X_i$ ($X_i > 0$)이다. 마을에 일이 생기면, 마을 사람들은 <strong>회의 세트</strong>를 통해서 일을 해결한다. 회의 세트는 마을 사람들 전체가 참여할 수도 있고, 일부만 참여할 수도 있다. 회의 세트는 회의들로 구성된다. 회의는 회의 세트의 모든 참여자들이 그중 한 사람의 집에서 모이는 방식으로 진행된다. 회의 세트에서는 모든 참여자들의 집에서 각각 한 번씩 회의를 한다. 즉, 회의 세트에 $K$명의 마을 사람들이 참여한다면, 회의 세트에서는 $K$번의 회의를 하게 된다. 회의 한 번에 필요한 <strong>비용</strong>은 회의에 참여하는 각 사람이 자신의 집에서 회의 장소인 집까지 이동하는 거리의 합이다. 회의 세트의 <strong>피로도</strong>는 각 회의를 할 때 모이는 집의 순서에 따라 달라진다. 회의 세트의 피로도는 모이는 순서에서 인접한 두 집의 회의 비용 차이의 합으로 정의한다.</p>

<p>예를 들어, 좌표 $1$, $3$, $10$, $11$, $15$에 지어진 집에 사람들이 살고 있고, $3$, $10$, $11$번 집에 사는 사람들이 회의 세트에 참여한다고 하자. 이때, 좌표가 $3$인 집에 모이기 위한 비용은 $|3 - 3| + |3 - 10| + |3 - 11| = 15$이고, 좌표가 $10$인 집에 모이기 위한 비용은 $|10 - 3| + |10 - 10| + |10 - 11| = 8$, 좌표가 $11$인 집에 모이기 위한 비용은 $|11 - 3| + |11 - 10| + |11 - 11| = 9$이다. 이때, 회의를 위해 모이는 집의 좌표 순서가 $3 - 10 - 11$일 경우, 회의 세트의 피로도는 $|15 - 8| + |8 - 9| = 8$이다. 반면, 모이는 집의 좌표 순서가 $3 - 11 - 10$일 경우, 피로도는 $|15 - 9| + |9 - 8| = 7$이다. 이 순서로 모일 때, 회의 세트의 피로도가 최소이다.</p>

<p>단, 회의 세트에 참여하는 사람이 $1$명 이하일 경우, $0$이 피로도이다.</p>

<p>KOI 마을에서는 총 $Q$번 회의 세트가 열릴 것이다. $i$번째 회의 세트는 집의 좌표가 $L_i$이상 $R_i$이하인 집에 사는 사람들이 참여한다. 각 회의 세트의 최소 <strong>피로도</strong>를 구하는 프로그램을 작성하라.</p>

### 입력 

 <p>첫 번째 줄에 $N$과 $Q$가 공백으로 구분되어 주어진다.</p>

<p>두 번째 줄에는 마을에 사람이 살고 있는 집들의 좌표 $X_i$가 증가하는 순서대로 주어진다.</p>

<p>다음 $Q$개의 줄에, 회의 세트에 대한 정보가 주어진다. $i$ ($1 ≤ i ≤ Q$)번째 줄에는 $i$번째 회의 세트에 대한 정보 $L_i$와 $R_i$가 공백으로 구분되어 주어진다.</p>

### 출력 

 <p>$Q$개의 줄을 출력한다. $i$ ($1 ≤ i ≤ Q$)번째 줄에는 $i$번째 회의 세트의 최소 피로도의 값을 출력한다.</p>

