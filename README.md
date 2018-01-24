# HighandLow
include<iostream>
using namespace std;
int smallest(int[],int);
int largest(int[],int);
/* 
  Input:  i is counter variable, n is the number of elements, si is smallest number index, li is largest number index
  Processing:
    1. Taken the number of elements of the array
    2. Takes the n elements into array one by one from the keyboard
    3. Displays the array elements
    4.Function call to smallest(), the arguments are array's base address and number of elements n
    5. same as 4 but with largest()
  
  Output: give min and max with first and last occurance
  Testing: number of elements:3 
  array elements: 3 1 2
  results: minimum=1 index of the smallest=1 
    maximum = 3 index of last = 0
*/
int main(){
   int array[20],i,n,si,li; 
   cout<<"Enter the number of elements to be entered into the array:";
   cin>>n; 
   cout<<"Enter the array elements one by one\n";
   for(i=0;i<n;i++)
   cin>>array[i]; 
   cout<<"The elements of the array are\n";
   for(i=0;i<n;i++)
   cout<<array[i]<<" ";
   si=smallest(array,n);
   cout<<"\nThe index of the first occurrence of the smallest element of the array is:"<<si;
   li=largest(array,n);
cout<<"\nThe index of the last occurrence of the largest element of the array is:"<<li;
   return 0;
}
/*smallest
  input: array and n
  Processing:
    1. Treat the first element as minimum
    2. compare each element and replace if it smaller
    3. Displays the array elements
    4.Function call to smallest(), the arguments are array's base address and number of elements n
    5. same as 4 but with largest()
  
  Output: brings all the seperate ones into "one" with the main
  Testing: number of elements:3 
  array elements: 3 1 2
  results: minimum=1 index of the smallest=1 
    maximum = 3 index of last = 0*/
int smallest(int array[],int n){
   int i,min;
   min=array[0]; 
   for(i=1;i<n;i++) {
       if(array[i]<min) {
         min=array[i];
       }
   }
   cout<<"\nThe minimum element of the array:"<<min; 
   for(i=0;i<n;i++){
       if(array[i]==min) 
       break; 
   }
return i;
}
int largest(int array[],int n)
{
   int i,max,index;
   max=array[0]; 
   for(i=1;i<n;i++) {
       if(array[i]>max) {
           max=array[i];
       }
   }
   cout<<"\nThe Maximum element of the array is:"<<max; 
   for(i=0;i<n;i++){
       if(array[i]==max) {
           index=i;
       }
   }
return index;
}
