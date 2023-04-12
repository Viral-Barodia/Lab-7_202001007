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

