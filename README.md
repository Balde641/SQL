# SQL

12. SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä 
FROM Kurssi, Kurssitehtävä, Tehtävä, Tehtäväsuoritus, Opiskelija 
WHERE Kurssi.kurssitunnus = kurssitehtävä,kurssi 
AND Tehtävä.tunnus = Kurssitehtävä,tehtävä
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä,tunnus
AND Tehtäväsuoritus.opiskelija = Opiakelija.opiskelijanumero
AND Opiakelija.nimi = 'Anna'
 

13. SELECT Kurssi.nimi,Tehtävä.nimi FROM Opiskelija, Tehtävä,Kurssitehtävä, Tehtäväsuoritus WHERE Opiskelija.opiskelija=Tehtäväsuoritus,opiskelija AND Tehtäväsuoritus.tehtävä=Kurssitehtävä.tunnus AND Tehtävä.tunnus Opiskelija='Anna'

13.SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä FROM Kurssi,Kurssitehtävä, Opiskelija, Kurssisuoritus
WHERE Opiskelija.nimi = 'Anna'
AND Opiskelija,opiskelijanumero = Kurssisuoritus.opiskelija
AND Kurssi, kursstunnus=
