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

11. Tehtävä: SELECT DISTINCT nimi, päivämäärä, arvosana FROM Opiskelija, Kurssisuoritus    #ei ole oikein vielä


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
    WHERE k.kurssitunnus = kt.kurssi GROUP BY k.nimi                                #ei oikein vielä


17. tehtävä:
SELECT k.nimi AS kurssi, COUNT(ks.kurssi) as lukumäärä FROM Kurssi k LEFT JOIN Kurssisuoritus ks
    ON k.kurssitunnus = ks.kurssi GROUP BY k.nimi

18. tehtävä:

19. tehtävä:

20. tehtävä:

21. tehtävä:

22. tehtävä:

23. tehtävä:

24. tehtävä:

25. tehtävä:

26. tehtävä:




    
