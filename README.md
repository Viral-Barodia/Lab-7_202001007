JAVA Program for determinding previous date:

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

Equivalence Partitioning
32,11,2014                                      An Error message
30,11,2014                                      Yes

2. Boundary value Analysis
a) Lower Bound:
The minimum valid input value.

b) Upper Bound:
The maximum valid input value.

Boundary Value Analysis
1,1,1900                                       An Error message
2,1,1900                                       Yes

-----------------------------------------------------------------------------------------------------------------------

Program 1

Code:

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

1. Equivalence partitions:

Valid input partition - an array of integers a and an integer v:
a) a is empty
b) a has only one element
c) a has more than one element
Invalid input partition - an array of integers a and an integer v:
a) a is NULL
Output partition:
a) v is found in the array
b) v is not found in the array

2. Boundary Value Analysis:

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

Program 2

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

1. Equivalence Partitioning:

Test case where v is not present in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 6, 7, 8, 9}                            Output: 0

Test case where v is present only once in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 5, 6, 7, 8, 9}                         Output: 1

Test case where v is present multiple times in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 5, 5, 6, 7, 8, 5, 9}                   Output: 4


2. Boundary Values:

Test case with minimum input values.
Input: v = 0, a[] = {}                                                  Output: 0

Test case where the array has only one element, and it is equal to v.
Input: v = 5, a[] = {5}                                                 Output: 1

-----------------------------------------------------------------------------------------------------------------------------

Program 3

Code:

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

1. Equivalence Partitioning:

Test case where the value v is not present in the array a[].
Input: v = 5, a[] = {1, 2, 3, 4, 6, 7, 8, 9}                                 Output: -1

Test case where the value v is present at the beginning of the array a[].
Input: v = 1, a[] = {1, 2, 3, 4, 6, 7, 8, 9}                                 Output: 0

2. Boundary Values:

Test case with minimum input values.
Input: v = 5, a[] = {}                                                       Output: -1

Test case where the array has only one element, and it is equal to v.
Input: v = 5, a[] = {5}                                                      Output: 0

--------------------------------------------------------------------------------------------------------------------

Program 4

Code:
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

1. Equivalence Partitioning:

Test case where all sides are equal, forming an equilateral triangle.
Input: a = 5, b = 5, c = 5                                                          Output: EQUILATERAL

Test case where two sides are equal, forming an isosceles triangle.
Input: a = 4, b = 4, c = 5                                                          Output: ISOSCELES

2. Boundary Values:

Test case where all sides are minimum input values.
Input: a = 1, b = 1, c = 1                                                           Output: EQUILATERAL

Test case where two sides are minimum input values, and the third side is greater than the sum of the other two, forming an invalid triangle.
Input: a = 1, b = 1, c = 3                                                           Output: INVALID

--------------------------------------------------------------------------------------------------------------------------------------------

Program 5
Code:
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

1. Equivalence Partitioning:

Test case where s1 is a prefix of s2.
Input: s1 = "abc", s2 = "abcdef"
Output: true

Test case where s1 is not a prefix of s2.
Input: s1 = "abc", s2 = "defgh"
Output: false

2. Boundary Values:

Test case where s1 is equal to s2.
Input: s1 = "hello", s2 = "hello"
Output: true

Test case where s1 is one character shorter than s2.
Input: s1 = "hi", s2 = "hello"
Output: false
