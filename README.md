Download Link: https://assignmentchef.com/product/solved-cs-3723-hw-5-operators
<br>
In this assignment, we will explore some simple expressions and evaluate them. We will use an unconventional approach and severely limit the expressions. The focus will be on operator precedence.

The only operators we support are logical or (|), logical and (&amp;), less than (&lt;), equal to (=), greater than (&gt;), add (+), subtract (-), multiply (*) and divide (/). Each has a precedence level from 1 to 5 where higher precedence operators are evaluated first, from left-to-right. For example, “1 + 2 * 3” is 1+6 = 7. It is NOT 3*3 = 9.

To evaluate an expression like “8 – 2*2 – 3” we first split it into two parts: “8 – 2*2” and “3”. We recursively evaluate “8 – 2*2” = 4 and “3” = 3. We subtract to get 4-3 = 1. Note that we look for the operators from right to left so they get evaluated from left to right (as shown in this example).

When we recursively evaluate “8 – 2*2” we split it into “8” = 8 and “2*2” = 4 so it returns 8-4 = 4.

Don’t worry about errors like divide-by-zero, overflow, etc. All operators and numbers are exactly one character long. No unary operators like negation (-) or not (!) and no parentheses are allowed.

You are not permitted to make substantive changes to the existing code. You should only modify the two TBD blocks.

Here is some sample output (you are not given the debug statements with ***):

Value of  4  is 4 as expected




Value of 9+8 is 17 as expected




*** Value of 4 * 5 is 20

Value of  3 + 4 * 5  is 23 as expected




*** Value of 9 – 2 is 7

Value of  9 – 2 – 1 is 6 as expected




*** Value of 3=4 is 0

*** Value of 5&lt;6 is 1

*** Value of 7&lt;8 is 1

*** Value of 5&lt;6 &amp; 7&lt;8 is 1

Value of 3=4 | 5&lt;6 &amp; 7&lt;8 is 1 as expected




*** Value of 3 * 6 is 18

Value of 2 + 3 * 6 is 20




Value of 8/4 is 2




Value of 3=4 is 0




Value of BOB + 5 is an Error

Hint #1: chars in C are the same as ints. ‘0’ equals 48, etc.

Hint #2: sc is the starting char, 0 is first. ec is ending char plus 1. Given “1+3” sc=2 ec=3 is just “3”.