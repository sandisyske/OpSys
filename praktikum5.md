# Praktikum 5 - 

### Ülesanne 5.1
Katsetage missuguseid minimaalseid õigusi (r,w,x) on Unixis omanikul (u) vaja (/tmp/kaust - directory, minufail.txt - fail) (Grupile ja teistele ei anna mitte mingeid õiguseid). Minimaalsed õigused tuua välja eraldi nii kataloogi kui faili kohta:

a) kataloogis /tmp/kaust oleva faili minufail.txt lugemiseks?
Esiteks /tmp/kaust lugemiseks on minimaalselt vaja õigusi u=x ehk  execute. 
Kui saab vaadata u=rx õigusega kausta sisu, siis on vaja veel lisada failile lugemis õigus, et kuvada faili sisu, ehk chmod u=r /tmp/kaust/minufail.txt
b) kataloogis /tmp/kaust oleva faili minufail.txt kustutamiseks?
Kustutamiseks on vaja lisada kaustale õigused u=rx ning tekstifailile lisada õigus u=r


### Ülesanne 5.2


### Ülesanne 5.3
