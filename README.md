# Lab-7_202001214
# Software Engineering IT314
## Name: Rons M Adhaduk
## Section A:
### 1) Consider a program for determining the previous date. Its input is triple of day, month and year with the following ranges 1 <= month <= 12, 1 <= day <= 31, 1900 <= year <= 2015.The possible output dates would be previous date or invalid date. Design the equivalence class test cases?
#### - Following are the equivalence class according to given input
#### i) Valid dates: The input triple (day, month, year) that represent a valid date in the Gregorian calendar, such as (3, 11, 1999).
#### ii) Invalid dates: The input triple (day, month, year) that represent an invalid date, such as (30, 2, 2020) or (31, 4, 1967).
#### iii) Out of range dates: The input triple (day, month, year) that are outside the allowed ranges, such as (0, 8, 2030) or (18, 13, 2012). 
#### -Based on these equivalence classes, we can design the following test cases:
**Valid dates:**<br>
| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Calculate previous date for (15, 10, 2022)          | 14, 10, 2022         | 
| Calculate previous date for (1, 1, 2015)         | 31, 12, 2014         | 
| Calculate previous date for (31, 3, 2000)          | 30, 3, 2000         | 

**Invalid dates:**<br>
| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Calculate previous date for (29, 2, 2022)          | Invalid date        | 
| Calculate previous date for (31, 4, 2010)       | Invalid date       | 
| Calculate previous date for (30, 2, 2000)         | Invalid date        | 


**Out of range dates:**<br>
| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Calculate previous date for (0, 5, 2010)          | Invalid date        | 
| Calculate previous date for (15, 13, 2005)       | Invalid date       | 
| Calculate previous date for (31, 12, 1899)         | Invalid date        | 

## **Boundary Value Analysis:**<br>
Using boundary value analysis, we can identify the following boundary test cases:
1) The earliest possible date: (1, 1, 1900)
2) The latest possible date: (31, 12, 2015)
3) The earliest day of each month: (1, 1, 2000), (1, 2, 2000), (1, 3, 2000),..., (1, 12, 2000)
4) The latest day of each month: (31, 1, 2000), (28, 2, 2000), (31, 3, 2000),..., (31, 12, 2000)
5) Leap year day: (29, 2, 2000)
6) Invalid leap year day: (29, 2, 1900)
7) One day before earliest date: (31, 12, 1899)
8) One day after latest date: (1, 1, 2016)<br>

Based on these boundary test cases, we can design the following test cases:<br>
Tester Action and Input Data Expected Outcome<br>

**Boundary Test Cases:**<br>
| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Calculate previous date for (1, 1, 1900)          | Invalid date        | 
| Calculate previous date for (31, 12, 2015)       | 30, 12, 2015       | 
| Calculate previous date for (1, 1, 2000)         | 31, 12, 1999        | 
| Calculate previous date for (31, 1, 2000)       | 30, 1, 2000        | 
| Calculate previous date for (29, 2, 2000)       | 28, 2, 2000       | 
| Calculate previous date for (29, 2, 1900)         | Invalid date        | 

<br>

## Program 1:
The function linearSearch searches for a value v in an array of integers a. <br>
If v appears in the array a, then the function returns the first index i, such that a[i] == v; otherwise, -1 is returned.<br>
int linearSearch(int v, int a[])<br>
{
int i = 0;<br>
while (i < a.length)<br>
{<br>
if (a[i] == v)<br>
return(i);<br>
i++;<br>
}<br>
return (-1);<br>
}

**Equivalence Partitioning:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| v is present in a        | Index of v         | 
| v is not present in a         | -1         | 

**Boundary Value Analysis:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Empty array a        | -1         | 
| v is present at the first index of a         | 0         | 
| v is present at the last index of a length of a        | -1         | 
| v is not present in a         | -1         | 





<br>

## Program 2:
The function countItem returns the number of times a value v appears in an array of integers a.<br>
int countItem(int v, int a[])<br>

{<br>
int count = 0;<br>
for (int i = 0; i < a.length; i++)<br>
{<br>
if (a[i] == v)<br>
count++;<br>

}<br>
return (count);<br>
}

**Equivalence Partitioning:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| v is present in a        | Number of times v appears in a         | 
| v is not present in a         | 0         | 

**Boundary Value Analysis:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Empty array a        | 0         | 
| v is present once in a         | 1         | 
| v is present multiple times in a        | Number of times v appears in a         | 
| v is present at the first index of a         | 1         | 
| v is present at the last index of a        | 1        | 
| v is not present in a         | 0        | 

<br>

