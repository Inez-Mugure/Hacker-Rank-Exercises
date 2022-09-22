## Solution


        function diagonalDifference(arr) {
    // Write your code here
    let { first, second } = (arr || []).reduce((target, item, index) => {
        target['first'] += arr[index][index];
        target['second'] += arr[index][arr.length - index - 1];
                let { first, second } = (arr || []).reduce((target, item, index) => {
        target['first'] += arr[index][index];
        target['second'] += arr[index][arr.length - index - 1];
        return target;
    }, { first: 0, second: 0 });

    return Math.abs(first - second);
    }


