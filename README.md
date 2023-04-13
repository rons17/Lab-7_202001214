# Lab-7_202001214
# Software Engineering IT314

## Section A:
### 1) Consider a program for determining the previous date. Its input is triple of day, month and year with the following ranges 1 <= month <= 12, 1 <= day <= 31, 1900 <= year <= 2015.The possible output dates would be previous date or invalid date. Design the equivalence class test cases?
#### - Following are the equivalence class according to given input
#### i) Valid dates: The input triple (day, month, year) that represent a valid date in the Gregorian calendar, such as (3, 11, 1999).
#### ii) Invalid dates: The input triple (day, month, year) that represent an invalid date, such as (30, 2, 2020) or (31, 4, 1967).
#### iii) Out of range dates: The input triple (day, month, year) that are outside the allowed ranges, such as (0, 8, 2030) or (18, 13, 2012). 
#### -Based on these equivalence classes, we can design the following test cases:
![image](https://user-images.githubusercontent.com/124248015/231714811-2fe1ca2c-b52c-46d4-a894-339c40a34322.png)

![image](https://user-images.githubusercontent.com/124248015/231714994-9b80e6ce-71af-49c1-ab68-5041beacd927.png)

![image](https://user-images.githubusercontent.com/124248015/231715072-1ae9c0bb-d5f6-4b29-a984-295fad7d456e.png)

### Boundary Value Analysis:
#### Using boundary value analysis, we can identify the following boundary test cases:
#### 1)The earliest possible date: (1, 1, 1900)
#### 2)The latest possible date: (31, 12, 2015)
#### 3)The earliest day of each month: (1, 1, 2000), (1, 2, 2000), (1, 3, 2000),..., (1, 12, 2000)
#### 4)The latest day of each month: (31, 1, 2000), (28, 2, 2000), (31, 3, 2000),..., (31, 12, 2000)
#### 5)Leap year day: (29, 2, 2000)
#### 6)Invalid leap year day: (29, 2, 1900)
#### 7)One day before earliest date: (31, 12, 1899)
#### 8)One day after latest date: (1, 1, 2016)
#### -Based on these boundary test cases, we can design the following test cases:
#### Tester Action and Input Data Expected Outcome

![image](https://user-images.githubusercontent.com/124248015/231716947-467eb77a-1272-469f-b889-6f8b4285e910.png)
## Programs for testing:
### Program 1:
![image](https://user-images.githubusercontent.com/124248015/231719171-0090581f-96ec-4935-be95-132f4d932128.png)

![image](https://user-images.githubusercontent.com/124248015/231719307-2fb37807-67c4-4c88-8c8b-28f68e621715.png)

### Program 2:

![image](https://user-images.githubusercontent.com/124248015/231719536-0865c0b9-1b18-4a12-b9a2-ad0c9dd2614b.png)

### Program 3:

![image](https://user-images.githubusercontent.com/124248015/231719689-1b944685-13fa-4b0e-9b51-5b1a7a4cbd9a.png)

![image](https://user-images.githubusercontent.com/124248015/231719758-03d11b42-3de7-49b0-b7af-a231a03ab52a.png)

### Program 4: 

![image](https://user-images.githubusercontent.com/124248015/231719897-00148f07-2c1f-46e2-a406-1e854d0b7486.png)

![image](https://user-images.githubusercontent.com/124248015/231719961-853b5327-ca90-4b32-af70-fc1171e1d39f.png)

### Program 5:

![image](https://user-images.githubusercontent.com/124248015/231720045-d70de9ef-404f-4109-bbec-2e8a430e5f2d.png)

![image](https://user-images.githubusercontent.com/124248015/231720172-6edc0b87-3b37-4e93-adb4-14ccb4afe974.png)


### Program 6:

![image](https://user-images.githubusercontent.com/124248015/231720277-fd1e4ab1-119d-4a80-951e-f8bab0757d01.png)

![image](https://user-images.githubusercontent.com/124248015/231720363-74c6ca8a-93fa-479a-b42f-d16dd2bbacb7.png)

![image](https://user-images.githubusercontent.com/124248015/231720435-c95b799e-946d-487d-8cfb-93fbd22df929.png)

## Section B:

### 1) Convert the Java code comprising the beginning of the doGraham method into a control flow graph (CFG):
#### -Below is the control flow graph of the converted Java code.

![image](https://user-images.githubusercontent.com/124248015/231724701-1218e2d3-f378-48cc-80fb-e44b6c391846.png)

### 2) Test sets for the given criteria:

![image](https://user-images.githubusercontent.com/124248015/231725169-c6d35cc7-dc68-4d90-b2f5-c059d7bffe50.png)











