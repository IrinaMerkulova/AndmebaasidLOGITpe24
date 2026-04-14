# AndmebaasidLOGITpe24
Andmebaasidega seotud sql kood ja konspektid

- SQL - structured Query Language - struktureeritud päringukeel
- DDL - Data Definition Language -andmebaasi struktuuri loomiseks - CREATE, ALTER
- DML - Data Manipulation Language -andmete lisamine ja uuendamine tabelis - INSERT, UPDATE, DELETE


### tunnis me kasutame andmebaasihaldusüsteemid:
1. SQL Server Management Stuudio (SQL Serveri haldamiseks)
   <img width="472" height="502" alt="{81ABDF60-8DD9-458A-B7D2-DCEB363321E1}" src="https://github.com/user-attachments/assets/fb13b99d-4abb-4280-9fdf-af8ffdacec1a" />

2. XAMPP -phpmyAdmin (mariaDB andmebaas) -vabavara

   ## Põhimõisted

- Andmebaas - struktueeritud andmete kogum
- Tabel - olem (entity)
- veerg - väli (field)
- rida - kirje (record)
- primaarne võti -PK- Primary Key - veerg (tavaliselt nimega id) unikaalse identifikaatooriga, mis eristab iga kirjet
- Välisvõti (võõrvõti) -FK Foreign Key - veerg, mis loob seose teise tabeli primaarvõtmega.

  ## Andmetüübid
  - INT, float, decimal(6,2) - numbrilised
  - varchar(50), char(6) -tekst/sümboolid
  - boolean, bool, bit -loogiline tüüp
  - date, time, datetime - kuupäeva
 
## Piirangud
```
1. Primary Key
2. Foreign Key
3. Unique
4. Not Null
5. Check
```
## Tabelivahelised Seosed
- üks  - ühele (nt mees --naine)
- üks - mitmele (õpilane käib erinevates õppeainetes)
  <img width="350" height="150" alt="{979F53E1-7365-40EE-BC26-CBFE1A45E637}" src="https://github.com/user-attachments/assets/33209fb4-d37e-4f77-82c5-e57f0c427d89" />

- mitu - mitmele (nt õpilane - õpetaja)

  
