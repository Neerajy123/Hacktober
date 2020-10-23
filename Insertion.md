#include<stdio.h>
int main()
{
int n,i,j,temp;
printf("enter the size of array: ");
scanf("%d",&n);
int a[n];
printf("\n elements of array:\n");
for(i=0;i<n;i++)
{
scanf("%d",&a[i]);
}
for(i=1;i<n;i++)
{
temp = a[i];
j = i-1;
while(j>=0 && a[j]>temp)

{
a[j+1] = a[j];
j--;
}
a[j+1] = temp;
}
printf(" Inserted sorted array is : ");
for(i=0;i<n;i++)
{
printf("%d\t",a[i]);
}
return 0;
}
