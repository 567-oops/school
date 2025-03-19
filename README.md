#include <iostream>
using namespace std;
void inputarray(int arr[],int size)
{
    for(int i=0;i<size;i++){
        cin>>arr[i];
    }
}
void displayarray(int arr[],int size)
{
    for(int i=0;i<size-1;i++){
        cout<<arr[i]<<", ";
    }
    cout<<arr[size-1]<<endl;
}
void BubbleSort(int arr[],int size,int direction)
{
    for(int i=0;i<size;i++)
    {
        if(i!=size-1){
         cout<<"這是第"<<i+1<<"次排列";
    }
        cout<<endl;
        for(int j=0;j<size-1-i;j++){
            if(direction==1&&arr[j]>arr[j+1]||direction==0&&arr[j]<arr[j+1]){
                int temp=0;
                temp=arr[j];
                arr[j]=arr[j+1];
                arr[j+1]=temp;
            }
            displayarray(arr,size);
            }
        }

    }

int main(){
    int size;
    int direction;
    cout<<"總共有多少數字:";
    cin>>size;
    int arr[size];
    cout<<"輸入陣列中數字，並用空格隔開:";
    inputarray(arr,size);
    cout<<"要從小到大排序嗎?(1代表小到大/0代表大到小):";
    cin>>direction;
    BubbleSort(arr,size,direction);
    cout<<"排列完的數據為:";
    displayarray(arr,size);
    return 0;

}

