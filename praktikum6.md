# Praktikum 6 - protsessid ja signaalid

### Ülesanne 6.1

Käivita gedit käsurealt, nüüd peata programmi töö ajutiselt klahvikombinatsiooniga CTRL+Z, veendu, et gediti aken on hangunud, seejärel saada talle SIGCONT-signaal ning veendu, et gediti aken toimib jälle. Pane oma aruandesse ekraanitõmmis käskude käivitamisest oma terminaliaknas.


![image](https://github.com/sandisyske/OpSys/assets/120086951/91b546ba-8fb5-49d7-aed8-a849fdd86aa0)


### Ülesanne 6.2

Käivita gedit taustal &-võtmega, saada sellele SIGHUP-signaal ja veendu, et aken sulgus. Seejärel käivita gedit nohup-käsuga, saada sellele uuesti SIGHUP-signaal ning veendu, et gedit jääb käima. Nüüd sisesta käsk, millega saad nohupi käivitatud gediti protsessi sulgeda. Pane oma aruandesse ekraanitõmmis käskude käivitamisest oma terminaliaknas, sh tõestuseks protsessi kadumise või allesjäämise kohta ps-käsu väljund.


![image](https://github.com/sandisyske/OpSys/assets/120086951/0fd70f7f-3616-433f-9a67-f942c00fa3c7)


### Ülesanne 6.3

Koosta ja lisa aruandesse käsujada, mis kuvab (modifitseerib) käsu ps -axu | grep daemon väljundi nii, et tulemuseks oleksid ainult programminimed koos lisaparameetritega (näiteks avahi-daemon: running [Perenimi-U22.local])


![image](https://github.com/sandisyske/OpSys/assets/120086951/bc4899da-2476-49cd-93af-d518aa028d37)


### Ülesanne 6.4

Koosta ja lisa aruandesse käsujada (ip a | grep ...| ... | cut ... jne), mis kuvab ekraanile vastuseks ainult arvuti IP-aadressi (enamasti 10.0.2.15) ip a-käsu väljundi põhjal. 


1. ps -axu | grep snap | cut -c68- (Otsin snap read)
2. ip a | grep inet | tail -n+3 | head -n 1 | cut -d " " -f 6 | cut -d "/" -f 1 (väljastan IP aadressi)
3. ip a | grep inet | tail -n+3 | head -n 1 | cut -d " " -f 6 | cut -d "/" -f 1 > ipaddress.txt (salvestasin IP aadressi tekstifaili)
4. xargs -n1 ping -c 2 < ipaddress.txt (Kontrollisin tulemust)

Viimasest neljast tegumist snapshotid

<img width="322" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/b31b4af4-9d11-4ecc-a7e0-491badb2751e">
<img width="515" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/fa70aed5-4a37-4b5c-a55f-139fbccfe3b5">

