# -
学习中的代码
#include <stdio.h>
#include <stdlib.h>
//将任意一个数倒序输出

int main()
{
    int a,j=0,x,i=1,wei=1,sum=0;//j记录这是个几位数，x是用于保存各种数的工具人，wei是位权
    scanf("%d",&a);
    x=a;
    while(x>0)
    {
        x=x/10;
        j++;//这个while用来记录是几位数
    }
    while(a>0)
    {
        x=a%10;//x保存最后一位数
        for(i=1; i<=j-1; i++)
        {
            wei=wei*10;
        }
        sum=sum+x*wei;
        j--;
        wei=1;
        a=a/10;//清除最后一位数

    }
    printf("%d",sum);
}
