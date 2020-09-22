# Maximum-Subarray
#This program is for finding the largest sum subarray by using Kadane's Algorithm.Time complexity of this program is o(n) which is very efficient process of solving the problem.
class Solution {
    public int maxSubArray(int[] nums) {
        //By Kandane's Algorithm
        int maxSum=Integer.MIN_VALUE;
        int currSum = 0;
        
        for(int i=0;i<nums.length;i++){
            currSum += nums[i];
            if(currSum>maxSum){
                maxSum=currSum;
            }
            if(currSum<0){
                currSum=0; //reset current sum as we dont need negative no.
                
            }
            
        }
       
        return maxSum;
    }
}
