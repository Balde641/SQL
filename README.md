# SQL

12. SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä FROM Kurssi, Tehtävä,Kurssitehtävä WHERE Kurssi.kurssitunnus = kurssitehtävä.kurssi (ei ole valmis)

13. SELECT Kurssi.nimi,Tehtävä.nimi FROM Opiskelija, Tehtävä,Kurssitehtävä, Tehtäväsuoritus WHERE Opiskelija.opiskelija=Tehtäväsuoritus,opiskelija AND Tehtäväsuoritus.tehtävä=Kurssitehtävä.tunnus AND Tehtävä.tunnus Opiskelija='Anna'

13.SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä FROM Kurssi,Kurssitehtävä, Opiskelija, Kurssisuoritus
WHERE Opiskelija.nimi = 'Anna'
AND Opiskelija,opiskelijanumero = Kurssisuoritus.opiskelija
AND Kurssi, kursstunnus=
