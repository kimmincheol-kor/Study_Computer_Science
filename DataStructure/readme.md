# Data Structure

> #### 1. Graph
> > 정점(Vertex)과 간선(Edge)이 존재   
> > 방향성과 비방향성   
> > 그래프는 네트워크 관계를 표현하는 자료구조   
---   
> #### 2. Tree
> > 그래프의 일종.   
> > 트리는 스택이나 큐와 같은 선형 구조가 아닌 비선형 자료구조   
> > 트리는 계층적 관계(Hierarchical Relationship)을 표현하는 자료구조  
> > 
> > 트리를 구성하는 요소   
> > - Node (노드) : 트리를 구성하고 있는 각각의 요소
> > - Edge (간선) : 트리를 구성하기 위해 노드와 노드를 연결하는 선
> > - Root Node (루트 노드) : 트리 구조에서 최상위에 있는 노드
> > - Terminal Node (단말 노드) : 하위에 다른 노드가 연결되어 있지 않은 노드
> > - Internal Node (내부노드) : 단말 노드를 제외한 모든 노드 (루트 노드를 포함)
---   
> #### 3. Binary Tree
> > 부모 노드를 중심으로 두 개(왼쪽, 오른쪽)의 서브 트리로 나누어지는 트리.   
> > 트리에서 각 층을 Level 이라하고, 최고 Level의 개수를 높이라고 한다.   
> > 탐색하는 방법으로는 Preorder, Inorder, Postorder의 3가지가 존재한다.   
> >    
> > 이진 트리의 종류
> > - 완전(Complete) 이진 트리 : 위에서 아래로, 왼쪽에서 오른쪽으로 순서대로 채워진 이진 트리
> > - 포화(Full) 이진 트리 : Leaf 노드를 제외하고 모든 노드가 2개의 자식을 갖는 이진 트리
---   
> #### 4. Binary Search Tree
> > 이진 트리에서 효율적인 탐색을 위해 만들어진 이진 트리의 일종.   
> >    
> > 데이터를 저장할 때의 규칙이 존재한다.   
> > - 규칙 1. 이진 탐색 트리의 노드에 저장된 키는 유일하다.   
> > - 규칙 2. 부모의 키가 왼쪽 자식 노드의 키보다 크다.   
> > - 규칙 3. 부모의 키가 오른쪽 자식 노드의 키보다 작다.   
> > - 규칙 4. 왼쪽과 오른쪽 서브트리도 이진 탐색 트리이다.   
> >    
> > 일반적으로 탐색할때 O(log N)의 시간 복잡도를 갖지만, 최악의 경우(Skewed) O(N)의 시간 복잡도를 갖는다.   
> > 이때 Skewed Tree의 문제점을 해결하기 위해 균형을 잡기 위한 재조정을 Rebalancing이라고 한다.
---   
> #### 5. AVL Tree
> > BST에서 노드가 한쪽으로 치우치면서 생기는(Skewed) 비효율성을 해결하기 위한 균형을 유지하는(Balanced) 이진탐색트리   
> > 모든 노드에서 왼쪽 서브트리와 오른쪽 서브트리의 높이 차이가 항상 '1 이하'이도록 유지한다.   
> > 삽입 -> 조건 확인 -> **Rotation**   
> > ***항상 탐색의 시간 복잡도를 O(log N)으로 보장한다.***   
> >    
> > 참고 : https://doublesprogramming.tistory.com/237
---   
> #### 6. Red-Black Tree (RBT)
> > BST에서 노드가 한쪽으로 치우치면서 생기는(Skewed) 비효율성을 해결하기 위한 균형을 유지하는(Balanced) 이진탐색트리   
> >    
> > **RBT의 조건**   
> > 1. Root Property : 루트 노드의 색깔은 검정(Black)이다.   
> > 2. Leaf Property : 모든 Leaf node들은 검정(Black)이다.   
> > 3. No Double Red : 빨강(Red)노드의 자식은 검정(Black)이다. (빨간색 노드가 연속으로 나올 수 없다.)    
> > 4. Depth Property : 모든 Leaf node에서 Root node까지의 경로에서 Black node의 개수는 같다.   
> >    
> > **삽입 과정**
> > 1. 삽입시 Red로 삽입 후 조건 확인.
> > 2. Doubled Red일시 Uncle Node의 색깔에 따라 해결.
> >    
> > > - Uncle Node가 Black : Restructuring   
> > > - Uncle Node가 Red : Recoloring   
> >    
> > ***항상 탐색의 시간 복잡도를 O(log N)으로 보장한다.***   
> >    
> > 참고 : https://zeddios.tistory.com/237
---   
> #### 7. Hash Table
> > O(log N)보다 빠른 탐색 연산(O(1))을 위해 만들어진 자료구조.   
> > 1차원 배열과 Key값의 인덱스 관계를 이용. **Hash 함수(Key)** => 배열의 **Index** 계산 => 해당 Index에 Data 저장(Value)   
> >    
> > **충돌 Collision**   
> > 같은 Key 값에 대하여 같은 Index값이 주어지는 경우 충돌이 발생한다.   
> > > 해결 방법   
> > > 1. Closed Addressing - Chaining   
> > > 2. Open Addressing - Linear Probing   
> >    
> > 테이블에 비어있는 공간이 적을수록 효율이 떨어진다 -> 동적 해싱
> >    
> > 참고 : https://doublesprogramming.tistory.com/242?category=694779
---   
