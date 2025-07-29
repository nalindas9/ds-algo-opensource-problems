Query all columns for all  cities in the CITY table with populations larger than 100000. The CountryCode for China is CIN.
The CITY table is described as follows:

![1449729804-f21d187d0f-CITY](https://github.com/user-attachments/assets/ca307a53-97f7-4142-bba3-988592b9e828)


```
SELECT *
FROM CITY
WHERE COUNTRYCODE = 'CIN' AND POPULATION >= 100000;
```
