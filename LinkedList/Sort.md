### ·정렬 구현   
#### 1. 새로운 입력된 데이터의 노드 연결   
```c
void SetSoortRule(List* plist, int (*comp)(LData, LData))
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
#### 3. 노드 끼워넣기를 통한 정렬
```c
void SInsert(List* plist, LData data)
{
  Node* newNode = (Node*_malloc(sizeof(Node));
  Node* pred = plist->head;
  newNode->data = data;
  
  while(pred->next != NULL && plist->comp(data, pred->next->data) != 0) //data가 pred->next->data보다 작지 않을 경우 실행(반복)
  {
    pred = pred->next; //다음 노드로 이동
  }
  
  newNode->next = pred->next;
  pred->next = newNode;
  
  (plist->numOfData)++;
}
```
<img src="https://blog.kakaocdn.net/dn/VYQ1Z/btqvP6cD5DZ/vGTe2nBVTkI9pKpyZbQkV0/img.png" width="68%" height="68%" title="SInsert 함수의 노드 추가 완료" alt="LinkedList 04-33"></img>
***
참조 : [오렌지미디어](https://www.orentec.co.kr/)
