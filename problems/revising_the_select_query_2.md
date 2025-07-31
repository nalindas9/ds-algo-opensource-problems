Query the NAME field for all XYZ cities in the CITY table with populations larger than 120000. The CountryCode for XYZ is XYZ.
The CITY table is described as follows:


![1449729804-f21d187d0f-CITY-2](https://github.com/user-attachments/assets/753d85e4-7854-4c91-9423-f2e75244c7f5)

```
SELECT NAME
FROM CITY
WHERE COUNTRYCODE = 'XYZ' AND POPULATION > 120000;
```
