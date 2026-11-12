# LeetCode Top 150 java Problems

# 88. Merge Sorted Array

**Difficulty:** Easy

**LeetCode:** https://leetcode.com/problems/merge-sorted-array/

## Problem Description

You are given two integer arrays, `nums1` and `nums2`, sorted in non-decreasing order.

- `nums1` has a length of `m + n`, where the first `m` elements contain valid values and the remaining `n` positions are empty (represented by zero).
- `nums2` has `n` elements.

Merge `nums2` into `nums1` as one sorted array.

The final sorted array must be stored inside `nums1`.

## Example

**Input:**
```text
nums1 = [1,3,5,0,0,0]
m = 3
nums2 = [2,4,6]
n = 3
```

**Output:**
```text
[1,2,3,4,5,6]
```

## Approach: Three Pointers (Merge from the End)

Instead of merging from the beginning, we start from the end of both arrays.

We use three pointers:

- `i = m - 1`: Last valid element in `nums1`.
- `j = n - 1`: Last element in `nums2`.
- `k = m + n - 1`: Last available position in `nums1`.

### Algorithm

1. Compare the elements at `nums1[i]` and `nums2[j]`.
2. Place the larger element at `nums1[k]`.
3. Move the corresponding pointer backward.
4. Decrease `k` after every placement.
5. Continue until all elements of `nums2` are merged.

## Complexity Analysis

- **Time Complexity:** O(m + n)
- **Space Complexity:** O(1) — in-place merging using constant extra space.

## Key Learnings

- Two-pointer technique.
- Merging sorted arrays.
- Traversing arrays from right to left.
- Avoiding overwriting existing elements.

