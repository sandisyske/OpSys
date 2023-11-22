# Praktikum 9 - Ressursihaldus
|  Küsimus 	|  Linux 	|  Windows 	|   Linuxis kasutatud käsklus	|   Windowsis kasutatud käsklus	|
|---	|---	|---	|---	|---	|
|  Mitu protsessi kokku arvutis käib? 	|  210	|  135 	|   ```ps aux \| wc -l```	|  Tegumihaldur -> Jõudlus 	|
|  Milline on kõige esimesena käivitatud protsess? 	|   /sbin/init splash	|  Registry 	|   `ps -eo pid,ppid,cmd,start --sort=start`	|  Process Explorer -> Process -> Sorteerimine Start Time järgi	|
|   Milliste kasutajate protsesse arvutis käib? 	|   Kasutaja Sandra protsessid (kokku 205)	|   Arvutis töötavad kasutajatest ainult Sandra protsessid (kokku 41 protsessi)	|   `top -u sandra`	|   Process Explorer -> Own Processes	|
|   Kui kaua on arvuti järjest töötanud (up time)?	|   01:05:29	|  0:00:59:12 	|   `htop` -> Uptime	|   Tegumihaldur -> Jõudlus -> CPU -> Tööaeg	|
|   Milline protsess käivitati kõige hiljem (viimasena)? 	|   root        3518  0.0  0.0      0     0 ?        I    21:21   0:00 [kworker/u4:0]	|  MoNotificationUx.exe 	|   `sudo ps axu`	|   Process Explorer -> Process -> Sorteerimine Start Time järgi alustades kõige hilisemast	|
|   Milline on kõige rohkem protsessoriaega võttev protsess?	|   /usr/bin/gnome-shell	|   System Idle Process (1:07:37.406)	|   `ps aux --sort=-%cpu \| head -n 2` |   Process Explorer -> Process -> Sorteerimine CPU Time järgi	|
|   Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess?	|   /usr/bin/gnome-shell	|   msedge.exe (3 433 078 500K)	|   `ps aux --sort=-vsz \| head -n 2`	|  Process Explorer -> sorteerimine Virtual size 	|
|   Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?	|   /usr/bin/gnome-shell	|   MsMpEng.exe (201 366 K)	|   `ps aux --sort=-rss \| head -n 2`	|  Process Explorer -> Working Set Size sorteerimine 	|
|   Kui palju füüsilisest mälust (Physical Memory) on vaba?	|   300Mi ehk 300 MB	|   Vaba on 1,5 GB (Kasutusel on Physical Usage on 56,98% kontrollides Process Explorer'ist 	|   `free -h \| awk '/^Mem:/ {print $4}'`	|   Tegmuhaldur -> Jõudlus -> Mälu -> Saadaval	|
|  Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt? 	|   Vaba ruumi on 11 GB ja protsentuaalselt on 46%	|  Vaba ruumi on 34,97 GB  ning protsentuaalselt 55%	|  `df -h /` 	|   Kettahaldus -> Vaba ruum ja % vaba    |
|  Milline on kõige suurem kõvakettal olev fail ja kõige suurem alamkaust? 	|  Suurim fail: /var/lib/snapd/snaps/gnome-42-2204_141.snap (497 MB) ning suurim alamkaust: /usr	|  Suurim fail pagefile.sys (1,4 GB) ja suurim alamkaust Windows (19,2 GB, 61846 alamkataloogi)|   Suurima faili `find / -type f -exec du -h --max-depth=1 {} + \| sort -rh \| head -n 1` ja alamkausta leidmiseks `du -h --max-depth=1 / \| sort -rh \| head -n 2` |   WinDirStat -> <failid> ja kaustad -> sorteerimine Suurus	|
|   Uurige, millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral. (pilt on peale tabelit)	|   Enim protsessori kasutus on kasutaja protsesside (us) peal (70,8%), ja süsteemi protsesside (sy) peal (29,2%)	|  x 	|   `top`	|   x	|
|   Milline protsess kõige rohkem salvestusseadmele kirjutab?	|   x	|   System (139 301 B/s)	|   x	|   Resource Monitor -> Disk -> Write(B/sec)	|
|   Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab?	|   x	|  C:\swapfile.sys 	|   x	|  Resource Monitor -> Disk -> Write(B/sec)	|
|  Milline protsess kõige rohkem salvestusseadmelt loeb? 	|   x	|   mmc.exe (1 446 B/s)	|  x 	|  Resource Monitor -> Disk -> Read(B/sec)	|
|   Millisest failist eelmise küsimuse protsess kõige rohkem loeb?	|   x	|  C:\Windows\System32\logoncli.dll	|   x	|  Resource Monitor -> Disk -> Read(B/sec)	|
|   Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? (pilt peale tabelit)	|   x	|  Suurim nextcloud.exe - kohalik IP-aadress: 10.0.2.15, kohalik port: 50805, ühenduse teise poole IP-aadress: 193.40.5.90, port: 443, latents: 0 ms ja antud ühenduse poolt kasutatav võrguliikluse kogumaht: 138 B/sekundis. 	|   x	|   Resource Monitor -> Network 	|
|   Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme või käsureakäske kasutad põhjustaja tuvastamiseks.	|  x	| Seadetest saab kontrollida, kas driverid on uuendatud ning vähendada Startupi käivituvaid programme. Antiviirusega saab teha viiruste kontrolli ning vajadusel teha arvutile puhastust (kustutada cache faile), Tegumihaldurist saab jälgida programme mis kasutavad palju mälu või CPU ruumi, Resouce Monitorist saab jälgida mis protsessid kasutavad palju kettaruumi ning võrku   	|   x	|   Seaded, Taskmanager/Tegumihaldur, Resouce Monitor, Antivirus	|

### 9.12 Linuxi CPU alamtegevused
![image](https://github.com/sandisyske/OpSys/assets/120086951/369b522d-6fce-47e0-b15f-6e2d228ea0c3)


### 9.14 Windows Resource Monitor Network 
<img width="691" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/fa7af8f6-0665-4140-8803-321028c25531">

