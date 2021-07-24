# Contains Duplicate

Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

### Example:

**_Input:_** `nums = [1,2,3,1]`

**_Output:_** `true`

### Constraints:

`1 <= nums.length <= 10^5`

`-10^9 <= nums[i] <= 10^9`

## Solution in JavaScript

```
var containsDuplicate = function(nums) {
    let contains = false;

    for (let i = 0; i < nums.length; i++) {
        for (let j = 0; j < nums.length; j++) {
            if (i !== j && nums[i] === nums[j]) {
                contains = true;
                break;
            }
        }
    }
    return contains;
};
```
