# assignment-1
1.
#include<stdio.h>
#include<string.h>
int isvalid(char a[])
{
    int at_count =0;
    int dot_count=0;
    int l = strlen(a);
    if(l>320){
        return 0;
    }
    if(!((a[0]>='a' && a[0]<='z') ||(a[0]>='A' && a[0]<='Z') ))
            {
                return 0;
            }
    for(int i=0;i<l;i++)
    {
        if(a[i]=='@')
        {
            at_count++;
            if(at_count>1){
                return 0;
            }
             if(!((a[i+1]>='a' && a[i+1]<='z') ||(a[i+1]>='A' && a[i+1]<='Z') ))
            {
                return 0;
            }
        }
        if(a[i]=='.')
        {
            dot_count++;
            if(!((a[i+1]>='a' && a[i+1]<='z') ||(a[i+1]>='A' && a[i+1]<='Z') ))
            {
                return 0;
            }
        }
    }
    if(at_count==0)
    {
        return 0;
    }
    if(dot_count==0)
    {
        return 0;
    }

return 1;
}

int main()
{   
    char email[300];
    printf("Enter your E-mail\n");
    scanf("%s",email);

    if(isvalid(email)){
        printf("Email is Valid\n");
    }
    else{
        printf("Email is Invalid\n");
    }
    return 0;
}
3. no problem
4. #include<stdlib.h>
#include<stdio.h>
struct matrix 
{
    int *a;
    int n;
};
void set(struct matrix *m,int i,int j,int val){
    m->a[i*m->n+j]=val;
}
void disp(struct matrix m){
    for(int i=0;i<m.n;i++){
        for(int j=0;j<m.n;j++)
        printf("%d ",m.a[i*m.n+j]);
        printf("\n");
    }
    printf("\n");
}
int main()
{
    struct matrix m;
    printf("enter the size of matrix\n");
    scanf("%d",&m.n);
    int size=m.n;
    m.a=(int*)malloc(size*size*sizeof(int));
    for(int i=0;i<size;i++){
        for(int j=0;j<size;j++){
            int val;
            scanf("%d",&val);
            set(&m,i,j,val);
        }
    }
    disp(m);
}
4 no problem
![image](https://user-images.githubusercontent.com/91239309/136700208-e18b1eef-a2b1-4e45-9026-6064e9365d88.png)
