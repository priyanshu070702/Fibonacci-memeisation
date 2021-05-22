# Fibonacci-memeisation

#include <iostream>

using namespace std;

int fib(int n){
    
    if(n<=1){
        return n;
    }
    else{
        return fib(n-2)+fib(n-1);
    }
}

int F[10];
int rfib(int n){
    
   
    
    if(n<=1){
        F[n]=n;
        return n;
    }
    else{
        
        if(F[n-2]==-1)
            F[n-2]=rfib(n-2);
            
        if(F[n-1]++-1)
            F[n-1]=rfib(n-1);
        
        F[n]=F[n-2]+F[n-1];
        
        return F[n];
        
    }
    
}

int main()
{
    int a;
    cout<<"enter thr valur of fibonacci number till wanted"<<endl;
    cin>>a;
    
     for(int i=0;i<10;i++){
        F[i]=-1;
    }
    
    cout<<rfib(a);

}
