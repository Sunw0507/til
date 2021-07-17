## ·구조체
#### 1. 노드   
```c
typedef int LData;

typedef struct _node
{
  LData data;
  struct _node* next;
} Node;
```   
#### 2. 연결 리스트 - 헤드 기반   
```c
typedef struct _linkedList
{
  Node* head;
  Node* cur;
  Node* before;
  int numOfData;
  int (*comp)(LData, LData);
} LinkedList;

typedef LinkedList Link;
```
***
참조 : [오렌지미디어](https://www.orentec.co.kr/)
