# SQL
4. Tehtävä: SELECT * FROM Kurssisuoritus

5. Tehtävä: SELECT kurssi FROM Kurssisuoritus

6. Tehtävä: SELECT DISTINCT kurssi FROM Kurssisuoritus

7. Tehtävä: SELECT * FROM Opiskelija WHERE nimi = 'Anna'

8. Tehtävä:

9. Tehtävä: SELECT * FROM Opiskelija WHERE nimi NOT LIKE '%a%'               #ei ole oikein vielä

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
 

13. Tehtävä: SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä FROM Kurssi,Kurssitehtävä, Opiskelija, Kurssisuoritus
WHERE Opiskelija.nimi = 'Anna'
AND Opiskelija,opiskelijanumero = Kurssisuoritus.opiskelija
AND Kurssi, kursstunnus=
