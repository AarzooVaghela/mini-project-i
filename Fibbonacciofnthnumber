#include<stdio.h>
int main(){
int p[4500]={0},q[4500]={0},r[4500]={0};
 p[0]=0,q[0]=1;
int sp=1,sq=1,sr=1;
int n,i,x,j,b,d,carry=0;
 printf("Enter the number n for finding nth fibonacci number\n");
scanf("%d",&n);
if(n==1){
    printf("0");
}
else if(n==2){
    printf("1");
}
else{
d=0;
 while(d<n-2){
    
    sp=sq;sq=sr;
    int s=sq,m=sp;
    if(sq>sp){
        for(i=sp;i>=0;i--){
          p[i+1]=p[i];
        }
        p[0]=0;
        d=d+1;
    }
     for(b=sq-1;b>=0;b--){
              int sum=0;
             sum =(p[b]+q[b]+carry);
             if(sum>9){
                 carry=1;
                 r[b]=sum%10;
             }
             if(sum<=9){
                 carry=0;r[b]=sum;
             }
             if(b==0&&carry==1){
                 sr=sq+1;
              for(i=sq;i>=1;i--){
                  r[i]=r[i-1];
              }
              r[0]=1;}
              }carry=0;

              for(j=0;j<sq;j++){
              p[j]=q[j];
              }
              for(x=0;x<sr;x++){
                 q[x]=r[x];
              }

              }
              for(i=0;i<sr;i++){
             printf("%d",r[i]);
      }
 }
          
 return 0;

 }
