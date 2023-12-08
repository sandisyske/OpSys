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
![image](https://github.com/sandisyske/OpSys/assets/120086951/fea2dfce-6ab6-4caa-861d-8660541a9eda)


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

```                                        
#!/bin/bash
echo "Sisesta protsessi nimi:"
read pnimi

ps_output=$(ps -A)
IFS=$'\n'

for rida in $ps_output; do
        trim_rida=" $rida"
        trim_rida=$(echo "$trim_rida" | tr -s ' ')
        protsessi_nimi=$(echo "$trim_rida" | cut -d ' ' -f5)
        protsessi_pid=$(echo "$trim_rida" | cut -d ' ' -f2)

        if [ "$protsessi_nimi" == "$pnimi" ]; then
                echo "Protsessi nimi on $protsessi_nimi, ja PID on $protsessi_pid"
        fi
done
IFS=$' \t\n'
```

<img width="202" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/61e550bc-3bdf-4696-bf0f-b715800aba78">

### Ülesanne 6 sktiprikood teksina ja ekraanipilt väljundist



