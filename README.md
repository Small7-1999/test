#include<stdio.h>
int main(void)
{
    int num,a[1010],b[1010],i;
    scanf("%d",&num);
    for(i=0;i<num;i++)
    {
        scanf("%d",&a[i]);
        b[i]=a[i];
    }
    a[0]=(b[0]+b[1])/2;
    for(i=1;i<num-1;i++)
        a[i]=(b[i-1]+b[i]+b[i+1])/3;
    a[num-1]=(b[num-2]+b[num-1])/2;
    for(i=0;i<num-1;i++)
        printf("%d ",a[i]);
    printf("%d\n",a[num-1]);
    return 0;
}
