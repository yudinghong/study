# Sort

## Bubble Sort

```c
void bubbleSort(int a[], int size){
  int i = 0;
  int j = 0;
  for(; i < size; i++){
    for(j = 0; j < size - i - 1; j++){
      if (a[j] > a[j+1]){
        swap(a[j], a[j+1]);
      }
    }
  }
}
```

## Insert Sort

```c
void insertSort(int arr[5], int len) {
  for(int i = 1; i < len; i++){
    for(int j = i; j > 0; j--){
      if (arr[j] < arr[j-1]){
        swap(arr[j], arr[j-1]);
      }
      else {
        break;
      }
    }
  }
}
```

## Quick Sort

```c
int Partition(int a[],int p,int r){
  int i=p,j=r+1;
  int x=a[p];
  int tramp;
  while(true){
    while(a[++i]<x&&i<r);
    while(a[--j]>x);
    if(i>=j) break;
    tramp=a[i];
    a[i]=a[j];
    a[j]=tramp;
  }
  a[p]=a[j];
  a[j]=x;
  return j;
}

void QuickSort(int a[],int p,int r){
  if(p < r){
    int q=Partition(a,p,r);
    QuickSort(a,p,q-1);
    QuickSort(a,q+1,r);
  }
}
```

## Select Sort

```c
void selectSort(int a[], int size) {
  
  int i = 0;
  int j = 0;
  for(i=0; i < size; i++){
    int maxIndex = 0;
    for(j = 1; j < size-i; j++){
      if (a[j] > a[maxIndex]){
        maxIndex = j;
      }
    }
    swap(a[maxIndex], a[size - i - 1]);
  }
}
```

## Shell Sort

```c
void shellSort(int *arr, int len){
  int step = len / 2;
  int index = 0;
  int swapTemp = 0;
  int j = 0;
  for(; step > 0; step/=2){
    for(index = 0; index + step < len; index++){
      int tempMin = *(arr+index);
      int tempMinIndex = index;
      for(j = index; j < len; j += step){
        if (*(arr+j) < tempMin){
          tempMin = *(arr+j);
          tempMinIndex = j;
        }
      }
      swapTemp = *(arr+index);
      *(arr+index) = *(arr+tempMinIndex);
      *(arr+tempMinIndex) = swapTemp;
    }
  }
}
```

<!-- ## 

```c
``` -->
