#include <iostream>

using namespace std;


int partition(int arr[],int s,int e)
{
    //taaking first element as pivot
    int pivot=arr[s];
    
     //count smaller elements
    int count=0;
    for(int i=s+1;i<=e;i++)
    {
        if(arr[i]<=pivot)
        count++;
    }
    
    //find right place for pivot
    int pivotindex=s+count;
    
    //swap
    swap(arr[pivotindex],arr[s]);
    
    //handel left and right
    
    //we want all lesser element on left side
    //and greater element on right side of pivotindex
    
    int i=s,j=e;
    while(i<pivotindex && j>pivotindex)
    {
    //already smaller element in left side
    
    while(arr[i]<=pivot)
    {
        i++;
    }
    
     //already smaller element in right side
     
     while(arr[j]>pivot)
     {
         j--;
     }
    
    if(i<pivotindex and j>pivotindex)
    {
        swap(arr[i],arr[j]);
        i++;
        j--; 
    }
    
    }
    return pivotindex;
}

void quicksort(int arr[], int s ,int e)
{
    //base case
    
    if(s>=e)
    return ;
    
    int pindex=partition(arr,s,e);
    
    //left
    quicksort(arr,s,pindex-1);
    
    //right
    quicksort(arr,pindex+1,e);
    
    
    
}


int main()
{
    
    int size;
    cin>>size;
    
    int arr[size];
    
   
    for(int i=0;i<size;i++)
    {
        cin>>arr[i];
    }
    
    quicksort(arr,0,size-1);
    
     for(int i=0;i<size;i++)
    {
        cout<<arr[i]<<" ";
    }
    cout<<endl;
    

    return 0;
}

eg:-
input size =4
input array= 3 2 7 5
output array= 2 3 5 7 
