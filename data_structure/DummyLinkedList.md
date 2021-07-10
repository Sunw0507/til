# dummylinkedList

## 더미 노드 기반의 다순 연결 리스트 구현1: 리스트 초기화 노드 삽입

- 다음은 연결 리스트를 표현한 구조체의 정의이다.

```c
typedef struct _linkedList
{
    Node* head;
    Node* cur;
    Node* before;
    int numOfData;
    int (*comp)(LData, LData);
} LinkedList;

```

<img src="https://blog.kakaocdn.net/dn/CWOxy/btqvNHkaWPy/VzaxxouPMMHGRHKuk2472k/img.png" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
