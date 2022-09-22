## Solution
    
    function timeConversion(s) {
    // Write your code here
    let num = s.slice(0,2);
    let string = s.slice(8);
    let time = parseInt(num);
    let rest = s.slice(2,8);
    if(string === "PM" && time > 0 && time < 12){
        time += 12;
    } else if(string === "AM" && time === 12){
        time -= 12;
    }
    
    toString(time); 
    
    if(time < 10){
        toString(time); 
        return "0" + time + rest;
    } else {
        toString(time);
        return time + rest;
    }
    }
    console.log(timeConversion("07:05:45PM"));

## Approach

- The first step is to break the input string down into something easier to work with. For this, we will use .slice() to take only the first 8 characters, as well as .split to break each section (hh/mm/ss) into separate integers.
- Next, we will take to original input string and call indexOf() to determine if it is AM or PM. With .indexOf(), it is important to remember that if the argument is NOT found, the index returned will be -1.
- In this challenge, the only conversion we need to make is in the case of a PM time, we must add 12 to that number. We can convert this into a ternary rather than an if statement, but we need to remember that it is possible for 12PM to occur. In the 12PM hour, we will not want to add +12 to the original output.
- Once this is done, we can simply use a .join() call to get our output where we want it!