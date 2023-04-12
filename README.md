### Problem 0

##### JAVA Program for determinding previous date:

import java.time.LocalDate;

public class PreviousDate {
    public static void main(String[] args) {
        // Get today's date
        LocalDate today = LocalDate.now();
        
        // Calculate the previous day
        LocalDate previousDay = today.minusDays(1);
        
        // Print the previous day's date
        System.out.println("The previous date was: " + previousDay);
    }
}

1. Partition the input data into equivalence classes:

a) Invalid Input:

Inputs that are not of type integer or outside the valid range.
b) Valid Input:

Inputs that are of type integer and within the valid range.

Test cases for the same:
Tester Action and Input Data                  Expected Outcome

##### 1. Equivalence Partitioning
32,11,2014                                      An Error message
30,11,2014                                      Yes

##### 2. Boundary value Analysis
a) Lower Bound:
The minimum valid input value.

b) Upper Bound:
The maximum valid input value.

Boundary Value Analysis
1,1,1900                                       An Error message
2,1,1900                                       Yes

-----------------------------------------------------------------------------------------------------------------------

### Program 1

##### Code:

int linearSearch(int v, int a[])
{
int i = 0;
while (i < a.length)
{
if (a[i] == v)
return(i);
i++;
}
return (-1);
}

##### 1. Equivalence partitions:

Valid input partition - an array of integers a and an integer v:
a) a is empty
b) a has only one element
c) a has more than one element
Invalid input partition - an array of integers a and an integer v:
a) a is NULL
Output partition:
a) v is found in the array
b) v is not found in the array

##### 2. Boundary Value Analysis:

For the given code, we can generate the following boundary value test cases:

Valid input test cases:
a) a is empty
b) a has only one element
c) a has two elements (one element equal to v, one element not equal to v)
d) a has more than two elements (one element equal to v, one element not equal to v, and one element between them)
e) a has more than two elements (no element equal to v)
f) a has more than two elements (all elements equal to v)
Invalid input test cases:
a) a is NULL
Output test cases:
a) v is found in the array
b) v is not found in the array

-------------------------------------------------------------------------------------------------------------------------------------------------------------

### Program 2

Code:
int countItem(int v, int a[])

{
int count = 0;
for (int i = 0; i < a.length; i++)
{
if (a[i] == v)
count++;

}
return (count);
}

##### 1. Equivalence Partitioning:

Test case where v is not present in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 6, 7, 8, 9}                            Output: 0

Test case where v is present only once in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 5, 6, 7, 8, 9}                         Output: 1

Test case where v is present multiple times in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 5, 5, 6, 7, 8, 5, 9}                   Output: 4


##### 2. Boundary Values:

Test case with minimum input values.
Input: v = 0, a[] = {}                                                  Output: 0

Test case where the array has only one element, and it is equal to v.
Input: v = 5, a[] = {5}                                                 Output: 1

-----------------------------------------------------------------------------------------------------------------------------

### Program 3

##### Code:

int binarySearch(int v, int a[])
{
int lo,mid,hi;
lo = 0;
hi = a.length-1;
while (lo <= hi)
{
mid = (lo+hi)/2;
if (v == a[mid])
return (mid);
else if (v < a[mid])
hi = mid-1;
else
lo = mid+1;

}
return(-1);
}

##### 1. Equivalence Partitioning:

Test case where the value v is not present in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 6, 7, 8, 9}                                 Output: -1

Test case where the value v is present at the beginning of the array a[].
Input: v = 1, a[] = {1, 2, 3, 4, 6, 7, 8, 9}                                 Output: 0

##### 2. Boundary Values:

Test case with minimum input values.
Input: v = 5, a[] = {}                                                       Output: -1

Test case where the array has only one element, and it is equal to v.
Input: v = 5, a[] = {5}                                                      Output: 0

--------------------------------------------------------------------------------------------------------------------

### Program 4

##### Code:
final int EQUILATERAL = 0;
final int ISOSCELES = 1;
final int SCALENE = 2;
final int INVALID = 3;
int triangle(int a, int b, int c)
{
if (a >= b+c || b >= a+c || c >= a+b)
return(INVALID);
if (a == b && b == c)
return(EQUILATERAL);
if (a == b || a == c || b == c)
return(ISOSCELES);
return(SCALENE);

}

##### 1. Equivalence Partitioning:

Test case where all sides are equal, forming an equilateral triangle.
Input: a = 5, b = 5, c = 5                                                          Output: EQUILATERAL

