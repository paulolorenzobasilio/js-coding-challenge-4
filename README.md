# js-coding-challenge-4
Javascript Coding Challenge 4

## Requirements
Write a function that accepts an integer and returns a “validation” number. This validation number is calculated by adding all the digits in the input. 

If the result of this sum has more than a single digit, another iteration is required, repeat the process until a single digit number is calculated. 


```javascript
const calculateValidationNumber = (numbers => {
        const digits = numbers.toString().split('').map(Number)
        const total = digits.reduce((previousDigit, currentDigit) => previousDigit + currentDigit);

        if (total.toString().length > 1) {
            return calculateValidationNumber(total)
        }

        return total
    })


    console.log('444444 = ', calculateValidationNumber(444444))
    console.log('1234 = ', calculateValidationNumber(1234))
    console.log('23478998 = ', calculateValidationNumber(23478998))
```
