```
import java.util.ArrayList;
public class Solution {
    static boolean searchMatrix(ArrayList<ArrayList<Integer>> mat, int target) {
        // Write your code here.
        // System.out.println(mat.get(0).size());
        int m=mat.size();

        for(int i=0;i<m;i++){
            for(int j=0;j<mat.get(i).size();j++){
                if(mat.get(i).get(j)==target){
                    return true;
                }
            }
        }
        return false;
    }
}
```
![Screenshot 2023-06-06 at 8 50 34 AM](https://github.com/Kaustav96/Strivers-SDE-Sheet-Challenge/assets/17098465/84bc5bee-9d4e-44d0-8179-134398bb852f)
