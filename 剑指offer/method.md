
**JZ11 旋转数组的最小数字**  //  logn



**JZ12 矩阵中的路径**       //  非常好的题。可以从任意一个点出发。


**JZ13 机器人的运动范围**   // 回溯


**JZ14 剪绳子**      // dp

**JZ15 二进制中1的个数**  // 这题考察 位运算。 & 是补码之间的操作。 << 也是补码的位移。

**快排求topk**  
```
class Solution {
    public boolean sort1(int[] nums, int left, int right, int target) {
        if (left >= right)
            return false;
        int pivotIndex = patition(nums, left, right); // left<right

        if (pivotIndex == target - 1)  //
            return true;
        if (pivotIndex > target - 1) {
            if (sort1(nums, left, pivotIndex - 1, target))
                return true;
        } else {
            if (sort1(nums, pivotIndex + 1, right, target))
                return true;
        }
        return false;
    }

    public int patition(int[] nums, int left, int right) {
        int pivot = nums[left];
        int start = left;
        int end = right;
        while (left < right) {
            while (nums[left] <= pivot && left < end) {
                left++;
            }
            while (pivot <= nums[right] && start < right) {  //nums[left]>pivot 。
                right--;
            }
            if (left >= right) break;
            else {
                int temp = nums[left];
                nums[left] = nums[right];
                nums[right] = temp;
            }
        }
        int temp = nums[start];
        nums[start] = nums[right];
        nums[right] = temp;
        return right;
    }
} 
```


