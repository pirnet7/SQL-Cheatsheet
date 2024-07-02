# Welcome To My SQL-Cheatsheet 👋

## Introduction

### Choose Database:

```
USE Vehicle;
```

### Show all tables:

```
SHOW TABLES;
```

<table>
<tr>
<th>Car</th>
<th>Owner</th>
</tr>
<tr>
<td>

| CarID | Brand       | ConstructionYear |
| ----- | ----------- | ---------------- |
| 1     | Ferrari     | 2001             |
| 2     | Alfa Roemeo | 2023             |
| 3     | Mercedes    | 2015             |
| 4     | BMW         | 2023             |
| 5     | Audi        | 2020             |

</td><td>

| OwnerID | FirstName | LastName | Birthyear |
| ------- | --------- | -------- | --------- |
| 1       | Max       | Meier    | 2002      |
| 2       | Tim       | Weber    | 1998      |
| 3       | Veronica  | Shabid   | 2005      |
| 4       | Alicia    | Davidson | 2002      |
| 5       | Simon     | Schmidt  | 2003      |

</td></tr> 
</table>

## Create

#### Create Database with name Vehicle

```
CREATE DATABASE Vehicle;
```

#### Create Table

```
CREATE TABLE OwnershipHistory (
    OwnershipHistoryID int,
    CarID varchar(255),
    OwnerID varchar(255)
);
```

<table>
<tr>
<th>Car</th>
<th>Owner</th>
<th>OwnershipHistory</th>
</tr>
<tr>
<td>

| CarID | Brand       | ConstructionYear |
| ----- | ----------- | ---------------- |
| 1     | Ferrari     | 2001             |
| 2     | Alfa Roemeo | 2023             |
| 3     | Mercedes    | 2015             |
| 4     | BMW         | 2023             |
| 5     | Audi        | 2020             |

</td><td>

| OwnerID | FirstName | LastName | Birthyear |
| ------- | --------- | -------- | --------- |
| 1       | Max       | Meier    | 2002      |
| 2       | Tim       | Weber    | 1998      |
| 3       | Veronica  | Shabid   | 2005      |
| 4       | Alicia    | Davidson | 2002      |
| 5       | Simon     | Schmidt  | 2003      |

</td><td>

| OwnershipHistoryID | CarID | OwnerID |
| ------------------ | ----- | ------- |
| 1                  | 1     | 3       |
| 2                  | 4     | 3       |
| 3                  | 3     | 1       |
| 4                  | 2     | 4       |
| 5                  | 1     | 4       |

</td></tr> 
</table>

## Read

<kbd>SELECT</kbd>

#### Get everything from table Car:

```
SELECT * FROM Car
```

#### Get Firstname and Lastname from table owner:

```
SELECT FirstName, LastName FROM Car
```

#### Get Firstname as "Name" from table owner:

```
SELECT FirstName as 'Name' FROM Car
```

## <kbd>WHERE</kbd>

#### Get everything from Car with ID=2:

```
SELECT * FROM Car WHERE CarID='2'
```

###

## <kbd>LIKE</kbd>

#### Get every FirstName which contains the letter m/M:

```
SELECT * FROM Owner WHERE FirstName LIKE '%m%'
```

#### Get every FirstName which it's second letter is i:

```
SELECT * FROM Owner WHERE FirstName LIKE '_i%';'
```

#### Get every FirstName which starts with the letter V and ends with the letter a:

```
SELECT * FROM Owner WHERE FirstName LIKE 'v%n';'
```

## <kbd>AND</kbd>

#### Get all Cars with ConstructionYear=2001 OR ConstructionYear=2023:

```
SELECT * FROM Cars WHERE ConstructionYear='2001' OR ConstructionYear='2023';
```

#### Get the Car with Brand='Ferrari' and ConstructionYear=2001

```
SELECT * FROM Car WHERE Brand='Ferrari' AND ConstructionYear='2001';
```

## <kbd>NOT</kbd>

#### Get all Owners except Veronica:

```
SELECT * FROM Owner WHERE NOT FirstName = 'Veronica';
```

## <kbd>MIN/MAX</kbd>

#### Get oldest Owner:

```
SELECT MIN(Birthyear) FROM Owner;
```

#### Get youngest Owner:

```
SELECT MAX(Birthyear) FROM Owner;
```

## <kbd>COUNT</kbd>

#### Count all Cars together:

```
SELECT COUNT(*) FROM Car;
```

## <kbd>SUM</kbd>

#### Count all ConstructionYears together:

```
SELECT SUM(ConstructionYear) FROM Car;
```

## <kbd>AVG</kbd>

#### Get Average of all Birthyear together:

```
SELECT AVG(Birthyear) FROM Owner;
```

## <kbd>BETWEEN</kbd>

#### Get Birthyears BETWEEN 2002 AND 2005:

```
SELECT * FROM Products WHERE Birthyear BETWEEN 2002 AND 2005;
```

## <kbd>ORDER BY</kbd>

#### Order table Owner by Birthyear

```
SELECT * FROM Owner ORDER BY Birthyear;
```

#### Order table Owner by Birthyear descending

```
SELECT * FROM Owner ORDER BY Birthyear DESC;
```

## Update

## Delete

> **© 2024 Pirnet7.**
