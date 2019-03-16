---
title:  "[이진트리] 이진트리의 순회"
date:   2018-07-16 00:27:00
categories:
- Easy-Algorithm
tags:
- Tree
---
지난 글에서는 이진트리의 간단한 구현 방법을 다뤘습니다.<br>
이번 글에서는 이진트리의 전위, 중위, 후위 순회에 대해 알아봅시다.

#### 전위순회
전위순회는
1. 루트 노드에서 시작해서
2. 왼쪽 하위 트리를 방문하고
3. 오른쪽 하위 트리를 방문하는 방식입니다.
<img src = "https://i.imgur.com/pZTcwtV.png">
이 트리에서 전위순회를 해봅시다.<br>
먼저, 왼쪽 하위 트리와 오른쪽 하위트리를 구분합니다.
<img src = "https://i.imgur.com/jD86aX4.png">

가장 먼저 루트 노드를 방문합니다.<br>
현재 방문 목록{1}

그 다음에는 왼쪽 하위 트리를 방문합니다.<br>
왼쪽 하위 트리의 루트 노드를 방문합니다.<br>
현재 방문 목록{1, 2}

그 다음은 2번 노드의 왼쪽 자식인 4를 방문합니다.<br>
현재 방문 목록{1, 2, 4}

그리고 2번 노드의 오른쪽 자식인 5를 방문합니다.<br>
현재 방문 목록{1, 2, 4, 5}

전체 트리의 왼쪽 하위 트리 방문을 끝냈으니 오른쪽 하위 트리를 방문합니다.

오른쪽 하위 트리의 루트 노드를 방문합니다.<br>
현재 방문 목록{1, 2, 4, 5, 3}

그 다음으로는 왼쪽 자식과 오른쪽 자식을 각각 방문하고 순회를 마칩니다.<br>
최종 방문 목록{1, 2, 4, 5, 3, 6, 7}

#### 중위순회
중위순회는
1. 왼쪽 하위 트리를 먼저 방문하고
2. 루트 노드를 방문한 뒤
3. 오른쪽 하위 트리를 방문하는 순회 방법입니다.

위에서 사용한 트리를 그대로 사용합시다.

가장 먼저 왼쪽 하위 트리를 방문합니다. (이 트리를 L이라고 칭하겠습니다.)<br>
L의 왼쪽 자식을 방문합니다.<br>
현재 방문 목록{4}

다음으로 L의 루트 노드를 방문합니다.<br>
현재 방문 목록{4, 2}

그 다음에는 L의 오른쪽 자식을 방문합니다.<br>
현재 방문 목록{4, 2, 5}

L을 모두 방문 했으므로 전체 트리의 루트 노드를 방문합니다.<br>
현재 방문 목록{4, 2, 5, 1}

루트 노드를 방문 했으므로 오른쪽 하위 트리를 방문합니다. (R이라고 칭하겠습니다.)<br>
R의 왼쪽 자식을 방문합니다.<br>
현재 방문 목록{4, 2, 5, 1, 6}

R의 루트노드와 오른쪽 자식을 차례로 방문하고 순회를 종료합니다.<br>
최종 방문 목록{4, 2, 5, 1, 6, 3, 7}

#### 후위순회
후위순회는
1. 왼쪽 하위 트리를 방문하고
2. 오른쪽 하위 트리를 방문한 뒤,
3. 루트 노드를 방문합니다.

먼저 왼쪽 하위 트리를 방문합니다. (L이라고 칭하겠습니다.)<br>
L의 왼쪽 자식을 방문합니다.<br>
현재 방문 목록{4}

L의 오른쪽 자식를 방문합니다.<br>
현재 방문 목록{4, 5}

L의 루트 노드를 방문합니다.<br>
현재 방문 목록{4, 5, 2}

그 다음으로 오른쪽 하위 트리를 방문합니다. (R이라고 칭하겠습니다.)<br>
R의 왼쪽 자식을 방문합니다.<br>
현재 방문 목록{4, 5, 2, 6}

R의 오른쪽 자식을 방문합니다.<br>
현재 방문 목록{4, 5, 2, 6, 7}

R의 루트 노드를 방문합니다.<br>
현재 방문 목록{4, 5, 2, 6, 7, 3}

마지막으로 루트 노드를 방문합니다.<br>
최종 방문 목록{4, 5, 2, 6, 7, 3, 1}

<hr>

여기까지가 이진 트리 순회에 대한 설명입니다.