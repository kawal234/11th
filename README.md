# 11th
#include<iostream>
#include<algorithm>
#include<vector>
using namespace std;

//Q1. to find the total no.of pairs in array whose sum is equal to a given number

// int main(){
//     int arr[] = {3,4,6,7,1};
//     int sum = 7;
//     int pairs=0;
//     int size=5;
//     for(int i=0;i<size;i++){
//         for(int j=i+1;j<size;j++){
//             if(arr[i]+arr[j]==sum){
//                 pairs++;
//             }
//         }
//     }
//     cout<<"No.of pairs in the array is : "<<pairs<<endl;
//     return 0;
// }


//Q2. Same Of the above question but now we need to add triplets and get the sum

// int main(){
//     int arr[] = {3,1,4,2,6,7,0};// (1,4,0)
//     int sum = 7;
//     int pairs=0;
//     int size=5;
//     for(int i=0;i<size;i++){
//         for(int j=i+1;j<size;j++){
//             for(int k=j+1;k<size;k++){
//                 if(arr[i]+arr[j]+arr[k]==sum){
//                 pairs++;
//             }
            
//             }
//         }
//     }
//     cout<<"No.of pairs in the array is : "<<pairs<<endl;
//     return 0;
// }


//Q3. find the unique number in a given Array where all the elements are being repeated twice with one value being unique

// int main(){
//     int arr[] = {1,2,3,1,3,2,4,4,5,6,5};
//     int size = 11;
//     for(int i=0;i<size;i++){
//         for(int j=i+1;j<size;j++){
//             if(arr[i]==arr[j]){
//                 arr[i]=arr[j]=-1;
//             }
//         }
//     }
//     for(int i=0;i<size;i++){
//         if(arr[i]>0){
//             cout<<arr[i]<<endl;
//         }
//     }
//     return 0;
// }


//Q4. Find the second largest Number

// int largest(int arr[],int size){// this is the function that performs the operation as the question required
//     int max=INT8_MIN;
//     int max_Index=-1;
//     for(int i=0;i<size;i++){
//         if(arr[i]>max){
//             max=arr[i];
//             max_Index=i;
//         }
//     }
//     return max_Index;
// }
// int main(){
//     int arr[]={2,3,5,7,6,1,7};
//     int n=7;
//     int large = largest(arr,6);
//     cout<<"The first largest element is : "<<arr[large]<<endl;
//     // arr[large] = -1;

//     int largest_el = arr[large];
//     for(int i=0;i<n;i++){
//         if(arr[i]==largest_el){
//             arr[i]=-1;
//         }
//     }
//     int second_largest=largest(arr,6);
//     cout<<"The second largest element is : "<<arr[second_largest]<<endl;
//     return 0;
// }

//Q5. rotate the given array 'a' by k steps where k is non-negative.
//NOTE: k can be greater than n also


// int main(){
//     int arr[]={1,2,3,4,5};
//     int n = 5;
//     int k=3;
//     // for k can be greater than n
//     k=k%n;
//     int ans_Arr[5];
//     int j=0;
//     // this is for inserting last k elements in ans_Arr
//     for(int i=n-k;i<n;i++){
//         ans_Arr[j++] = arr[i];
//     }
//     // Inserting first n-k elements in ans_Arr
//     for(int i=0;i<=k;i++){
//         ans_Arr[j++] = arr[i];
//     }
//     for(int i=0;i<n;i++){
//         cout<<ans_Arr[i]<<" ";
//     }
//     cout<<endl;
//     return 0;
// }

// Doing the above problem in a different manner by vectors 

int main(){
    vector<int> v;// initialization of vector
    v.push_back(1);
    v.push_back(2);
    v.push_back(3);
    v.push_back(4);
    v.push_back(5);
    int k=2;
    k=k%v.size();

    reverse(v.begin(),v.end());
    reverse(v.begin(),v.begin()+k);
    reverse(v.begin()+k,v.end());

    for(int a:v){
        cout<<a<<" ";
    }cout<<endl;
    return 0;
}




