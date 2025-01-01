# LeetCode Top 150 - My JavaScript Solutions 💻

A personal collection of my solutions to LeetCode's Top 150 Interview Questions. This is a passion project where I document my problem-solving journey as I work through these challenges.

## Solution Structure 📁

Each solution includes my implementation

```javascript
/**
 * Merge Sorted Array (Problem 88)
 * @param {number[]} nums1 - First array with extra space
 * @param {number} m - Number of elements in nums1
 * @param {number[]} nums2 - Second array to merge
 * @param {number} n - Number of elements in nums2
 */
var merge = function(nums1, m, nums2, n) {
    let i = m - 1, j = n - 1, k = m + n - 1;
    
    while(i >= 0 && j >= 0) {
        nums1[k--] = nums1[i] > nums2[j] ? nums1[i--] : nums2[j--];
    }
    
    while(j >= 0) {
        nums1[k--] = nums2[j--];
    }
};
```

## Running Solutions
```bash
node "88. src/Merge Sorted Array.js"
```
