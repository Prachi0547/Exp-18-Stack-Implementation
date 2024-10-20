# Exp-18-Stack-Implementation
# Aim
To study and implement stack implementation using array.
# Problem Statement
Write a c++ program to do stack implementation.
# Theory
A stack is a linear data structure that follows the Last In, First Out (LIFO) principle, meaning that the last element added to the stack is the first one to be removed. Stacks are used in various applications, such as function call management, expression evaluation, and backtracking algorithms.

The Basic Operations are:
Push (Adds an element to the top of the stack.) ,
Pop (Removes the element from the top of the stack.) ,
Peek/Top (Retrieves the element at the top of the stack without removing it.) ,
IsEmpty (Checks whether the stack is empty.)

# Program Code
```
//Stack Implementation

#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Stack{
    int top, ar[size];
    public:
    Stack()
    {
        top=-1;
        ar[0]=0;
    }
    void push(int);
    int pop();
    int peak();
    void disp();
};
void Stack::push(int num)
{
    if (top==size-1)
    {
        cout<<"STACK OVERFLOW: Stack is full"<<endl;
        return;
    }
    else
    {
        ar[++top]=num;
    }
}
int Stack::pop()
{
    int val;
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: STACK IS EMPTY"<<endl;
        return ERROR;
    }
    else{
         val=ar[top--];
         return val;
    }
}
int Stack::peak()
{
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ERROR;
    }
    else
    {
        return ar[top];
    }
}
void Stack::disp()
{
    if(top==-1)
    {
       cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ;
    }
    else
    {
        int i=0;
        while(i!=(top+1))
        {
            cout<<ar[i]<<"  ";
            i++;
        }
    }
}
int main()
{
    Stack s1;
    s1.push(7);
    s1.push(10);
    s1.push(4);
    int val=s1.pop();
    cout<<val;
    int top=s1.peak();
    cout<<top;
    s1.disp();
    return 0;
}
```
# Output
![image](https://github.com/user-attachments/assets/2a0e82d0-c621-45c1-ab56-c80dc1e4bebb)

# Conclusion
We learnt how to do stack in c++.
