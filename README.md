# Simple SQL Queries

## Create Tables

### Statement
```sql
CREATE TABLE DEPT (
    deptNo,
    dName,
    loc
) AS SELECT * FROM DEMO_DEPTEMP.DEPT;

CREATE TABLE EMP (
    empNo,
    eName,
    job,
    mrg,
    hireDate,
    sal,
    comm,
    deptNo
) AS SELECT * FROM DEMO_DEPTEMP.EMP;

CREATE TABLE SALGRADE (
    grade,
    losal,
    hisal
) AS SELECT * FROM DEMO_DEPTEMP.salgrade;

```


### Result
![](./img/result1.png)

## Naming columns in a result set

### Statement

```sql
SELECT DNAME DepName FROM DEPT;
```

### Result
![](./img/result2.png)

## Removing duplicate records
### Statement
```sql
SELECT DISTINCT job FROM EMP;
```

### Result
![](./img/result3.png)

## Date Format

### Statement
```sql
SELECT EMPNO, ENAME, TO_CHAR(HIREDATE, 'DD.MONTH YYYY') FROM EMP;
```

### Result

![](./img/result4.png)

## Date Calculations

### Statement
```sql
SELECT ENAME, CURRENT_DATE - HIREDATE DAYS FROM EMP;
```

### Result
![](./img/result4.png)

## Upper bounds

### Statement
```sql
SELECT MAX(SAL) FROM EMP;
```

### Result
![](./img/result7.png)

## Lower bounds

### Statement
```sql
SELECT MIN(SAL) FROM EMP;
```

### Result
![](./img/result6.png)


## Average

### Statement
```sql
SELECT AVG(SAL) FROM EMP;
```

### Result
![](./img/result8.png)

## Simple Counting

### Statement
```sql
SELECT COUNT(EMPNO) FROM EMP;
```

### Result

![](./img/result9.png)

## Counting unique Results

### Statement

```sql
SELECT COUNT(DISTINCT JOB) FROM EMP;
```

### Result

![](./img/result10.png)




