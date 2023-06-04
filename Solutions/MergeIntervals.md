```
import java.util.* ;
import java.io.*; 
/*******************************************************

    Following is the Interval class structure

    class Interval {
        int start, int finish;

        Interval(int start, int finish) {
            this.start = start;
            this.finish = finish;
        }
    }
    
*******************************************************/

import java.util.List;


import java.util.*;

public class Solution {
    public static List<Interval> mergeIntervals(Interval[] intervals) {
        // write your code here.
        if (intervals.length <= 0)
            return new ArrayList<>();
   
        Stack<Interval> stk=new Stack<>();
   
        // sort the intervals in increasing order of start time
        Arrays.sort(intervals,new Comparator<Interval>(){
            public int compare(Interval i1,Interval i2)
            {
                return i1.start-i2.start;
            }
        });

        stk.add(intervals[0]);

        for(int i=1;i<intervals.length;i++){
            Interval top = stk.peek();
            if(top.finish<intervals[i].start){
                stk.push(intervals[i]);
            }
            else if(top.finish<intervals[i].finish){
                top.finish = intervals[i].finish;
                stk.pop();
                stk.push(top);
            }
        }
        if(stk.isEmpty()){
            return new ArrayList<>();
        }
        List<Interval> ans = new ArrayList<>();
        while(!stk.isEmpty()){
            ans.add(0,stk.peek());
            stk.pop();
        }
        return ans;
    }
}
```
![Screenshot 2023-06-04 at 6 37 57 PM](https://github.com/Kaustav96/Strivers-SDE-Sheet-Challenge/assets/17098465/3f185271-2219-4220-9f1d-1b4b63d2f7c1)
