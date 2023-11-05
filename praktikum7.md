# Praktikum 7 - Haakimine

### Ülesanne 7.1 
Miks andmekandjad vajavad lähtestamist? - Andmekandja lähtestamisel kustutatakse sellelt kogu sisu ning valmistatakse ette, see tähendab, et lähtestamine võimaldab valida sobiva failisüsteemi (NTFS, FAT32, ext4 jne) , et Windows saaks sellega edasi tegeleda. Peale lähtestamist on võimalik partitsioone lisada.

Millised on GPT kasutamise eelised võrreldes MBRiga?
1. 1. GPT on parem kui soovid partistioone lisada 2 TB suuremale kettale, sest MBR seda ei võimalda.
2. 2. MBR salvastab boot ja partitsioneerimise andmed, aga GPT salvestab neid andmeid nii, et kui midagi kirjutatakse üle või on korrupteerunud, siis saab GPT peal andmed taastada.
3. 3. MBR on tihedalt seotud vananenud BIOS-iga, kuid GPT ühilduv UEFI-ga, mis on BIOS-i kaasaegne alglaadimise süsteem.  UEFI pakub kaasaegsematele süsteemidele paljusid praktilisi eeliseid nagu kiirus, efektiivsus, turvalisus, suurem andmete käsitlemise võimalus ning ühilduvus kaasaegsete tehnoloogiatega.
  
4. # Ülesanne 7.2
5. https://kodu.ut.ee/~sandrae/hdd.png

# Ülesanne 7.3

<img width="480" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/0a4a68c3-343d-4e4c-b433-1b01f50de7b5">

# Ülesanne 7.5

Mida mõjutasid mount-käsu parameetrid -o ro ja -t auto?

Mount käsu parameetrid:
1. -o ro - -o tähistab valikuid (options) ja ro ehk read only tähendab ainult lugemise režiimi, ehk saab ainult andmeid lugeda, mitte kirjutada.

2. -t auto - -t tähistab failisüsteemi tüüpi (filesystem type) ja auto tähendab, et süsteem peab ise tuvastama mis failisüsteemi kasutatakse USB-seadmel.

Leidke mount-käsu väljundist üles, mis väärtusega asendas Ubuntu auto-parameetri.

Mount käsuga sain USB-seadme info :

/dev/sdd1 on /media/usb type vfat (ro,relatime,fmask=0022,dmask=0022,codepage=437,iocharset=iso8859-1,shortname=mixed,errors=remount-ro)

See tähendab, et Ubuntu asendas auto parameetri väärtusega vfat.

# Ülesanne 7.6

