Download Link: https://assignmentchef.com/product/solved-cmpt360-assignment1-palindromebeer-time-and-recursion
<br>
<h1>A. Palindrome</h1>

<h2>Problem Description</h2>

A palindromic number is an integer that is the same when the digits are reversed. For example, 121 and 625526 are palindromic, but 625 is not a palindromic number.

<strong>Input:</strong>

The input is in ‘palindrome.txt’. The first line of the input contains the line count <em>m </em>(1 ≤ <em>m </em>≤ 1<em>,</em>000), which is the number of lines that follows the first line. Each of the following lines contains an integer of <em>n </em>digits (1 ≤ <em>n </em>≤ 5<em>,</em>000). <strong>Sample input:</strong>

3.

12333.

92837465.

1000000000000000123.

<strong>Output:</strong>

The output consists of <em>m </em>lines. Each line transforms the corresponding input line into a palindrome by concatenating the input and its digits in reversed order. To minimize the output length, you must not repeat the trailing digit (or, digits if there are multiple occurrences of the same digit) of the input integer.

<strong>Sample output:</strong>

1233321.

928374656473829.

1000000000000000123210000000000000001.

<strong>Submission and Grading Information</strong>

<ol>

 <li>The expected complexity is <em>O</em>(<em>n</em>).</li>

 <li>Your can assume that the input integers are positive, and does not start with zero. Write a code ‘A.YourNSID.java’ that reads ‘palindrome.txt’ and writes the output in a file called ‘A.YourNSID.txt’. <strong>Only submit the file ‘A.YourNSID.java’ in Moodle.</strong></li>

 <li>The score will be 0 if your program does not terminate within 10 seconds. If your output is correct for <em>k </em>out of <em>m </em>inputs, then you will receive a score of .</li>

</ol>

Every palindrome of 4 digits is divisible by 11 (good to know, but not related to this assignment). Can you prove it in a midterm question?

<h1>B. Beer Time</h1>

<h2>Problem Description</h2>

A group of <em>n </em>students of CMPT360 is standing around a circle, but there are (<em>n</em>−1) bottles of water and only 1 bottle of beer. They came up with an algorithm to solve their problem (yes, this is how those students are). They will start counting clockwise, starting at position 1, removing every second remaining person to get out of the circle and have a bottle of water. As the process goes on, the circle becomes smaller and smaller, until only one lucky student remains, who can have that only bottle of beer. A smart student quickly computes the position <em>J</em>(<em>n</em>) that would get the bottle of beer and stand in that position.

For example, if there are 10 people numbered 1 to 10 in clockwise order around the circle, then the order of getting a water bottle is 2, 4 , 6, 8, 10, 3, 7, 1, 9, as follows (* indicates the position where the counting starts):

*1, 2, 3, 4, 5, 6, 7, 8, 9, 10 (initial state)

1, *3, 4, 5, 6, 7, 8, 9, 10

1, 3, *5, 6, 7, 8, 9, 10

1, 3, 5, *7, 8, 9, 10

1, 3, 5, 7, *9, 10

*1, 3, 5, 7, 9

1, *5, 7, 9

1, 5, *9

*5, 9

*5 (survivor)

Here the person at the 5th position survives. Therefore, <em>J</em>(10) = 5. A quick way to find the <em>J</em>(<em>n</em>) is to use the following:

<em>J</em>(1) = 1

<em>J</em>(2<em><sup>m </sup></em>+ <em>x</em>) = 2<em>x </em>+1<em>,</em>

where <em>m </em>≥ 0 and 0 ≤ <em>x &lt; </em>2<em>m</em>.

For example, if <em>n </em>= 10, then <em>J</em>(<em>n</em>) = <em>J</em>(10) = <em>J</em>(2<sup>3</sup>+2). Therefore in this case, <em>m </em>= 3 and <em>x </em>= 2, and hence <em>J</em>(10) = 2∗2+1 = 5. Similarly, if <em>n </em>= 16, then <em>J</em>(<em>n</em>) = <em>J</em>(16) = <em>J</em>(2<sup>4</sup>+0). Therefore, <em>m </em>= 4<em>,x </em>= 0, and <em>J</em>(16) = 2 ∗ 0+1 = 1.

