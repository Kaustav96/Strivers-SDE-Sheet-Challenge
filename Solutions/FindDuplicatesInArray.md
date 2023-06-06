<b>Find element repeating twice</b>
```
import java.io.*;
import java.util.* ;

import java.util.ArrayList;

public class Solution{
    public static int findDuplicate(ArrayList<Integer> arr, int n){
        // Write your code here.
        int[] count = new int[n];

        for(int i = 0;i<n;i++){
            count[arr.get(i)-1]++;
        }

        for(int i=0;i<n;i++){
            if(count[i]>1){
                return i+1;
            }
        }
        return -1;
    }
}
```
![Screenshot 2023-06-06 at 8 33 48 AM](https://github.com/Kaustav96/Strivers-SDE-Sheet-Challenge/assets/17098465/0f995819-ada8-4e9b-9dfe-4657905a0b78)
