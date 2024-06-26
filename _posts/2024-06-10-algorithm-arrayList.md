---
title: ArrayList 와 LinkedList
author: winnie
date: 2024-06-18 14:10:00 +0800
categories: [Alogrithm]
render_with_liquid: false
---


## Array
배열은 동일한 타입의 데이터들이 순차적으로 메모리에 저장되는 자료구조입니다.
인덱스를 통한 직접 접근이 가능하기 때문에 탐색 속도가 빠르다는 장점이 있습니다.
하지만 크기가 고정되어 있으며 동적으로 변경할 수 없다는 단점이 있습니다.
변경이 필요한 경우 배열을 새로 생성한 후 기존의 요소들을 복사하여야 합니다.


## ArrayList
동적 배열 기반의 리스트 자료구조입니다. 내부적으로 배열을 사용하여 요소를 저장하며
요소의 추가나 삭제에 의해 크기가 동적으로 조정됩니다.

ArrayList는 생성할 때 초기 용량을 설정할 수 있으며 기본으로 10 으로 설정됩니다.
내부 배열의 용량이 초과되면 ArrayList 는 자동으로 배열의 크기를 증가시킵니다.

이 과정에서  더 큰 새로운 배열을 생성하고, 기존 배열의 요소를 새로운 배열로 복사합니다.
(새로운 배열의 크기는 기존 배열 크기의 1.5 또는 2 배)

초기 용량을 적절히 설정하면 배열의 크기를 동적으로 늘리는 작업을 줄일 수 있습니다.
배열을 늘리는 작업은 새로운 배열을 생성하고 기존 배열의 요소를 복사해야하기 때문에 비용이 많이 듭니다.

너무 크게 설정하면 메모리 공간을 낭비하게 되며
너무 작게 설정하게 되면 크기 조정 작업이 빈번하게 발생하여 오버헤드가 발생할 수 있습니다.

배열을 기반으로 하기 때문에 인덱스를 통한 직접 접근이 가능합니다.


## LinkedList
양방향 연결리스트 기반의 자료구조입니다. 
노드로 구성이 되며 배열에 비해 삽입 삭제가 유연합니다.
각 노드는 데이터 요소와 두 개의 참조(이전 노드, 다음 노드를 가리키는 포인터)로 이루어져 있습니다. 
이러한 노드들이 서로 연결되어 있어서 양방향 연결 리스트(doubly linked list) 구조를 형성합니다.


## ArrayList와 LinkedList의 요소 추가 및 삭제 성능 차이
ArrayList는 요소를 끝에 추가하는 작업이 빈번한 경우에 유리합니다.
요소를 중간에 추가하거나 삭제하는 경우 비효율적일 수 있습니다.

LinkedList는 요소를 중간에 추가하거나 삭제하는 작업이 빈번한 경우에 유리합니다.
하지만 인덱스를 기반으로 요소에 접근하는 작업에는 비효율적입니다.
특정 인덱스의 요소에 접근하려면 처음부터 해당 인덱스까지 찾아가야합니다.



##ArrayList와 LinkedList의 탐색 속도
ArrayList 는 인덱스를 기반으로 요소에 직접 접근하기 때문에 요소에 대한 빠른 접근이 가능합니다.
따라서 요소를 탐색하는데 있어 O(1)의 시간이 소요됩니다.

LinkedList 특정 인덱스의 요소에 접근하기 위해서는 처음부터 해당 인덱스까지 찾아가야 합니다. 
따라서 요소를 탐색하는 데에는 평균적으로 O(n/2)의 시간이 소요됩니다. 
최악의 경우 O(n)의 시간이 소요될 수 있습니다.

따라서 요소의 탐색이 빈번한 경우에는 ArrayList를 사용하는 것이 효율적이며
요소의 추가 및 삭제가 자주 일어나는 경우에는 LinkedList를 사용하는 것이 효율적일 수 있습니다.





