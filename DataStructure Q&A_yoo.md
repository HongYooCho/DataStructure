## 1. One pass로 링크드리스트 middle point 찝어내기
- 보통의 경우 currentNode->next가 null일때까지 탐색 하여 linkedlist의 길이를 구하고, 그 길이의 절반을 찾아 middle point를 찝어낸다. -> 2pass
- 1 pass로 끝내는 법
* 2개의 포인터를 사용하자
1. currentNode와 middleNode라는 두개의 포인터가 있다고 가정
2. currentNode는 똑같이 한 노드씩 탐색 후 length++
3. middleNode는 length가 짝수 일때만 다음 노드로 이동.
즉 middleNode는 currentNode가 탐색하는 것의 절반만큼만 이동하므로 middle point를 찝어낼 수 있다.
<br>그리고 길이가 홀수인 경우 middleNode를 한번더 다음으로 이동하면서 정중앙을 찝어낼 수 있다.
`while(currentNode->next!=null){
	length++;
	If(legnth%2==0)
	  middleNode=middleNode->next;
 	currentNode=currentNode->next;
}
if(length%2!=0)
   middleNode=middleNode->next;`
