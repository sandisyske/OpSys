# Praktikum 12 - Skriptimine Linuxis

### Ülesanne 3 sktiprikood teksina ja ekraanipilt väljundist
```
#!/bin/sh
echo "Sisesta nimi:"
read nimi
echo "Sisesta eriala:"
read eriala
echo "Sisesta enda matriklinumber:"
read mnr

echo "Sinu nimi on $nimi."
echo "Sa õpid $eriala erialal."
echo "Sinu matriklinumber on $mnr"
```
![image](https://github.com/sandisyske/OpSys/assets/120086951/3b586cc7-c30f-4a3c-88ab-e28ad4c3687f)

### Ülesanne 4 sktiprikood teksina ja ekraanipilt väljundist
```
#!/bin/bash
echo "Sisesta kaust: "
read kaust
vanalaiend="txt"
uuslaiend="csv"
cd "$kaust" || exit
for fail in *.$vanalaiend; do
        if [ -e "$fail" ]; then
                if [ "${fail##*.}" = "$vanalaiend" ]; then
                        #faili ymbernimetamine
                        uusnimi="${fail%.*}.$uuslaiend"
                        mv "$fail" "$uusnimi"
                        echo "Faili $fail ümbernimetus on $uusnimi"
                fi
        fi
done
```
<img width="239" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/ce5a7079-7926-468e-b500-5a0d80455d97">


### Ülesanne 5 sktiprikood teksina ja ekraanipilt väljundist


### Ülesanne 6 sktiprikood teksina ja ekraanipilt väljundist



