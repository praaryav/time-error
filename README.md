#include<stdio.h>
int main()
{
 int T,N,A[100],i,j,et,h;
 jump:
 scanf("%d",&T);
 if(T<1||T>100)
 {
  goto jump;
 }
 for(i=0;i<T;i++)
 {
  jump1:
  scanf("%d",&N);
  if(N<7||N>100)
  {
   goto jump1;
  }
  for(j=0;j<N;j++)
  {
   scanf("%d",&A[j]);
  }
 }  
 et=N%2;
 if(et==0)
 {
  h=N/2;
  for(i=1;i<=(N/2);i++)
  {
   if(A[h-i]!=A[N+i-h])
   {
    printf("no");
    break;
   } 
  }
  printf("yes");
 } 
 if(et!=0)
 {
  h=(N/2)+1;
  for(i=1;i<=(N/2);i++)
  {
   if(A[h-i-1]!=A[N+i-h])
   {
    printf("no");
    break;
   } 
  }
  printf("yes");
 }
 return 0;
}    
