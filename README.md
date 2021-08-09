#include<stdio.h>
int ar[100];
main()
{
    int n;
    scanf("%d",&n);
    for(int i=0;i<n;i++)
        scanf("%d",&ar[i]);

    for(int i=0;i<n;i++)
    {
        for(int j=0;j<n-i-1;j++)
        {
            if(ar[j]>ar[j+1])
            {
                int temp=ar[j+1];
                ar[j+1]=ar[j];
                ar[j]=temp;
            }
        }
    }

    for(int i=0;i<n;i++)
        printf("%d ",ar[i]);

}
