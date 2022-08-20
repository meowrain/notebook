# C语言-获取最大最小值函数

```c
#include <stdio.h>

void minmax(const int a[],int len,int *max, int *min);
int main(void) {
    int a[] = {1,2,3,4,5,25,7,8,9,10,11,12,13};
    int min,max;
    minmax(a,sizeof(a)/sizeof(a[0]),&max,&min);
    printf("min:%d,max:%d\n",min,max);
    return 0;
}
void minmax(const int a[], int len, int *max, int *min) {
    int i;
    *max = a[0];
    *min = a[0];
    for (i = 1; i < len; ++i) {
        if(*min>a[i]) {
            *min = a[i];
        }
        if(*max<a[i]) {
            *max = a[i];
        }
    }
}

```

> ![image-20220814204732981](https://static.meowrain.cn/i/2022/08/14/xuxbtr-3.png)