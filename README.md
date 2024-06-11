# 1.-Two-Sum-Java
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.  You may assume that each input would have exactly one solution, and you may not use the same element twice.  You can return the answer in any order.
Code:

class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer,Integer> hash=new HashMap<>();
        for(int i=0;i<nums.length;i++){
            hash.put(nums[i],i);
        }
        for(int i=0;i<nums.length;i++){
            int Snum=target-nums[i];
            if(hash.containsKey(Snum) && hash.get(Snum)!=i){
                return new int[]{i,hash.get(Snum)};
            }
        }
        return new int[]{};
    }
}
