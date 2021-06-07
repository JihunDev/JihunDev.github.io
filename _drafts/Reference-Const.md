# C - const

## Const

- Const 값은 절대로 바꿀수 없음
- 처음 상수를 정의 할때 값을 지정해야함



```c
const (자료형) (상수명) = (상수 값);
```



만약 상수 값을 변경할시에 <u>Assignment of read-only Variable '상수명'</u> 에러 메세지가 나오며 읽기 전용 변수 접근 했다고 하며 상수로 정의된 값을 변경 할수없다는 것이다.



## pointer Const

```c
int a = 10;
int b = 20;
const int* c = &a;

*c = 100; //err
c = &b;
```

- c는 상수만을 가르키는 포인터
- c가 가리키는 대상은 변경이 가능하지만, 가리키는 값을 변경 할 수 없음



```c
int a = 10;
int b = 20;
int* const c = &a;

*c = 100;
c = &b; //err
```

- c는 정수변수를 가리키는 상수형 포인터
- 포인터가 가리키는 위치를 변경 할 수 없고, 가리키는 값은 변경 가능함