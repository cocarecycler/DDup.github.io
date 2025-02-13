# day2 数组2 209，59，区间和
209滑动窗口
超时的暴力解...
```C
class Solution {
public:
    int minSubArrayLen(int target, vector<int>& nums) {
        int i,j,min,l,flag;//i是快指针，j是慢指针，min是最小长度,l是当前长度
        int n = nums.size();
        l=i=j=0;
        min=1000000;
        flag=1;
        int sum=0;
        for(i;i<n;i++)
        {
            j=i;l=0;sum=0;
            while(sum<target&&j<n)
            {
                sum+=nums[j];
                j++;
                l++;
            }
            if(j=n&&sum<target)
                l=0;
            if(l>=0&&l<min&&sum>=target)
            {
                min=l;
                flag=0;
            }
                

        }
        if(flag)return 0;
        return min;
    }
};
```