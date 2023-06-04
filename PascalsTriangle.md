```
import java.io.*;
import java.util.* ;

import java.util.ArrayList;

public class Solution {
	public static ArrayList<ArrayList<Long>> printPascal(int n) {
        // Write your code here.
		ArrayList<ArrayList<Long>> ans = new ArrayList<>();
		if(n==0) return ans;

		ans.add(new ArrayList<>());
		ans.get(0).add(1L);

		for(int i=1;i<n;i++){
			ArrayList<Long> row = new ArrayList<>();
			ArrayList<Long> prev = ans.get(i-1);
			row.add(1L);
			for(int j=1;j<i;j++){
				row.add(prev.get(j-1)+prev.get(j));
			}
			row.add(1L);
			ans.add(row);
		}
		return ans;
	}
}
```

![image](https://github.com/Kaustav96/Strivers-SDE-Sheet-Challenge/assets/17098465/4780842f-2e48-4704-9501-c14bcc804352)
