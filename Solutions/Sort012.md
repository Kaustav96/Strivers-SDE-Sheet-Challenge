```
import java.util.* ;
import java.io.*; 
public class Solution 
{
    public static void sort012(int[] arr)
    {
        //Write your code here
        int n = arr.length;

        int c0=0,c1=0,c2=0;

        for(int i=0;i<n;i++){
            switch(arr[i]){
                case 0:c0++;break;
                case 1:c1++;break;
                case 2:c2++;break;
            }
        }
        int i =0;
        while(c0>0){
            arr[i++]=0;
            c0--;
        }
        while(c1>0){
            arr[i++]=1;
            c1--;
        }
        while(c2>0){
            arr[i++]=2;
            c2--;
        }
    }
}
```
![Screenshot 2023-06-04 at 6 22 40 PM](https://github.com/Kaustav96/Strivers-SDE-Sheet-Challenge/assets/17098465/4bfef708-f724-4415-9fd7-82c3c0b8ff7b)
