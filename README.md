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
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/b02f6b15-96b3-424f-bbcd-202a2d89ce5a)


## 3. Program to check whether a given number is positive or negative number
### Code
```
#include <stdio.h>

int main() {
  int number;

  // Get the number from the user
  printf("Enter a number: ");
  scanf("%d", &number);

  // Check if the number is positive, negative, or zero
  if (number > 0) {
    printf("%d is positive.\n", number);
  } else if (number < 0) {
    printf("%d is negative.\n", number);
  } else {
    printf("%d is zero.\n", number);
  }

  return 0;
}
```
### Algorithm
```
Algorithm to check if a number is positive, negative, or zero:
1. Input:
A number x (integer or real).
Steps:

2. Compare x to zero:
If x > 0 then x is positive.
If x < 0 then x is negative.
If x = 0 then x is zero.

4. Output:
Based on the comparison in step 1, determine and output the type of the number: positive, negative, or zero.
```

### Flowchart
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/fa5c2c26-9caf-429e-939d-c607e159f4d2)


## Bubble Sort
### code
```
#include <stdio.h>

void bubble_sort(int arr[], int n) {
  bool swapped = true;
  for (int i = 0; i < n - 1 && swapped; ++i) {
    swapped = false;
    for (int j = 0; j < n - i - 1; ++j) {
      if (arr[j] > arr[j + 1]) {
        int temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
        swapped = true;
      }
    }
  }
}

int main() {
  int arr[100], n;
  printf("Enter number of elements: ");
  scanf("%d", &n);
  printf("Enter %d numbers: \n", n);
  for (int i = 0; i < n; ++i) {
    scanf("%d", &arr[i]);
  }

  bubble_sort(arr, n);

  printf("Sorted array: \n");
  for (int i = 0; i < n; ++i) {
    printf("%d ", arr[i]);
  }
  printf("\n");

  return 0;
}
```

## Algorithm
```
1. Iterate through the array: Begin by going through the array from the first element to the second-to-last element.
2. Compare adjacent elements: At each step, compare two adjacent elements.
3. Swap if necessary: If the elements are in the wrong order (for example, if sorting in ascending order, and the current element is greater than the next element), swap them.
4. Continue this process: Keep going through the array, comparing and swapping adjacent elements until you reach the end.
5. Largest element moves to the end: After each full iteration through the array, the largest unsorted element will settle at the end.
6. Repeat until sorted: Repeat this process for all elements until no more swaps are needed in an iteration. If no swaps are made in a pass, it means the array is already sorted.
```
