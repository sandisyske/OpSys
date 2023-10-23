# Praktikum 5 - Failiõigused Linuxis
Selle praktikumi läbimiseks kulus kokku 6 tundi. Oli väga palju ise otsimist ja materjali lugemist. 

### Ülesanne 5.1
Katsetage missuguseid minimaalseid õigusi (r,w,x) on Unixis omanikul (u) vaja (/tmp/kaust - directory, minufail.txt - fail) (Grupile ja teistele ei anna mitte mingeid õiguseid). Minimaalsed õigused tuua välja eraldi nii kataloogi kui faili kohta:

a) kataloogis /tmp/kaust oleva faili minufail.txt lugemiseks?

Esiteks /tmp/kaust lugemiseks on minimaalselt vaja õigusi u=x ehk  execute. 
Kui saab vaadata u=rx õigusega kausta sisu, siis on vaja veel lisada failile lugemis õigus, et kuvada faili sisu, ehk chmod u=r /tmp/kaust/minufail.txt

b) kataloogis /tmp/kaust oleva faili minufail.txt kustutamiseks?

Kustutamiseks on vaja lisada kaustale õigused u=rx ning tekstifailile lisada õigus u=r


### Ülesanne 5.2
Miks chmod a=x skriptifail ei ole piisav õigus shelli skriptifaili käivitamiseks? Millist õigust lisaks käivitamisele veel vaja läheb skriptifaili käivitamiseks? Põhjendage lühidalt.

chmod a=x ei ole enam piisav skriptifaili käivitamiseks, sest isegi kui meil on execute õigus ei saa me skripti sisu kuvada ilma read õiguseta.

### Ülesanne 5.3
Miks on igal kasutajal omanimeline grupp?

Igale kasutajale luuakse omanimeline grupp, et ei tekiks olukorda, kui teised kasutajad saaksid üle kirjutada või kustutada mitte nende loodud faile. Samuti on võimalik omanimelistes gruppides muuta umaski väärtusi nii, nagu kasutaja ise soovib.


### Ülesanne 5.4
Millised on minimaalsed õigused (rwx), mis on vajalikud teie tavakasutajal (kuulub gruppi majasisene) (mitte root- või peeter-kasutajal, kausta ja faili omanikud) faili uusfail.txt sisu kuvamiseks? Esitage ekraanivaade käskude id, ls -la ja cat uusfail.txt väljundist, tõestamaks lahendust.

uusfail.txt = tekst.txt
Tavakasutaja kuulub gruppi majasisene ning et tavakasutaja saaks faili tekst.txt lugeda peab olema tekstifailile lisatud õigus g=r, ehk gruppi kuuluvad isikud saaksid faili lugeda.

Tõestusmaterjal
![image](https://github.com/sandisyske/OpSys/assets/120086951/165b80d2-c69e-48ad-878b-d2019aea1b06)


### Ülesanne 5.5
 Tehke kuvatõmmis tulemusest, kus oleks näha faili hinded.txt õigused ja jukuisa käivituskäsk koos väljundiga, ning lisage see oma esitusele. Milleks on vaja setuid-õigust?
 Setuid-õigust on vaja, et omanikest erinevad kasutajad saaksid käivitada programme või skripte, ilma muude õigusteta.

Tõestusmaterjal
![image](https://github.com/sandisyske/OpSys/assets/120086951/cc7278c5-2082-43fd-8e4c-488115951719)


### Ülesanne 5.6
 Kas setuid-i kasutamine võib vähendada süsteemi turvalisust? Kui jah, siis kuidas?
 Setuid kasutamine võib vähendada süsteemi turvalisust, oleneb kuidas seda kasutatud on. Programm või skript millel on setuid lisatud peab olema hoolikalt läbi mõeldud ning turvaline. Näiteks kui programmi või skripti jooksutatakse root õigustega siis on võimalik teisel kasutajal saada läbi selle ligipääs süsteemi.


 ### Ülesanne 5.7
 Kirjutage oma esitusele kõik kasutajad, kes saavad sticky bit-õigustega yhiskaust-kataloogist nüüd peeter-kasutaja loodud faile kustutada. (Õige vastus sisaldab vähemalt 3 eri kasutajat).
 root, peeter, ja sandra


 ### Ülesanne 5.8
 Seejärel uurige õigusi täpsemalt, kasutades käsku getfacl, ning kopeerige see tulemus oma esitusele.
tulemus mis sain kasutades getfacl hinded.txt

peeter@erik-U23:/home/opetaja/klass$ getfacl hinded.txt

 file: hinded.txt
 
 owner: opetaja
 
 group: opetaja
 
user::rw-

group::---

group:direktor:rw-

mask::rw-

other::---


 ![image](https://github.com/sandisyske/OpSys/assets/120086951/b1bbc6d3-1b1a-4ca1-b0ec-247805a63a8a)


 ### Ülesanne 5.9
 Kes saab chattr +i-parameetriga faili sisu modifitseerida (kirjutada)? Milliste käskudega saate kustutada testfail-2-nimelise faili (ehk kuidas siiski kustutada +i-parameetriga faili).

 Chattr +i parameetriga faili sisu ei saa mitte keegi muuta, parameetrit saab eemaldada ainult superuser.
 testfail-2 saab kustutada järgmiseid käske:
 sudo chattr -i testfail-2
 rm testfail-2

 