<strong>Input:</strong>

The input is in ‘beer.txt’. The first line of the input contains the line count <em>c </em>(1 ≤ <em>c </em>≤ 1<em>,</em>000), which is the number of lines that follows the first line. Each of the following lines contains an integer <em>n </em>(1 ≤ <em>n </em>≤ 10<em>,</em>000). <strong>Sample input:</strong>

2.

<ol start="16">

 <li>10.</li>

</ol>

<strong>Output:</strong>

The output consists of <em>c </em>lines. Each line prints the lucky position <em>J</em>(<em>n</em>) of the corresponding input.

<strong>Sample output:</strong>

1.

5.

<strong>Submission and Grading Information</strong>

<ol>

 <li>The expected complexity is <em>O</em>(log<em>n</em>).</li>

 <li>Write a code ‘B.YourNSID.java’ that reads ‘beer.txt’ and writes the output in a file called ‘B.YourNSID.txt’. <strong>Only submit the file ‘B.YourNSID.java’ in Moodle.</strong></li>

 <li>The score will be 0 if your program does not terminate within 3 seconds. If your output is correct for <em>k </em>out of <em>m </em>inputs, then you will receive a score of .</li>

</ol>

<h2>C. Recursion</h2>

Recursion may appear in various contexts and in different forms. For fast implementation, we should always aim at transforming recursions into a simpler form of computation. In this assignment, the task is to evaluate <em>X</em>(·), which is defined as follows:

<table>

 <tbody>

  <tr>

   <td></td>

  </tr>

 </tbody>

</table>

0<em>,</em>if <em>m </em>= 0 or <em>n </em>= 0

is odd and <em>m </em>is even <em>n </em>is even otherwise.

<strong>Input:</strong>

The input is in ‘recursion.txt’. The first line of the input contains the line count <em>c </em>(1 ≤ <em>c </em>≤ 1<em>,</em>000)<sub>, which is the number of lines that follows the first line. Each of the following lines </sub>contains a pair of integers <em>m,n </em>(1 ≤ <em>m,n </em>≤ 10<em>,</em>000). <strong>Sample input:</strong>

3.

102,21.

10000,10000.

<strong>Output:</strong>

The output consists of <em>c </em>lines. Each line prints <em>X</em>(<em>m,n</em>). <strong>Sample output:</strong>

2060.

100010000.

<strong>Submission and Grading Information</strong>

<ol>

 <li>The expected complexity is <em>O</em>(1).</li>

 <li>Write a code ‘C.YourNSID.java’ that reads ‘recursion.txt’ and writes the output in a file called ‘C.YourNSID.txt’. <strong>Only submit the file ‘C.YourNSID.java’ in Moodle.</strong></li>

 <li>The score will be 0 if your program does not terminate within 3 seconds. If your output is correct for <em>k </em>out of <em>m </em>inputs, then you will receive a score of .</li>

</ol>

<h2>D. Software Testing (Time Limit: 10 Seconds)</h2>

Murphy’s law states that ‘things will go wrong in any given situation, if you give them a chance,’ or more commonly, ‘whatever can go wrong, will go wrong.’ Many automated software testing tries to test for all possible inputs, whenever the number of possibilities are reasonably small.

An image is normally processed by a set of three satellite modules <em>m</em><sub>1</sub><em>,m</em><sub>2</sub><em>,m</em><sub>3 </sub>in this order. The image might get corrupted during the transfer. During this process, a module <em>m<sub>j </sub></em>can request any of its predecessor <em>m<sub>i</sub></em>, where 1 ≤ <em>i &lt; j </em>≤ 3, to resend the information. Upon receiving a resend request, <em>m<sub>i </sub></em>must pass the data to the next module <em>m<sub>i</sub></em><sub>+1</sub>.

