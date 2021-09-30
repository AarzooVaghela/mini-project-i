#include<stdio.h>
int main(){
int p[5000]={0},q[5000]={0},r[5000]={0};
 p[0]=0,q[0]=1;
int lp=1,lq=1,lr=1;
int n,i,k,j,t,x,y,carry=0;
printf("Enter the number for finding nth fibonacci number\n");
scanf("%d",&n);
if(n==1){
    printf("0");
}
else if(n==2){
    printf("1");
}
else{
for(y=0;y<n-2;y++){
    
    lp=lq;lq=lr;t=lq-lp-1;
    int l=lq,m=lp;
    if(lq>lp){
        for(i=lq;i>=0;i--){
          p[i+1]=p[i];
        }
        p[0]=0;
    }
   
    

    for(x=lq-1;x>=0;x--){
              int sum=0;
             sum =(p[x]+q[x]+carry);
             if(sum>9){
                 carry=1;
                 r[x]=sum%10;
             }
             if(sum<=9){
                 carry=0;r[x]=sum;
             }
             if(x==0&&carry==1){
                 lr=lq+1;
              for(i=lq;i>=1;i--){
                  r[i]=r[i-1];
              }
              r[0]=1;}
              }carry=0;

              for(j=0;j<lq;j++){
              p[j]=q[j];
              }
              for(k=0;k<r;k++){
                 q[k]=r[k];
              }

              }
              for(i=0;i<lr;i++){
             printf("%d",r[i]);
             }}
          
          return 0;

          }
