# insertion-sort
#include<stdio.h>
#include<conio.h>
void main()
{
    int arr[30],i,n;
    void insertionsort(int[],int);
    printf("\nEnter no of elements:");
    scanf("%d",&n);
    printf("\nEnter %d value",n);
    for(i=0;i<n;i++)
        scanf("%d",&arr[i]);
    printf("\nBefore sorting elements are:");
    for(i=0;i<n;i++)
        printf("%d ",arr[i]);
    insertionsort(arr,n);
    printf("\nAfter sorting elements are:");
    for(i=0;i<n;i++)
        printf("%d ",arr[i]);
}
void insertionsort (int arr[],int n)
{
    int i,j,key;
    for(i=1;i<n;i++)
    {
        key=arr[i];
        j=i-1;
        while(j>=0 && arr[j]>key)
        {
            arr[j+1]=arr[j];
            j=j-1;
        }
        arr[j+1]=key;
    }
}
