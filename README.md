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

## <kbd>SELECT</kbd>

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