Test case where two sides are equal, forming an isosceles triangle.
Input: a = 4, b = 4, c = 5                                                          Output: ISOSCELES

##### 2. Boundary Values:

Test case where all sides are minimum input values.
Input: a = 1, b = 1, c = 1                                                           Output: EQUILATERAL

Test case where two sides are minimum input values, and the third side is greater than the sum of the other two, forming an invalid triangle.
Input: a = 1, b = 1, c = 3                                                           Output: INVALID

--------------------------------------------------------------------------------------------------------------------------------------------

### Program 5

##### Code:
public static boolean prefix(String s1, String s2)
{
if (s1.length() > s2.length())
{
return false;
}
for (int i = 0; i < s1.length(); i++)
{
if (s1.charAt(i) != s2.charAt(i))
{
return false;
}
}
return true;
}

##### 1. Equivalence Partitioning:

Test case where s1 is a prefix of s2.
Input: s1 = "abc", s2 = "abcdef"                                                     Output: true

Test case where s1 is not a prefix of s2.
Input: s1 = "abc", s2 = "defgh"                                                      Output: false

##### 2. Boundary Values:

Test case where s1 is equal to s2.
Input: s1 = "hello", s2 = "hello"                                                   Output: true

Test case where s1 is one character shorter than s2.
Input: s1 = "hi", s2 = "hello"                                                      Output: false

-------------------------------------------------------------------------------------------------------------------------------------------------

### Program 6

Consider again the triangle classification program (P4) with a slightly different specification: <br>
The program reads floating values from the standard input. The three values A, B, and C are interpreted as representing the lengths of the sides of a triangle. <br>
The program then prints a message to the standard output that states whether the triangle, if it can be formed, is scalene, isosceles, equilateral, or right angled.<br>
Determine the following for the above program:<br>
<br>

**a) Identify the equivalence classes for the system<br>**

##### Equivalence Classes:<br>
EC1: All sides are positive, real numbers.<br>
EC2: One or more sides are negative or zero.<br>
EC3: The sum of the lengths of any two sides is less than or equal to the length of the remaining side (impossible lengths).<br>
EC4: The sum of the lengths of any two sides is greater than the length of the remaining side (possible lengths).<br>

<br>


**b) Identify test cases to cover the identified equivalence classes. Also, explicitly mention which test case would cover which equivalence class.<br>**
(Hint: you must need to be ensure that the identified set of test cases cover all identified equivalence classes)<br>

Test cases:<br>
TC1 (EC1): A=3, B=4, C=5 (right-angled triangle)<br>
TC2 (EC1): A=5, B=5, C=5 (equilateral triangle)<br>
TC3 (EC1): A=5, B=6, C=7 (scalene triangle)<br>
TC4 (EC1): A=5, B=5, C=7 (isosceles triangle)<br>
TC5 (EC2): A=-2, B=4, C=5 (invalid input)<br>
TC6 (EC2): A=0, B=4, C=5 (invalid input)<br>

<br>


**c) For the boundary condition A + B > C case (scalene triangle), identify test cases to verify the boundary.<br>**

Test cases for the boundary condition A + B > C:<br>
TC7 (EC4): A=2, B=3, C=6 (sum of A and B is equal to C)<br>

<br>


**d) For the boundary condition A = C case (isosceles triangle), identify test cases to verify the boundary.<br>**

Test cases for the boundary condition A = C:<br>
TC8 (EC4): A=5, B=6, C=5 (A equals to C)<br>

<br>

**e) For the boundary condition A = B = C case (equilateral triangle), identify test cases to verify the boundary.<br>**

Test cases for the boundary condition A = B = C:<br>
TC9 (EC4): A=1, B=1, C=1 (all sides are equal)<br>

<br>

**f) For the boundary condition A2 + B2 = C2 case (right-angle triangle), identify test cases to verify the boundary.<br>**

Test cases for the boundary condition A^2 + B^2 = C^2:<br>
TC10 (EC4): A=3, B=4, C=5 (right-angled triangle)<br>

<br>

**g) For the non-triangle case, identify test cases to explore the boundary.<br>**

Test cases for the non-triangle case:<br>
TC11 (EC3): A=2, B=2, C=4 (sum of A and B is less than C)<br>

<br>

**h) For non-positive input, identify test points.<br>**

Test points for non-positive input:<br>
TP1 (EC2): A=0, B=4, C=5 (invalid input)<br>
TP2 (EC2): A=-2, B=4, C=5 (invalid input)<br>
Note: Test cases TC1 to TC10 covers all identified equivalence classes.<br>
