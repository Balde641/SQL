# SQL
4. Tehtävä: SELECT * FROM Kurssisuoritus

5. Tehtävä: SELECT kurssi FROM Kurssisuoritus

6. Tehtävä: SELECT DISTINCT kurssi FROM Kurssisuoritus

7. Tehtävä: SELECT * FROM Opiskelija WHERE nimi = 'Anna'

8. Tehtävä:

9. Tehtävä: SELECT pääaine FROM Opiskelija WHERE pääaine NOT LIKE '%tiede%'

10. Tehtävä: SELECT nimi, päivämäärä, arvosana
 FROM Opiskelija, Kurssisuoritus
 WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija

11. Tehtävä: SELECT DISTINCT nimi, päivämäärä, arvosana FROM Opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija


12. Tehtävä: SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä 
FROM Kurssi, Kurssitehtävä, Tehtävä, Tehtäväsuoritus, Opiskelija 
WHERE Kurssi.kurssitunnus = kurssitehtävä,kurssi 
AND Tehtävä.tunnus = Kurssitehtävä,tehtävä
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä,tunnus
AND Tehtäväsuoritus.opiskelija = Opiakelija.opiskelijanumero
AND Opiakelija.nimi = 'Anna'
 

13. Tehtävä: SELECT Kurssi.nimi AS Kurssi, Tehtävä.nimi AS Tehtävä 
FROM Kurssi, Kurssitehtävä, Tehtävä, Tehtäväsuoritus, Opiskelija
WHERE Kurssi.kurssitunnus = Kurssitehtävä.kurssi
AND Tehtävä.tunnus = Kurssitehtävä.tehtävä
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus
AND Tehtäväsuoritus.opiskelija = Opiskelija.opiskelijanumero
AND Opiskelija.nimi = 'Anna'

14. Tehtävä: 

Ensimmäisessä koodissa etsitään tehtävä nimikkeitä, toisessa eri oppilas nimiä joilla on annettu tehtävä, 
koska oppilaita on enemmän kuin tehtäviä, vaikuttaa listan kokoon.

15. tehtävä:
SELECT nimi FROM Kurssi k
    WHERE k.kurssitunnus
        NOT IN (SELECT kurssi FROM Kurssitehtävä)
        
        
Toinen vaihtoehtoa 15. tehtävävlle:
SELECT nimi FROM Kurssi k
    LEFT JOIN Kurssitehtävä t
    ON k.kurssitunnus = t.kurssi
    WHERE t.tunnus IS NULL
    
16. tehtävä:
SELECT k.nimi AS kurssi, COUNT(kt.tunnus) lukumäärä FROM Kurssi k, Kurssitehtävä kt
    WHERE k.kurssitunnus = kt.kurssi GROUP BY k.nimi                                        #ei oikein vielä


17. tehtävä:
SELECT k.nimi AS kurssi, COUNT(ks.kurssi) as lukumäärä FROM Kurssi k LEFT JOIN Kurssisuoritus ks
    ON k.kurssitunnus = ks.kurssi GROUP BY k.nimi

18. tehtävä: CREATE TABLE Kurssi2(kurssitunnus, nimi, kuvaus)  

19. tehtävä: 
INSERT INTO Kurssi (kurssitunnus, nimi, kuvaus)
   VALUES ("12345", "SQL-kielen perusteet", "SELECT 'Hei maailma'.")

20. tehtävä:
CREATE TABLE Kurssi3(tehtävä, kurssitunnus);
PRAGMA TABLE_INFO(tehtävä)

21. tehtävä:
CREATE TABLE Kurssi4 (kurssitunnus, nimi, kuvaus)
tarkistus:
PRAGMA TABLE_INFO(Kurssi4)

22. tehtävä: SELECT * FROM Opiskelija

23. tehtävä: CREATE TABLE Kurssi5 (kurssitunnus, nimi, kuvaus)

24. tehtävä:
PRAGMA foreign_keys = ON;

CREATE TABLE Kurssi6 (
    kurssitunnus integer PRIMARY KEY,
    nimi varchar(200) NOT NULL,
    kuvaus varchar(3000)
);

INSERT INTO Kurssi (nimi) VALUES ('Ohpe');
INSERT INTO Kurssi (nimi) VALUES ('Tikape');

25. tehtävä:
PRAGMA foreign_keys = ON;

CREATE TABLE Kurssi7 (
    kurssitunnus integer PRIMARY KEY,
    nimi varchar(200) NOT NULL,
    kuvaus varchar(3000)
);

INSERT INTO Kurssi (nimi) VALUES ('Ohpe');
INSERT INTO Kurssi (nimi) VALUES ('Tikape');

26. tehtävä: ALTER TABLE -käskyä käytetään olemassa olevan taulukon sarakkeiden lisäämiseen, poistamiseen tai muokkaamiseen.

ALTER TABLE -käskyä käytetään myös lisäämään ja pudottamaan olemassa olevan taulukon erilaisia rajoituksia.




    
