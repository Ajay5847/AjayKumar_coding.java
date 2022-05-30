# AjayKumar_coding.java

#Question : 1
Leader of an array
This is the pseudo code i have written.

class Solution{
    static ArrayList<Integer> leaders(int arr[], int n){
        ArrayList<Integer>  result = new  ArrayList<Integer>();
         ArrayList<Integer>  result2 = new  ArrayList<Integer>();
        int max = arr[n-1];
        result.add(max);
        for(int i = n-2;i>=0;i--){
            if(arr[i] >= max){
                result.add(arr[i]);
                max = arr[i];
            }
        }
        for(int i = result.size() - 1;i>=0;i--){
            result2.add(result.get(i));
        }
        return result2;
    }
}
  
  
#Question : 1
Best Time to Buy and Sell a Stock.
This is the pseudo code i have written.
  
 class Solution {
    public int maxProfit(int[] prices) {
        int maxdiff = 0;
        int currdiff = 0;
        int temp = prices[0];
        for(int i = 1;i<prices.length;i++){
            currdiff = prices[i] - temp;
            if(currdiff > maxdiff){
                maxdiff = currdiff;
            }
            if(prices[i] < temp){
                temp = prices[i];
            }
        }
        return maxdiff;
    }
}


#Question : 3 
SUM OF ALL SUBSET XOR TOTALS
This is the pseudo code i have written.


class Solution {
         int k =0;
    public int subsetXORSum(int[] nums) {
        subsets(nums, 0, 0);
        return k;
    }
    
     void subsets(int[] nums, int idx, int xor){
         
         if(idx == nums.length){
            return;
         }
            for(int i=idx; i<nums.length; i++){
                
                k+=xor^nums[i];
                subsets(nums, i+1, xor^nums[i]);
        }
    }
    
}
