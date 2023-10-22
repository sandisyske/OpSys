# Praktikum 5 - 

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
