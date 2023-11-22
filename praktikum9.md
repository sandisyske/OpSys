# Praktikum 9 - Ressursihaldus
|  Küsimus 	|  Linux 	|  Windows 	|   Linuxis kasutatud käsklus	|   Windowsis kasutatud käsklus	|
|---	|---	|---	|---	|---	|
|  Mitu protsessi kokku arvutis käib? 	|   	|  135 	|   	|  Tegumihaldur -> Jõudlus 	|
|  Milline on kõige esimesena käivitatud protsess? 	|   	|  Registry 	|   	|  Process Explorer -> Process -> Sorteerimine Start Time järgi	|
|   Milliste kasutajate protsesse arvutis käib? 	|   	|   Arvutis töötavad kasutajatest ainult Sandra protsessid (kokku 41 protsessi)	|   	|   Process Explorer -> Own Processes	|
|   Kui kaua on arvuti järjest töötanud (up time)?	|   	|  0:00:59:12 	|   	|   Tegumihaldur -> Jõudlus -> CPU -> Tööaeg	|
|   Milline protsess käivitati kõige hiljem (viimasena)? 	|   	|  MoNotificationUx.exe 	|   	|   Process Explorer -> Process -> Sorteerimine Start Time järgi alustades kõige hilisemast	|
|   Milline on kõige rohkem protsessoriaega võttev protsess?	|   	|   System Idle Process (1:07:37.406)	|   	|   Process Explorer -> Process -> Sorteerimine CPU Time järgi	|
|   Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess?	|   	|   	|   	|   	|
|   Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?	|   	|   	|   	|   	|
|   Kui palju füüsilisest mälust (Physical Memory) on vaba?	|   	|   	|   	|   	|
|  Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt? 	|   	|   	|   	|   	|
|  Milline on kõige suurem kõvakettal olev fail ja kõige suurem alamkaust? 	|   	|   	|   	|   	|
|   Uurige, millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral. (pilt on peale tabelit)	|   	|  x 	|   	|   x	|
|   Milline protsess kõige rohkem salvestusseadmele kirjutab?	|   x	|   	|   x	|   	|
|   Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab?	|   	|  x 	|   	|  x 	|
|  Milline protsess kõige rohkem salvestusseadmelt loeb? 	|   	| x  	|   	|  x 	|
|   Millisest failist eelmise küsimuse protsess kõige rohkem loeb?	|   	|  x 	|   	|  x 	|
|   Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? (pilt peale tabelit)	|   	|   x	|   	|  x 	|
|   Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme või käsureakäske kasutad põhjustaja tuvastamiseks.	|   	|   x	|   	|   x	|

3. Milliste kasutajate protsesse arvutis käib? (arvesta ka süsteemiprotsesse, mitte ainult sisse logitud kasutajaid)
4. Kui kaua on arvuti järjest töötanud (up time)? (Alternatiivselt võib vastata ka, millal (kuupäev ja kellaaeg) arvuti viimati käima pandi.)
5. Milline protsess käivitati kõige hiljem (viimasena)? (Mitte võtta arvesse programmi, millega seda infot otsida.)
6. Milline on kõige rohkem protsessoriaega võttev protsess?
7. Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess?
8. Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?
9. Kui palju füüsilisest mälust (Physical Memory) on vaba?
10. Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt?
11. Milline on kõige suurem kõvakettal olev fail ja kõige suurem alamkaust?
12. Võrrelge terminali käskude: sha1sum /dev/zero | sha1sum /dev/zero ja
    sha1sum /dev/urandom | sha1sum /dev/urandom protsessori kasutust.
    Võrdluseks avage teine terminaliaken ja top samaaegseks käivitamiseks.
    Uurige, millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral.
    (Ainult Linuxis) Lisa ka ekraanipilt aruande juurde näiteks pärast tabelit.
    Vasta järgnevatele alamküsimustele: (Ainult Windowsis)
  a. Milline protsess kõige rohkem salvestusseadmele kirjutab?
  b. Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab?
  c. Milline protsess kõige rohkem salvestusseadmelt loeb?
  d. Millisest failist eelmise küsimuse protsess kõige rohkem loeb?
13. Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? Vali antud protsessi poolt kasutatavatest
 ühendustest üks ning kirjuta välja järgnev: kohalik IP-aadress, kohalik port, ühenduse teise poole IP-aadress,
port, latents ja antud ühenduse poolt kasutatav võrguliikluse kogumaht. (Ainult Windowsis) Lisa ka ekraanipilt
aruande juurde näiteks pärast tabelit.
14. Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme
  või käsureakäske kasutad põhjustaja tuvastamiseks. Mõlemal juhul kirjuta, mida konkreetselt jälgid
  (nt mis aken, veerud, numbrid jne). (Vali Linuxis või Windowsis)
