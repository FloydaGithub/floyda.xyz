---
title: 两数之和
tags: ["Rust", "LeetCode", "边学Rust边LeetCode"]
excerpt: 两数之和
date: 2020-2-25
---


# [边学Rust边LeetCode][两数之和](https://leetcode-cn.com/problems/two-sum/)
> 给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。  
> 你可以假设每种输入只会对应一个答案。但是，你不能重复利用这个数组中同样的元素。  
> 示例:  
> ```  
> 给定 nums = [2, 7, 11, 15], target = 9  
>   
> 因为 nums[0] + nums[1] = 2 + 7 = 9  
> 所以返回 [0, 1]  
> ```  


## Code  
```rust
use std::collections::HashMap;

impl Solution {
    pub fn two_sum(nums: Vec<i32>, target: i32) -> Vec<i32> {
        let mut hash = HashMap::with_capacity(nums.len());

        for (k, v) in nums.iter().enumerate() {
            match hash.get(&(target - v)) {
                None => { hash.insert(v, k); },
                Some(pos) => {
                    return vec![*pos as i32, k as i32]
                }
            }
        }
        vec![]
    }
}
```  

