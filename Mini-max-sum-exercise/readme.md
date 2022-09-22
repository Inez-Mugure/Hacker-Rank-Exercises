## Solution

    function miniMaxSum(arr) {
    // Write your code here
    arr.sort(function(a, b){return a-b});
    let min=0, max=0;
    for (let i=0; i<=3; i++) {
    min += arr[i]
    }
    for (let i=arr.length-1; i>=arr.length-4; i--) {
    max += arr[i]
    }
    console.log(min, max); 
    }

## Approach

- Find the minimum and maximum element of the array.
- Calculate the sum of all the elements in the array.
- Excluding maximum element from the sum gives the minimum possible sum.
- Excluding the minimum element from the sum gives the maximum possible sum.