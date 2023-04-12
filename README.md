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