A normal processing must start at <em>m</em><sub>1 </sub>and end at <em>m</em><sub>3</sub>. If the maximum number of total resend requests exceeds <em>n</em>, then the system generates an alarm.

We want to count the number of different ways with exactly <em>n </em>resend requests. If <em>n </em>= 1, then there are exactly 3 different ways (* denotes the resend request).

12*123 [2 gets the corrupt data and decides to ask from 1]

123*23 [3 gets the corrupt data and decides to ask from 2]

123*123 [3 gets the corrupt data and decides to ask from 1] If <em>n </em>= 2, then the number of different ways is 8.

12*12*123

12*123*123

12*123*23

123*23*23

123*23*123

123*123*23

123*123*123

123*12*123

<strong>Input:</strong>

The input is in ‘software.txt’. The first line of the input contains the line count <em>m </em>(1 ≤ <em>m </em>≤ 1<em>,</em>000), which is the number of lines that follows the first line. Each of the following lines contains an integer <em>n </em>(1 ≤ <em>n </em>≤ 10<em>,</em>000). <strong>Sample input:</strong>

2.

1.

2.

<strong>Output:</strong>

The output consists of <em>m </em>lines. Each line prints the number of different ways that exactly <em>n </em>resend requests can happen.

<strong>Sample output:</strong>

3.

8.

<strong>Submission and Grading Information</strong>

<ol>

 <li>The expected complexity is <em>O</em>(<em>n</em>).</li>

 <li>Write a code ‘D.YourNSID.java’ that reads ‘software.txt’ and writes the output in a file called ‘D.YourNSID.txt’. <strong>Only submit the file ‘D.YourNSID.java’ in Moodle.</strong></li>

 <li>The score will be 0 if your program does not terminate within 10 seconds. If your output is correct for <em>k </em>out of <em>m </em>inputs, then you will receive a score of .</li>

</ol>

<h2>E. World of Unknowns, Time limit: 3 seconds</h2>

The Collatz conjecture is about a sequence: start with any positive integer n. Then each term is obtained from the previous term as follows: if the previous term is even, the next term is one half the previous term. If the previous term is odd, the next term is 3 times the previous term plus 1. The conjecture is that no matter what value of n, the sequence will always reach 1.

is odd <em>f</em>(<em>n</em>/2)<em>,</em>otherwise.

Your task is to count the number of terms in the sequence. For example, if <em>n </em>= 12, then the sequence has 10 terms: 12<em>,</em>6<em>,</em>3<em>,</em>10<em>,</em>5<em>,</em>16<em>,</em>8<em>,</em>4<em>,</em>2<em>,</em>1.

<strong>Input:</strong>

The input is in ‘sequence.txt’. The first line of the input contains the line count <em>m </em>(1 ≤ <em>m </em>≤ 1<em>,</em>000), which is the number of lines that follows the first line. Each of the following lines contains an integer <em>n </em>(1 ≤ <em>n </em>≤ 10<em>,</em>000). <strong>Sample input:</strong>

2.

12.

27.

<strong>Output:</strong>

The output consists of <em>m </em>lines. Each line prints the number of terms in the sequence of <em>f</em>(<em>n</em>). <strong>Sample output:</strong>

10.

112.

<strong>Submission and Grading Information</strong>

<ol>

 <li>The complexity is unknown, but try your fastest algorithm &#x1f642;</li>

 <li>Write a code ‘E.YourNSID.java’ that reads ‘sequence.txt’ and writes the output in a file called ‘E.YourNSID.txt’. <strong>Only submit the file ‘E.YourNSID.java’ in Moodle.</strong></li>

 <li>The score will be 0 if your program does not terminate within 10 seconds. If your output is correct for <em>k </em>out of <em>m </em>inputs, then you will receive a score of .</li>

</ol>