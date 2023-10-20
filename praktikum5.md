
Ülesanne 5-1:

a) Faili minufail.txt lugemiseks on vaja read õigust (r) kataloogile /tmp/kaust.
b) Faili minufail.txt kustutamiseks on vaja write õigust (w) kataloogile /tmp/kaust.


Ülesanne 5-2:

chmod a=x skriptifailile ei ole piisav, kuna lisaks käivitamisõigusele on vaja ka lugemisõigust (r), et skriptifaili sisu oleks võimalik lugeda ja seejärel käivitada.


Ülesanne 5-3:

Igal kasutajal on omanimeline grupp, et hõlbustada ressursside jagamist ja haldamist.


Ülesanne 5-4:

Minimaalsed õigused faili uusfail.txt sisu kuvamiseks on read (r) õigus failile ja execute (x) õigus kataloogile majasiseseks-kasutamiseks.



<img width="222" alt="LINUX2" src="https://github.com/daum88/opsys2023/assets/68275432/880d240f-cfff-436b-9df1-49c061cbd502">
<img width="371" alt="LINUX" src="https://github.com/daum88/opsys2023/assets/68275432/8d1112c8-50b2-4665-930e-8e8e65fe9381">




Ülesanne 5-5:

Setuid-õigus võimaldab programmi käivitada faili omaniku õigustes, isegi kui programmi käivitab mõni muu kasutaja.


Ülesanne 5-6:

Jah, setuid-i kasutamine võib vähendada süsteemi turvalisust, kuna see võib anda kasutajatele rohkem õigusi kui neil peaks olema, võimaldades neil teostada ohtlikke toiminguid.


Ülesanne 5-7:

Sticky bit-õigusega kataloogist yhiskaust saavad peeter-kasutaja loodud faile kustutada ainult peeter, root ja võib-olla kataloogi omanik (kui see pole peeter).


Ülesanne 5-8:

ACL-i kasutamine võimaldab määrata rohkem detaileeritud juurdepääsuõigusi, mida saab kontrollida ja muuta getfacl ja setfacl käskudega.


Ülesanne 5-9:

chattr +i parameetriga faili saab modifitseerida ainult root kasutaja. +i parameeter teeb faili muutumatuks. Faili testfail-2 kustutamiseks tuleb esmalt eemaldada +i atribuut käskudega sudo chattr -i testfail-2 ja seejärel kustutada fail käskudega rm testfail-2 või sudo rm testfail-2
