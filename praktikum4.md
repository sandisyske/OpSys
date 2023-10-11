# Windowsi seadistus ja turvalisuse praktikum

Selles praktikumis kulus kokku 4,5 tundi. Minule ei tundunud see nii keeruline, kuid leidsin ka endale midagi uut näiteks Windowsi käsureal kaustade tekitamine ja õiguste muutmine. Tegin iga ülesande jaok väikese alapealkirja, et seda oleks hindajal kergem lugeda. Väga palju pilte sai üles laetud.

### Ülesanne 4.1 - Windows update

Minul on kõik asjakohane

<img width="513" alt="op4 1" src="https://github.com/sandisyske/OpSys/assets/120086951/fd9c9fec-acf4-4982-8e63-e6b262403551">

### Ülesanne 4.2 - Windows antivirus

Tõmbasin arvutisse "viiruse" ja siin on logi arvuti tegevusest.

<img width="523" alt="op4 2" src="https://github.com/sandisyske/OpSys/assets/120086951/02fbe5a0-9873-493d-a349-f443b293676b">

### Ülesanne 4.3 - Windows firewall

Ekraanipilt Windows 11 praktikumi virtuaalmasina tülemüüri detailsest seadistamise vaatest

<img width="778" alt="op4 3" src="https://github.com/sandisyske/OpSys/assets/120086951/e554880e-9e76-4e34-8938-7bffd0511787">

### Ülesanne 4.4 - Käsurida kasutaja õigused

Selles ülesandes alguses võrdlesin tavaõiguste kasutusõiguste käsurida administraatori õiguses käsureaga. Hiljem võrdlesin viimast psexec.exe käivitusega käsurida.
Märkasin kuidas õigused järjest kasvasid. Üks võrdlus mille ma välja toon: "Debug programs" mis ei ole võimalik administraatoriõigustega käsurealt. Sellega võib käivitada programme või käsklusi, mis nõuavad sügavamat ligipääsu või protsesside jälgimise võimalust. Kuid sellega võib kaasneda tõsised turvariskid ja süsteemi probleemid, mis tõttu ei ole ka administraatori õigusega sellele ligipääsu.

<img width="963" alt="op4 4" src="https://github.com/sandisyske/OpSys/assets/120086951/4a426726-6b0a-4a0a-89cf-b3b006a0ef90">

### Ülesanne 4.5 - kausta ja failiõigused
Windows cmd on minu jaoks võõras, seega proovisin lahendada seda osa käsurealt.
Lõin uued kasutajad koodiga "net user tootaja1 /add"
Lõin uued kaustad (vastavalt kasutajale) "mkdir C:\OS2023\tootaja1"
Haldasin kausta ligipääsu töötajale, andministraatorile ja enda "Sandra" kontole 
käsuga "icacls C:\OS2023\tootaja1 /grant tootaja1:(OI)(CI)F /grant Administrators:(OI)(CI)F /grant Sandra:(OI)(CI)F"
Edasised kaustaõigused andsin graafilises liideses kausta täpsematest turbesätetest. Ma ei lugenud juhendist välja, kuid jätsin ka enda administraatoriõigustega "Sandra" kontole kaust õigused samad nagu tootaja1 kasutajale.
Pilt kasutajaõigustest kaustal tootaja1

<img width="1040" alt="op4 5" src="https://github.com/sandisyske/OpSys/assets/120086951/c1684bf2-9744-4030-9e46-d951088f01dd">

### Ülesanne 4.6 - Turbe- ja privaatsussätted

Edasi töötasin kasutajas ylemus.
Turbeülevaates soovitab Microsoft Viiruse- ja ohutõrje alaseadistuses häälestama OneDrive'i. Häälestage OneDrive'i failitaastesuvandid lunavararünnaku korral.

### Ülesanne 4.7 - Windowsi turvapoliitikad ja turvamallid

Tavakasutaja tootaja1 keelatakse alla laadida thonny.exe kõigile kasutajatele.

<img width="514" alt="op4 7" src="https://github.com/sandisyske/OpSys/assets/120086951/52afcacc-45fa-443a-9cdb-81c7c99f25cd">

### Ülesanne 4.8 - Tavakasutajaga installimine administraatoriõiguste küsimine

Muutsin administraatori õiguste küsimine tavakasutajal ning proovisin uuesti installida Thonny.

<img width="512" alt="op4 8" src="https://github.com/sandisyske/OpSys/assets/120086951/224bc46e-e592-42cb-9014-1f238a6f0def">

### Ülesanne 4.9 - Turbelogid

Ekraanipilt logikirje ebaõnnestunud sisselogimiskatse kohta.

<img width="502" alt="op4 9" src="https://github.com/sandisyske/OpSys/assets/120086951/4d080844-058d-469b-8530-709d71b9c9ca">

### Ülesanne 4.10 Windowsi registri muutmine

Ekraanivaade, kus pärast DisplayLastLogonInfo-registrivõtme väärtuse muutmist 1-ks, saate sisselogimisel teate, millal arvutisse viimati sisse logiti.

<img width="503" alt="op4 10" src="https://github.com/sandisyske/OpSys/assets/120086951/27bdc7bb-965b-47a2-b8e3-e61845917dc2">

