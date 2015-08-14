Source: [SQL_Basic](http://sqlzoo.net/wiki/SELECT_basics)

Show the population of Germany
```
SELECT population FROM world
  WHERE name = 'Germany'
```

Show the name and per capita gdp: gdp/population for each country where the area is over 5,000,000 km2
```
SELECT name, gdp/population FROM world
  WHERE area > 5000000
```

Show the name and continent where the area is less than 2000 and the gdp is more than 5000000000
```
SELECT name , continent
  FROM world
  WHERE area < 2000
    AND gdp > 5000000000
```

Show the name and the population for 'Denmark', 'Finland', 'Norway', 'Sweden'
```
SELECT name, population FROM world
  WHERE name IN ('Finland', 'Norway', 'Sweden',
                 'Denmark')
```

Show each country that begins with G
```
SELECT name FROM world
  WHERE name LIKE 'G%'
```

Show the area in 1000 square km. Show area/1000 instead of area
```
SELECT name, area/1000 FROM world
  WHERE area BETWEEN 200000 AND 250000
```

