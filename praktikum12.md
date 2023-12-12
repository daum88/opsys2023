
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

Ülesanne 4:
#!/bin/bash
for fail in *.$1; do
    mv "$fail" "${fail%.$1}.$2"
done

Ülesanne 5:
#!/bin/bash
ps -A | grep "$1" | while read line; do
    pid=$(echo $line | cut -d ' ' -f1)
    name=$(echo $line | cut -d ' ' -f4)
    echo "Protsessi nimi: $name, PID: $pid"
done

Ülesanne 6:
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
