# 연결 리스트 구현
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
#### 2. 연결리스트 - 헤드 기반   
```c
typedef struct _linkedList
{
  Node* head;
  Node* cur;
  Node* before;
  int numOfData;
  int (*comp)(data1, data2);
} LinkedList;

typedef LinkedList Link;
```
***
### -정렬 구현   
#### 1. 새로운 입력된 데이터의 노드 연결   
```c
void SetSoortRule(List* plist, int (*comp)(LData data1, LData data2))
{
  plist->comp = comp;
}
```  
#### 2. 정렬 함수 정의 및 지정   
```c
int WhoIsPrecede(int d1, int d2)
{
  if(d1 < d2)
    return 0;
  return 1;
}

int main(void)
{
  List list;
  //···
  SetSortRule(&list, WhoIsPrecede);
  //···
}
```

참조 : [오렌지미디어](https://www.orentec.co.kr/)
