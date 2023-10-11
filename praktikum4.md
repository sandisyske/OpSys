# Windowsi seadistus ja turvalisuse praktikum


### Ülesanne 4.1 

### Ülesanne 4.4 - Käsurida kasutaja õigused

Selles ülesandes alguses võrdlesin tavaõiguste kasutusõiguste käsurida administraatori õiguses käsureaga. Hiljem võrdlesin viimast psexec.exe käivitusega käsurida.
Märkasin kuidas õigused järjest kasvasid. Üks võrdlus mille ma välja toon: "Debug programs" mis ei ole võimalik administraatoriõigustega käsurealt. Sellega võib käivitada programme või käsklusi, mis nõuavad sügavamat ligipääsu või protsesside jälgimise võimalust. Kuid sellega võib kaasneda tõsised turvariskid ja süsteemi probleemid, mis tõttu ei ole ka administraatori õigusega sellele ligipääsu.

### Ülesanne 4.5
Windows cmd on minu jaoks võõras, seega proovisin lahendada seda osa käsurealt.
Lõin uued kasutajad koodiga "net user tootaja1 /add"
Lõin uued kaustad (vastavalt kasutajale) "mkdir C:\OS2023\tootaja1"
Haldasin kausta ligipääsu töötajale, andministraatorile ja enda "Sandra" kontole 
käsuga "icacls C:\OS2023\tootaja1 /grant tootaja1:(OI)(CI)F /grant Administrators:(OI)(CI)F /grant Sandra:(OI)(CI)F"
´teskt´
'teskt'
