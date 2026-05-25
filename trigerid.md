## Triger - trigger -päästik
### Triger - andmebaasi objekt, mis käivitub automaatselt, kui toimub teatud sündmus (nt INSERT, UPDATE, DELETE).
Trigerite loomine - automatseerub protsessid SQL Serveris.

Tabelid mis tuleb luua enna trigerit!
```sql
Create database trigerLogitpe24;

use trigerLogitpe24;
CREATE TABLE linnad(
linnId int primary key identity(1,1),
linnanimi varchar(30) unique,
maakond varchar(50),
rahvaarv int);
select * from linnad;
INSERT INTO linnad(linnanimi, maakond, rahvaarv)
VALUES ('Tallinn', 'Harjumaa', 600000);

--tabel logi - tabel, mis täidab triger, kui kasutaja täidab tabeli linnad!
CREATE TABLE logi(
id int primary key identity(1,1),
kasutaja varchar(50),
aeg DATETIME,
andmed TEXT);
```

```sql
CREATE TRIGGER linnaLisamine
ON linnad -- tabel, mida triger jälgib
FOR INSERT
AS
INSERT INTO logi(kasutaja, aeg, andmed)
SELECT 
SYSTEM_USER, --siselogitud user
GETDATE(), 
CONCAT('lisatud: ',inserted.linnanimi,', ',
inserted.maakond,', ',inserted.rahvaarv)
FROM inserted;

--kontrollimiseks tuleb lisada linna tabelisse linnad
INSERT INTO linnad(linnanimi, maakond, rahvaarv)
VALUES ('Viljandi', 'Viljandimaa', 50000);

SELECT * FROM linnad;
SELECT * FROM logi;
```
<img width="646" height="367" alt="{25A079C5-3DA9-44AC-9D57-12F5D476D956}" src="https://github.com/user-attachments/assets/94aa5c38-af20-4b96-bf10-1ca58a771990" />

