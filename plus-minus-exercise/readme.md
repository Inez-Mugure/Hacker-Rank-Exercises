## Problem

### Let’s break down the challenge into requirements:

- Link to challenge: HackerRank’s Plus Minus Code Challenge
- n = length of array arr, between 0 and 100
- arr = array with values between -100 and 100
- Goal is to console.log 3 values based on the number negative, positive, and zeros present in the array.
- Count the number of (positive, negative, zeros) and divide it by the total length of the array to get the ratio.

## Goal

    Write a function or functions that console.logs the ratios for positive, negative, and zero numbers in that order

## Solution


     function plusMinus(arr){
     let positives = 0, negatives = 0, zeros = 0;
     const len = arr.length || 0;
      
     if (len > 0 && len <= 100) {
          arr.map((elem, key) => {
               if (elem > 0) {
                    positives++;
               } else if (elem < 0) {
                    negatives++; 
               } else {
                    zeros++;
               }
                  
               return elem; 
          }); 
     } 
     
     console.log((positives / len) || 0);
     console.log((negatives / len) || 0);
     console.log((zeros / len) || 0);
     }