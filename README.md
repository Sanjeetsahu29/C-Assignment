# C-Assignment
## 1. Simple Interest and compound Interest
### Code 
```
#include <stdio.h>
#include <math.h>

int main() {
  // Declare variables
  float principal, rate, time, simple_interest, compound_interest;

  // Take input from user
  printf("Enter Principal Amount: ");
  scanf("%f", &principal);
  printf("Enter Rate of Interest (%): ");
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

## 2. Conversion of temperature from Celsius to Fahrenhiet
### Code
```
#include <stdio.h>

int main() {
  float celsius, fahrenheit;

  // Take input from user for Celsius temperature
  printf("Enter temperature in Celsius: ");
  scanf("%f", &celsius);

  // Convert Celsius to Fahrenheit using the formula
  fahrenheit = (celsius * 9/5) + 32;

  // Display the converted temperature
  printf("%.2f degrees Celsius is equal to %.2f degrees Fahrenheit.\n", celsius, fahrenheit);

  return 0;
}
```
### Algorithm to convert the temperature in celsius to fahrenhiet
```
1. Input
Obtain the temperature in Celsius, denoted as celsius.

2. Calculation:
Apply the following formula to celsius:
fahrenheit = (celsius * 9/5) + 32

3. Output
Store the calculated value in a variable (fahrenheit).
Display the fahrenheit value as the temperature in Fahrenheit.
```
### Flowchart
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/7d2ccb61-dcef-4e07-95b6-c744cf1ccdd5)
