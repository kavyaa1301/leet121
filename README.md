# leet121
# Solution: Best Time to Buy and Sell Stock (LeetCode 121)

## Problem Description
You are given an array `prices` where `prices[i]` is the price of a given stock on the `i-th` day.

Your goal is to maximize your profit by choosing a **single day** to buy one stock and choosing a **different day in the future** to sell that stock. Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return `0`.

**Examples:**Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.

Input: prices = [7,6,4,3,1]
Output: 0
Explanation: In this case, prices are constantly decreasing, so no profit is possible
## Approach: One Pass (Greedy Algorithm)
This solution uses a single pass through the prices array to track the minimum price encountered and calculate the maximum potential profit at each step.

### Intuition
The key insight is that the maximum profit is determined by the largest difference between a selling price and the minimum buying price that occurred before it. We need to:
- Track the lowest price seen so far (`minPrice`)
- At each day, calculate the profit if we sold at the current price (after having bought at `minPrice`)
- Keep the maximum profit found (`maxProfit`)
- ## Approach: One Pass (Greedy Algorithm)
This solution uses a single pass through the prices array to track the minimum price encountered and calculate the maximum potential profit at each step.

### Intuition
The key insight is that the maximum profit is determined by the largest difference between a selling price and the minimum buying price that occurred before it. We need to:
- Track the lowest price seen so far (`minPrice`)
- At each day, calculate the profit if we sold at the current price (after having bought at `minPrice`)
- Keep the maximum profit found (`maxProfit`)
- ## Complexity Analysis
- **Time Complexity**: O(n) - Single pass through the array
- **Space Complexity**: O(1) - Only two variables used regardless of input size
###  Key Features
✅ Single pass: Processes each element only once
✅ Constant space: Uses only O(1) extra memory
✅ Handles edge cases: Returns 0 when no profit is possible
✅ Optimal solution: Most efficient approach for this problem
### Conclusion
This one-pass greedy algorithm provides the optimal solution for finding the maximum profit from a single buy-sell transaction. The solution efficiently tracks the minimum price and maximum profit simultaneously, making it both time and space optimal.
