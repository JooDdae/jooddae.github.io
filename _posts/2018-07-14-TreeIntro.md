---
title:  "[이진트리] 트리의 개념"
date:   2018-07-14 01:27:00
categories:
- Easy-Algorithm
tags:
- Tree
---

트리(tree)는 이름을 보면 아시겠지만, 나무를 닮은 구조를 가진 자료구조입니다. 나무는 뿌리, 가지, 잎 등으로 구성이 되어 있습니다. 트리 구조도 실제 나무처럼 뿌리, 가지, 잎을 가지고 있습니다.<br>

<img src = "https://i.imgur.com/q9CGd9g.png"><br>
이 트리를 한 번 봅시다.<br>
모든 사각형(노드) 는 맨 위에 있는 노드로 부터 뻗어 나옵니다. 그래서 맨 위에 있는 노드를 뿌리, 즉 루트(root)라고 부릅니다.<br>
나무에서 잎은 가장 뿌리로 부터 뻗어나온 가지를 점점 따라 가다 가장 끝에서 나옵니다. 트리에서 가지 역할을 하는것은 바로 노드와 노드를 이어주는 선 입니다. 그리고, 가장 아래에 있는 노드들을 가장 끝에 있다 해서 잎 노드 라 부릅니다.

설명을 위해 위에 있는 트리에 몇 개의 노드를 추가하고, 이름을 붙여주도록 하겠습니다.

<img src = "https://i.imgur.com/ixaDHc0.png"><br>
이 트리의 루트 노드는 A, 가지의 개수는 12개, 잎 노드는 {E, G, I, J, K, L, M}입니다.

G노드를 봅시다. G노드는 C노드에서 뻗어 나왔습니다. 그러므로 C노드는 G노드의 부모 노드입니다. 바꿔 말하면, G노드는 C노드의 자식 노드입니다.<br>
J노드는 B노드에서 몇 단계를 거쳐 도달합니다. F노드는 J노드의 부모이고, B노드는 F노드의 부모입니다. 따라서, B는 J의 조상이라 할 수 있습니다. E노드 또한 B노드를 조상으로 갖고 있습니다. 이 때, B노드를 E와 J노드의 공통 조상이라 합니다.

K노드에서 A노드로 가고 싶으면, K에서 H, D를 거쳐 A노드로 갈 수 있습니다. 이 때 {K, H, D, A}를 K에서 A까지의 경로가 됩니다.<br>
모든 경로는 길이라는 속성을 가집니다. 시작 노드에서 도착 노드까지 갈 때 거쳐야 하는 노드의 수를 길이 라고 합니다. K에서 A까지 가는 경로의 길이는 3 이 됩니다.

각각의 노드에는 깊이 라는 속성도 존재합니다. 깊이는 루트 부터 자신까지 가는 경로의 길이입니다. G의 깊이는 2고, A(루트)의 깊이는 0입니다.

또한, 트리에는 레벨과 높이라는 속성도 있습니다. 레벨은 깊이가 같은 노드들의 집합입니다. 레벨2 는 {E, F, G, H, I}를 뜻합니다.<br>
높이는 가장 깊이 있는 노드의 깊이 를 나타냅니다. 위 트리의 높이는 3 입니다.

그래프와 마찬가지로 트리도 차수(Degree) 라는 속성이 있습니다. 노드의 차수 는 각 노드의 자식의 개수를 말하고, 트리의 차수 는 자식 노드가 가장 많은 노드의 자식 수 를 나타냅니다. 위 트리의 차수는 3 입니다.

다음 글에서는 트리의 표현 방법을 다루겠습니다.