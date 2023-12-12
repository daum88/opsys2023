Seekordses prktikumis tegelesime skriptimiega Ubuntus. Sain proovida erineate skriptide loomist ja ka AI kasutamist oma töö tegemisel.
Ülesanne 3:
<img width="355" alt="12 3" src="https://github.com/daum88/opsys2023/assets/68275432/eab1349f-fd48-4012-b41c-3e6dcdd975ff">
#!/bin/bash
echo "Sisesta oma nimi:"
read nimi
echo "Sisesta oma eriala:"
read eriala
echo "Sisesta oma matriklinumber:"
read matriklinumber
echo "Tere, $nimi! Sinu eriala on $eriala ja matriklinumber on $matriklinumber."

Ülesanne 4:<img width="260" alt="12 4" src="https://github.com/daum88/opsys2023/assets/68275432/1ceecf16-6679-4a5e-b2ea-4e63efb68eb3">
#!/bin/bash

if [ $# -ne 2 ]; then
    echo "Kasutus: $0 algne_laiend uus_laiend"
    exit 1
fi

algne_laiend=$1
uus_laiend=$2

if [[ $algne_laiend != .* ]]; then
    algne_laiend=".$algne_laiend"
fi

if [[ $uus_laiend != .* ]]; then
    uus_laiend=".$uus_laiend"
fi

for fail in *$algne_laiend; do
    # Kontrolli, kas fail eksisteerib
    if [ -f "$fail" ]; then
        uus_nimi="${fail%$algne_laiend}$uus_laiend"
        mv "$fail" "$uus_nimi"
        echo "Faili nimi muudetud: $fail -> $uus_nimi"
    fi
done


Ülesanne 5:
#!/bin/bash
ps -A | grep "$1" | while read line; do
    pid=$(echo $line | cut -d ' ' -f1)
    name=$(echo $line | cut -d ' ' -f4)
    echo "Protsessi nimi: $name, PID: $pid"
done



Ülesanne 6: <img width="271" alt="12 6" src="https://github.com/daum88/opsys2023/assets/68275432/bead6fc0-c955-4438-aa44-097054ace708">
#!/bin/bash
astenda() {
    tulemus=1
    for (( i=0; i<$2; i++ )); do
        tulemus=$(($tulemus * $1))
    done
    echo $tulemus
}

echo "9 astmes 5 on $(astenda 9 5)"







<img width="479" alt="chat2" src="https://github.com/daum88/opsys2023/assets/68275432/4e0c7278-a55c-46a2-9650-05fd028f5512">
<img width="482" alt="chat1" src="https://github.com/daum88/opsys2023/assets/68275432/c3c34e1b-0071-472d-8ecd-0d32696a31bc">
