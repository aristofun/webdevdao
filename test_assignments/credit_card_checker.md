## Ruby: credit card checker

**Task**

Write a program that accepts a credit card number as a command-line argument. The program should print the card's type (or Unknown) as well a Valid/Invalid indication of whether or not the card passes the Luhn algorithm.

Hint: use git, cover with specs, make some user friendly interface (can be a command line), make it modular.

Before a credit card is submitted to a financial institution, it generally makes sense to run some simple reality checks on the number. The numbers are a good length and it's common to make minor transcription errors when the card is not scanned directly. The first check people often do is to validate that the card matches a known pattern from one of the accepted card providers. Some of these patterns are:

| Card Type  | Begins With | Number Length |
| ---------- |------------ | ------------- |
| AMEX       | 34 or 37    | 15            |
| Discover   | 6011        | 16            |
| MasterCard | 51-55       | 16            |
| Visa       | 4           | 13 or 16      |

All of these card types also generate numbers such that they can be validated by the Luhn algorithm, so that's the second check systems usually try.

1. The steps are:

    1.1. Starting with the next to last digit and continuing with every other digit going back to the beginning of the card, double the digit

    1.2. Sum all doubled and untouched digits in the number

    1.3. If that total is a multiple of 10, the number is valid

2. For example, given the card number `4408 0412 3456 7893`:

    2.1. `8 4 0 8 0 4 2 2 6 4 10 6 14 8 18 3`

    2.2. `8+4+0+8+0+4+2+2+6+4+1+0+6+1+4+8+1+8+3 = 70`

    2.3. `70 % 10 == 0 #=> This that card is valid.`

3. Let's try one more, `4417 1234 5678 9112`:

    3.1. `8 4 2 7 2 2 6 4 10 6 14 8 18 1 2 2`

    3.2. `8+4+2+7+2+2+6+4+1+0+6+1+4+8+1+8+1+2+2 = 69`

    3.3. `69 % 10 != 0 #=> That card is not valid.`
