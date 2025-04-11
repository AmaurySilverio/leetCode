# [Two Sum](https://leetcode.com/problems/two-sum/)

## 🧩 Problem

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

## 🔍 Pattern

**Hash Map / Hash Set**

## 🛠️ Approach

- PREP (Parameters, Returns, Examples, Pseudo Code)

### Parameters

Array of integers(no funny biz, just integers.), target: integer.
Example: nums = [2,3,4], target = 6

### Returns

An array of indices of the two numbers that add up to the target. Only one valid answer exists.
Example: [0,2]

### Examples

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]

### Pseudo Code

### 1. Create a Map to Store What You've Seen

We’ll use an object to remember the numbers we’ve already gone through. The object will use:

- the number itself as a **key**
- the index where we saw it as the **value**

This helps us quickly look up if the "pairing" number exists.

### 2. Loop Through the Array

Go through each number in the array using a loop. At each step, calculate what number you’d need to add to the current number to reach the target.

### 3. Check If the Needed Number Exists

If the number you’re looking for has already been seen (it's in the map), return the index of that number and the current index.

### 4. Otherwise, Save the Current Number

If you don’t find a match, save the current number and its index in the object so it can be used later.

```js
function twoSum(nums, target) {
  let map = {}; // Step 1: Create the map

  for (let i = 0; i < nums.length; i++) {
    // Step 2: Loop through array
    const dif = target - nums[i]; // Step 3: Find the number we need to hit target

    if (dif in map) {
      // Step 4: Check if it's already in the map
      return [map[dif], i]; // ✅ Found the pair
    }

    map[nums[i]] = i; // Step 5: Store current number in the map
  }
}
```

## 💪 Answer

```js
function twoSum(nums, target) {
  //[3,2,4] 6
  let index = {}; // {key(number): value(index of number)}

  for (let i = 0; i < nums.length; i++) {
    // 0
    const dif = target - nums[i]; // 3 = 6 - 3
    if (dif in index) {
      // 3 exists in index
      return [index[dif], i]; // return [index[dif], i] -> [2,4]
    } else {
      index[nums[i]] = i; // add number: index of number to index obj
    }
  }
}
```

## ✅ Summary

- 04/11/25 - This was a fun one. How can i use hash maps to optimize sorting in my [arr]ange application?
