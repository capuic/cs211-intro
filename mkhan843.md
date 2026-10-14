* **NetID:** mkhan843
* **Major:** CS
* **Question that I chose from the memoization exercise:** Count ways to reach the n'th stair
* **Link to the question article:** https://www.geeksforgeeks.org/dsa/count-ways-reach-nth-stair/
* **My solution:**

**int countWays(int n) {**

&#x20;   **// code here**

&#x20;   **int\* dp = (int\*)malloc((n+1)\*sizeof(int));**

&#x20;   **for (int i = 0; i <= n; i++) {**

&#x20;       **dp\[i] = -1;**

&#x20;   **}**

&#x20;   

&#x20;   **int result = countWaysRecursion(n, dp);**

&#x20;   **free(dp);**

&#x20;   **return result;**

**}**



**int countWaysRecursion(int n, int dp\[]) {**

&#x20;   **// code here**

&#x20;   **if (n == 0 || n == 1) {**

&#x20;       **return 1;**

&#x20;   **}**

&#x20;   

&#x20;   **if (dp\[n] != -1) {**

&#x20;       **return dp\[n];**

&#x20;   **}**

&#x20;   

&#x20;   **return dp\[n] = countWaysRecursion(n-1, dp) + countWaysRecursion(n-2, dp); // forgot to include second parameter dp**

**}**

