//Queue using array
#include<iostream>
using namespace std;

class Queue{
    int Size;
    int addCount = -1;
    int* arr = new int[Size];

public:
    Queue(int x)
    {
        Size = x;
    }

    //add an element to last
    void adda(int value)
    {
        if(addCount < Size-1)
        {
            addCount++;
            arr[addCount]=value;

        }
        else
        {
            cout<<"Storage full"<<endl;
            addCount = Size-1;
        }
    }
    //delete an element from first
    void del()
    {
        if(addCount > -1)
        {
            for(int i=1; i < Size ; i++)
            {
                arr[i-1] = arr[i];
            }
            addCount--;

        }
        else{ cout<<"Storage empty"<<endl; addCount = -1;}
    }
    //display the queue
    void disp()
    {
        for(int i = 0; i <= addCount ; i++)
        {
            cout<<arr[i]<<"\t";
        }
        cout<<endl;
    }

};

int main()
{
/*
Functions to play the queue
1. add en element to the queue ---> class_object.adda(above_element);
2. remove en element from the queue ---> class_object.del();
3. display the queue ---> class_object.adda(above_element);
*/
    Queue q1(10);

}