## Program 3:
The function binarySearch searches for a value v in an ordered array of integers a. <br>
If v appears in the array a, then the function returns an index i, such that a[i] == v; otherwise, -1 is returned.<br>
Assumption: the elements in the array a are sorted in non-decreasing order.<br>
int binarySearch(int v, int a[])<br>
{<br>
int lo,mid,hi;<br>
lo = 0;<br>
hi = a.length-1;<br>
while (lo <= hi)<br>
{<br>
mid = (lo+hi)/2;<br>
if (v == a[mid])<br>
return (mid);<br>
else if (v < a[mid])<br>
hi = mid-1;<br>
else<br>
lo = mid+1;<br>
}<br>
return(-1);<br>
}


**Equivalence Partitioning:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| v is present in a        | Index of v         | 
| v is not present in a         | -1         | 

**Boundary Value Analysis:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Empty array a        | -1         | 
| v is present at the first index of a         | 0         | 
| v is present at the last index of a length of a        | -1         | 
| v is not present in a         | -1         | 

<br>

## Program 4:
P4. The following problem has been adapted from The Art of Software Testing, by G. Myers (1979). <br>
The function triangle takes three integer parameters that are interpreted as the lengths of the sides of a triangle. <br>
It returns whether the triangle is equilateral (three lengths equal), isosceles (two lengths equal), scalene (no lengths equal), or invalid (impossible lengths).<br>

final int EQUILATERAL = 0;<br>
final int ISOSCELES = 1;<br>
final int SCALENE = 2;<br>
final int INVALID = 3;<br>
int triangle(int a, int b, int c)<br>
{<br>
if (a >= b+c || b >= a+c || c >= a+b)<br>
return(INVALID);<br>
if (a == b && b == c)<br>
return(EQUILATERAL);<br>
if (a == b || a == c || b == c)<br>
return(ISOSCELES);<br>
return(SCALENE);<br>
}


**Equivalence Partitioning:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Invalid triangle (a+b<=c)        | INVALID         | 
| Valid equilateral triangle (a=b=c)         | EQUILATERAL         | 
| Valid isosceles triangle (a=b<c)        | ISOSCELES         | 
| Valid scalene triangle (a<b<c)         | SCALENE         | 

**Boundary Value Analysis:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Invalid triangle (a+b<=c)        | INVALID         | 
| Invalid triangle (a+c<b)         | INVALID         | 
| Invalid triangle (b+c<a)        | INVALID         | 
| Valid equilateral triangle (a=b=c)         | EQUILATERAL         | 
| Valid isosceles triangle (a=b<c)        | ISOSCELES         | 
| Valid isosceles triangle (a=c<b)        | ISOSCELES         | 
| Valid isosceles triangle (b=c<a)        | ISOSCELES         | 
| Valid scalene triangle (a<b<c)         | SCALENE         | 

<br>

## Program 5:
The function prefix (String s1, String s2) returns whether or not the string s1 is a prefix of string s2 (you may assume that neither s1 nor s2 is null).<br>
public static boolean prefix(String s1, String s2)<br>
{<br>
if (s1.length() > s2.length())<br>
{<br>
return false;<br>
}<br>
for (int i = 0; i < s1.length(); i++)<br>
{<br>
if (s1.charAt(i) != s2.charAt(i))<br>
{<br>
return false;<br>
}<br>
}<br>
return true;<br>
}

**Equivalence Partitioning:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Empty string s1 and s2        | True         | 
| Empty string s1 and non-empty s2         | True         | 
| Non-empty s1 is a prefix of non-empty s2        | True         | 
| Non-empty s1 is not a prefix of s2         | False         | 
| Non-empty s1 is longer than s2         | False         | 

**Boundary Value Analysis:**

| Tester Action and Input Data     | Expected Outcome      | 
| ------------- | :---: | 
| Empty string s1 and s2        | True         | 
| Empty string s1 and non-empty s2         | True         | 
| Non-empty s1 is not a prefix of s2         | False         | 
| Non-empty s1 is longer than s2         | False         | 
<br>

## Program 6:
Consider again the triangle classification program (P4) with a slightly different specification: <br>
The program reads floating values from the standard input. The three values A, B, and C are interpreted as representing the lengths of the sides of a triangle. <br>
The program then prints a message to the standard output that states whether the triangle, if it can be formed, is scalene, isosceles, equilateral, or right angled.<br>
Determine the following for the above program:<br>
<br>

**a) Identify the equivalence classes for the system<br>**

Equivalence Classes:<br>
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

## Section B:
### 1. Convert the Java code comprising the beginning of the doGraham method into a control flow graph (CFG).
#### -Below is the control flow graph of the converted Java code:

![image](https://user-images.githubusercontent.com/124248015/231727944-ad3e32c1-a94b-4eee-bf16-81c98b735228.png)

### 2. Test sets for the given criteria:

![image](https://user-images.githubusercontent.com/124248015/231728203-a5db4283-0596-4f6f-8b42-05c70f21edd9.png)









