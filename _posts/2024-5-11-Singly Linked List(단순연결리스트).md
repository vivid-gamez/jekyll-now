---
layout: post
title: 단순 연결 리스트 기초구현(Singly Linked List)
---

*자료구조 스터디를 하면서 공부했던 부분 일부분 블로그로 남겨두려고 합니다.

자료구조 스터디를 시작하여 첫 시간에 진행한 내용이 바로 단순 연결리스트(Singly Linked List) 구현이다.<br>
자료구조에서 포인터를 활용한 가장 단순한 자료구조 구현이다.<br>

글로 코드를 외우기만 했지 직접 짜보기는 처음이라, 생각보다 어렵게 느껴졌다.<br>
이 포스팅에서는 단순 연결 리스트에서 <br> 
<b>새 노드 생성</b>, <b>첫 번째 노드의 위치에 삽입, 출력</b>의 세 가지 기능만 구현해보았다.<br>

![image](https://github.com/vivid-gamez/vivid-gamez.github.io/assets/103167519/1b45bb7a-133a-40e8-b528-740952fba29f)

우선 단순 연결 리스트의 구조를 구조체로 정의한 typedef structure listNode{}listNode; 코드이다.<br>
*여기서 코드에서 문제가 생길만한 점은 typedef로 정의할 때 포인터 변수에 <b>struct 키워드</b>의 유무 정도이다.<br>

typedef를 통해 listNode라는 이름으로 호출하도록 구조체를 만든다.<br>
구조체는 포인터 변수를 활용해 구조체 자기 자신을 정의하는 자기참조 구조체(Self Referential Structure) 형태이다.<br>
구조체의 구조는 정수 data, 다음 노드를 가리키기 위한 구조체 포인터 *link로 단순하게 구성되어있다.<br>

![image](https://github.com/vivid-gamez/vivid-gamez.github.io/assets/103167519/89a0bf47-6c0a-4d94-bf7c-c3bbc8df68b0)

다음으로 아무 데이터나 연결이 없는 노드 하나를 생성한 후,<br>
빈 노드를 이용하여 첫번째 위치의 노드의 데이터 필드에 int x를 삽입하는 함수인 insert_First()이다. <br>
동적할당 시 malloc() 함수가 실패할 경우의 보안대책을 위한 널값 체크를 주의한다.<br>

나중에 스택도 배우면 알게 되는데, insert_First()는 스택 구조에서 pop()의 기능과 동일하다.<br>
스택 구조는 나중에 삽입한 것이 가장 먼저 나오는 LIFO(Last-In, First-Out = 후입선출) 구조인데,<br>
메인함수를 보면 가장 마지막에 삽입한 1이 가장 먼저 출력되는 것을 확인할 수 있다.<br>

![image](https://github.com/vivid-gamez/vivid-gamez.github.io/assets/103167519/eda2cad3-1f8b-4253-bceb-8b02be9a4d63)

printLL()함수는 단순 연결 리스트의 구조를 파악하면 구현이 간단하다.<br>
첫 번째 노드를 가리키는 포인터를 설정한 후, 이제 포인터가 널값을 가리킬 때 까지 반복한다.<br>
반복문 내에는 노드의 데이터 출력을 한 후 포인터가 다음 노드를 가리키도록 p = p->link로 설정한다.<br>
이게 끝이다.<br>

오늘의 포스팅은 여기까지 입니다. :)<br> 








