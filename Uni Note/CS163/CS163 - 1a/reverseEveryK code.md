```cpp
void reverseEveryK(Node* &pHead, int k) {
	Node* tail = pHead;
	for(int t=1; t<k; t++) {
		if(!tail->pNext) return;
		tail = tail->pNext;
	}
	Node* nTail = tail->pNext;
	
	for(Node* a = pHead, *b = a->pNext; a != tail;) {
		Node* bb = b;
		if(b->pNext != nTail) bb = b->pNext;
		Node* aa = b;
		b->pNext = a;
		b = bb;
		a = aa;
	}
	
	Node* tmp = pHead;
	tmp->pNext = nTail;
	pHead = tail;
	
	if(tmp->pNext) reverseEveryK(tmp->pNext, k);
}
```