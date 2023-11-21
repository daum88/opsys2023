Selles praktikumis pidin uurima erinevaid ressursihaldusega seotud ülesandeid Ubuntus ja Windowsis. Otseseid probleeme ei olnud ja ülesandeid said tehtud ning teadmised tulevad tulevikus kasuks.




| Küsimus                                         | Linux                            | Windows                              | Vastus (Linux \| Windows) |
|-------------------------------------------------|----------------------------------|--------------------------------------|---------------------------|
| Mitu protsessi kokku arvutis käib?              | `ps -aux \| wc -l`               | Task Manager -> Jõudlus              | 172 \| 118                |
| Milline on kõige esimesena käivitatud protsess? | `ps axo pid,cmd,comm,etime \| head`| Process Explorer -> Start Time     | `/sbin/init sp`           |
| Milliste kasutajate protsesse arvutis käib?     | `ps aux \| awk '{print $1}' \| sort \| uniq` | Task Manager -> Detailid        | Mattias \| mattias, tootaja1, tootaja2, ylemus |
| Kui kaua on arvuti järjest töötanud (up time)?  | `uptime` või `top`               | Task Manager -> Jõudlus              | 10min \| 8min             |
| Milline protsess käivitati kõige hiljem (viimasena)? | `ps -eo pid,etime,cmd --sort=etime \| tail` | Process Explorer -> Start Time, sorteerida | `/usr/bin/gnome` \| `antimalware service executable` |
| Milline on kõige rohkem protsessoriaega võttev protsess? | `top` või `htop`               | Task Manager -> Protsessid või Jõudlus | `/usr/bin/gnome` \| `antimalware service executable` |
| Milline on kõige rohkem virtuaalmälu võttev protsess? | `top` või `htop`, VIRT veerg    | Task Manager -> Protsessid, sorteerida 'Virtuaalmälu' järgi | `/usr/bin/gnome` \| `antimalware service executable` |
| Milline on kõige rohkem füüsilist mälu võttev protsess? | `top` või `htop`, RES veerg     | Task Manager -> Protsessid, sorteerida 'Mälu' järgi | `/usr/bin/gnome` \| `antimalware service executable` |
| Kui palju füüsilisest mälust (Physical Memory) on vaba? | `free -m`                      | Task Manager -> Jõudlus              | 12GB \| 1.8GB             |
| Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt? | `df -h` | Explorer -> paremklõps C: -> Properties | 46GB/75% \| 35.8GB/56%    |
| Milline on kõige suurem kõvakettal olev fail ja kõige suurem alamkaust? | `find / -type f -exec du -h {} + \| sort -rh \| head -n 1` ja `du -h --max-depth=1 / \| sort -rh \| head -n 1` | Exploreris kasuta otsingut suurte failide ja kaustade jaoks | Nextcloud/ allalaaditud failid |
| Võrrelge terminali käskude: sha1sum /dev/zero \| sha1sum /dev/zero ja sha1sum /dev/urandom \| sha1sum /dev/urandom protsessori kasutust. (Ainult Linuxis) | Jookse käsklusi eraldi terminaliakendes ja vaata top käsku teises aknas. | - | - |
| Milline protsess kõige rohkem salvestusseadmele kirjutab? (Ainult Windowsis) | - | Resource Monitor -> Disk sektsioon | system |
| Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab? (Ainult Windowsis) | - | Resource Monitor -> Disk sektsioon, veerg 'Kirjutatud (B/sec)' | system |
| Milline protsess kõige rohkem salvestusseadmelt loeb? (Ainult Windowsis) | - | Resource Monitor -> Disk sektsioon | memory compression |
| Millisest failist eelmise küsimuse protsess kõige rohkem loeb? (Ainult Windowsis) | - | Resource Monitor -> Disk sektsioon, veerg 'Loetud (B/sec)' | nextcloud.exe |
| Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? (Ainult Windowsis) | - | Resource Monitor -> Network sektsioon | nextcloud.exe |
| Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme või käsureakäske kasutaksid probleemi diagnoosimiseks? | `top` või `htop` (Linux) | Task Manager või Resource Monitor (Windows) | - |
