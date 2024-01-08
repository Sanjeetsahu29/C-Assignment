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
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/37cc2d67-d63d-4877-9b83-20aef61086bb)


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
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/761f97e2-ab0c-4399-89d8-a692795474a3)

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
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/a7b26aae-d0fc-4618-b1ff-e8ea0e4b6d6a)

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
int main(){
    int arr[50], num, x, y, temp;    
    printf("Please Enter the Number of Elements you want in the array: ");
    scanf("%d", &num);    
    printf("Please Enter the Value of Elements: ");
    for(x = 0; x < num; x++)
        scanf("%d", &arr[x]);
    for(x = 0; x < num - 1; x++){       
        for(y = 0; y < num - x - 1; y++){          
            if(arr[y] > arr[y + 1]){               
                temp = arr[y];
                arr[y] = arr[y + 1];
                arr[y + 1] = temp;
            }
        }
    }
    printf("Array after implementing bubble sort: ");
    for(x = 0; x < num; x++){
        printf("%d  ", arr[x]);
    }
    return 0;
}

```
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/ede0b224-ca9d-425c-af8a-c3dab33b4122)


## Algorithm
```
1. Iterate through the array: Begin by going through the array from the first element to the second-to-last element.
2. Compare adjacent elements: At each step, compare two adjacent elements.
3. Swap if necessary: If the elements are in the wrong order (for example, if sorting in ascending order, and the current element is greater than the next element), swap them.
4. Continue this process: Keep going through the array, comparing and swapping adjacent elements until you reach the end.
5. Largest element moves to the end: After each full iteration through the array, the largest unsorted element will settle at the end.
6. Repeat until sorted: Repeat this process for all elements until no more swaps are needed in an iteration. If no swaps are made in a pass, it means the array is already sorted.
```

# Prime number or not

```
#include <stdio.h>

int main() {

  int n, i, flag = 0;
  printf("Enter a positive integer: ");
  scanf("%d", &n);

  // 0 and 1 are not prime numbers
  // change flag to 1 for non-prime number
  if (n == 0 || n == 1)
    flag = 1;

  for (i = 2; i <= n / 2; ++i) {

    // if n is divisible by i, then n is not prime
    // change flag to 1 for non-prime number
    if (n % i == 0) {
      flag = 1;
      break;
    }
  }

  // flag is 0 for prime numbers
  if (flag == 0)
    printf("%d is a prime number.", n);
  else
    printf("%d is not a prime number.", n);

  return 0;
}
```

### Output
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/da65f971-7523-4715-8963-09262a2f1b73)

# Factor of a number
```
#include <stdio.h>
int main() {
    int num, i;
    printf("Enter a positive integer: ");
    scanf("%d", &num);
    printf("Factors of %d are: ", num);
    for (i = 1; i <= num; ++i) {
        if (num % i == 0) {
            printf("%d ", i);
        }
    }
    return 0;
}
```
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/e7aca9e8-6ab2-464f-b631-0104e1466880)

# Check Palindrome of a number
```
#include <stdio.h>
int main() {
  int n, reversed = 0, remainder, original;
    printf("Enter an integer: ");
    scanf("%d", &n);
    original = n;

    // reversed integer is stored in reversed variable
    while (n != 0) {
        remainder = n % 10;
        reversed = reversed * 10 + remainder;
        n /= 10;
    }

    // palindrome if orignal and reversed are equal
    if (original == reversed)
        printf("%d is a palindrome.", original);
    else
        printf("%d is not a palindrome.", original);

    return 0;
}
```
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/1ad755c1-5568-4134-9e54-7ff36d0e4fea)

# Multiplication of a number
```
#include <stdio.h>
int main() {
  int n;
  printf("Enter an integer: ");
  scanf("%d", &n);

  for (int i = 1; i <= 10; ++i) {
    printf("%d * %d = %d \n", n, i, n * i);
  }
  return 0;
}
```
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/60a9b1d2-2d4a-4676-9dba-df31b9562941)

# Sum and average of a n number
```
#include<stdio.h>
int main()
{
  int i,n,sum=0,num;
  float avg;

  printf("\nEnter How many Number you want?\n");
  scanf("%d",&n);

  printf("\nEnter elements one by one\n");
  for(i=0;i<n;++i)
   {
     scanf("%d",&num);
     sum = sum +num;
   }

  avg = sum/(float)n;

  printf("\nSum of %d Numbers = %d",n, sum);
  printf("\nAverage of %d Numbers = %.2f",n, avg);

  return 0;
}
```
![image](https://github.com/Sanjeetsahu29/C-Assignment/assets/108270460/664d6fc2-1f30-4233-b4d0-b9f443a7e371)
