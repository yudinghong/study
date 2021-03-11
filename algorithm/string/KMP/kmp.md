# <center>KMP</center>

```c
void getNext(char str[], int len, int *next){
  next[0] = -1;
  int i = 0;
  int j = -1;
  while(i < len){
    if (j == -1 || str[i] == str[j]){
      next[++i] = ++j;  
    }
    else{
      j = next[j];
    }
  }
}
```
