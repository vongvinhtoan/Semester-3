```cpp 
// Binary Search
int findX(int* a, int n, int x)
{
	int l=0, r=n-1;
	while(l<=r) {
		m = (l+r) / 2;
		if(a[m] < x) l = m + 1;
		else r = m;
	}

	if(a[l] != x) return -1;
	return l;
}
```

```cpp
// Binary lifting
int findX(int* a, int n, int x)
{
	int ans = 0;
	for(int i = 32 - countl_zero(n); i >= 0; i--) {
		if(ans + (1 << i) >= n) continue;
		ans ^= 1<<i;
		if(a[ans] >= x) ans ^= 1<<i;
	}
	
	while(a[ans] < x) ans++;
	if(a[ans] == x) return ans;
	else return -1;    
}
```
