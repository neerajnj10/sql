Source: [Noble_sql](http://sqlzoo.net/wiki/SELECT_from_Nobel_Tutorial)

Change the query shown so that it displays Nobel prizes for 1950.
```
SELECT yr, subject, winner
  FROM nobel
 WHERE yr = 1950
```

Show who won the 1962 prize for Literature.
```
SELECT winner
  FROM nobel
 WHERE yr = 1962
   AND subject = 'Literature'
```

Show the year and subject that won 'Albert Einstein' his prize.
```
SELECT yr, subject
  FROM nobel
 WHERE winner='Albert Einstein'
```

Give the name of the 'Peace' winners since the year 2000, including 2000.
```
SELECT winner
  FROM nobel
 WHERE yr>1999 AND subject ='Peace'
```

Show all details (yr, subject, winner) of the Literature prize winners for 1980 to 1989 inclusive.
```
SELECT yr, subject, winner
  FROM nobel
 WHERE subject = 'Literature' AND yr>1979 AND yr<1990
```

Show all details of the presidential winners:

Theodore Roosevelt
Woodrow Wilson
Jimmy Carter
```
SELECT * FROM nobel
 WHERE winner IN ('Theodore Roosevelt','Woodrow Wilson', 'Jimmy Carter')
```

Show the winners with first name John
```
SELECT winner FROM nobel 
WHERE winner LIKE 'John%'
```

