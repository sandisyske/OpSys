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
![image](https://github.com/sandisyske/OpSys/assets/120086951/67da7219-a367-4b8f-b7c9-08751fefb1af)


### Ülesanne 6 sktiprikood teksina ja ekraanipilt väljundist
```
#!/bin/bash
# Funktsioon
astenda() {
        number=$1
        astendaja=$2
        tulemus=1

        for ((i=5; i>=1; i--)); do
                tulemus=$(($tulemus * $number))
        done
        echo $tulemus
}
tulemus=$(astenda 9 5)
echo "9 astmes 5 tulemus on $tulemus"
```
<img width="237" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/30bd9677-4249-4056-a059-faa4d02cae90">

### Ülesanne 7 Skriptimine ja AI

* Prompt AI-le:
Ülesanne 6: Looge funktsioon astendamiseks Linuxi skriptina

Loo bash-skript nimega yl6.sh Linuxi keskkonnas. Skript peaks sisaldama funktsiooni astendamiseks, kasutades korrutamistehet ja rekursiooni või tsüklit. Funktsioon peaks arvutama ja väljastama 9^5 väärtuse.

Veendu, et skripti alguses on määratud õige interpretaator (#!/bin/bash). Sa võid kasutada rekursiooni, for-tsüklit või muud sobivat meetodit astendamiseks.

* Bing Chat vastus
```
  #!/bin/bash

power() {
    local res=1
    for ((i=1;i<=$2;i++)); do
        res=$((res*$1))
    done
    echo $res
}

power 9 5
```
<img width="644" alt="image" src="https://github.com/sandisyske/OpSys/assets/120086951/9c14fcbb-cb3c-47cd-b7d2-9d0f1201c8d4">

  
