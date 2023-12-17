# C-Assignment
### Code for Simple Interest and compound Interest
```
#include <stdio.h>
#include <math.h>

int main() {
  // Declare variables
  float principal, rate, time, simple_interest, compound_interest;

  // Take input from user
  printf("Enter Principal Amount: ");
  scanf("%f", &principal);
  printf("Enter Rate of Interest (%%): ");
  scanf("%f", &rate);
  printf("Enter Time (in years): ");
  scanf("%f", &time);

  // Calculate simple interest
  simple_interest = (principal * rate * time) / 100;

  // Calculate compound interest using pow function
  compound_interest = principal * pow((1 + (rate / 100)), time);

  // Print results
  printf("Simple Interest: %.2f \n", simple_interest);
  printf("Compound Interest: %.2f \n", compound_interest);

  return 0;
}
```

### Algorithm to Find Simple Interest and Compound Interest

```
1. Start
2. Declare variables: 
     - principal (float)
     - rate (float)
     - time (float)
     - simpleInterest (float)
     - compoundInterest (float)
3. Input principal amount (principal)
4. Input rate of interest (rate)
5. Input time period in years (time)
6. Calculate simpleInterest as (principal * rate * time) / 100
7. Calculate compoundInterest as principal * (pow((1 + rate / 100), time)) - principal
8. Display "Simple Interest is: " + simpleInterest
9. Display "Compound Interest is: " + compoundInterest
10. End
```
###   Flowchart to find Simple Interest and Compound Interest
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/0d9b0dd9-5f44-4b74-90cd-016bbdcaad7a)
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/b8e7dd07-6a06-4037-a0c2-4697d861dde4)


