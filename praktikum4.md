4.1


4.2



![4-3](https://github.com/daum88/opsys2023/assets/68275432/5da0a99a-2244-49d5-ae5b-5b310e1f9468)



4.3


![4-2](https://github.com/daum88/opsys2023/assets/68275432/90c2f38c-df73-44f7-b081-6114e22c0cb3)

4.4

Kasutusala:

Administrator: Administratori konto võimaldab teha süsteemiulatuslikke muudatusi arvutis, nagu teiste kasutajakontode nimede, piltide, paroolide ja tüüpide muutmine​1​. Administratori konto võib konfigureerida süsteemi seadeid ja pääseda juurde tavaliselt piiratud osadele operatsioonisüsteemist.
SYSTEM: SYSTEM-konto on mõeldud operatsioonisüsteemi ja Windowsi all töötavate teenuste kasutamiseks. Paljud Windowsi teenused ja protsessid vajavad võimalust sisemiseks sisselogimiseks, mida SYSTEM-konto võimaldab​2​.
Konto Tüüp:

Administrator: Administrator on tegelik konto, millel on parool ja mida saab kasutada inimkasutaja poolt.
SYSTEM: SYSTEM ei ole tegelik konto, vaid "turva põhimõte" (security principal) ja sellel pole parooli. Praktiliselt, kui arvuti on ühendatud domeeniga, saavad SYSTEMina töötavad protsessid pääseda juurde domeeni serveritele, mis on erinevus võrreldes Administratori kontoga​3​.
Õigused:

Administrator: Administraatoritel on õigus teostada erinevaid süsteemiga seotud toiminguid, nagu süsteemi sulgemine, draiverite laadimine või süsteemi aja muutmine​4​.
SYSTEM: SYSTEM-kontol on samad failiõigused nagu administraatoril, kuid seda kasutavad süsteem ja süsteemiteenused, mis võivad nõuda sügavamaid süsteemiõigusi kui administraatori tasemel.
Üks tegevus, mille jaoks on vaja SYSTEMi õigusi (ja mille jaoks ei piisa administraatori õigustest), on süsteemiteenuste käitamine ja haldamine, mida tavaliselt teostab operatsioonisüsteem või süsteemi taustaprotsessid. SYSTEMi konto on mõeldud süsteemi enda jaoks ja sellel on ulatuslikumad õigused süsteemiressurssidele ja -ülesannetele, võimaldades seeläbi suuremat kontrolli arvuti üle kui administraatori konto.




4.5



![4-5 2](https://github.com/daum88/opsys2023/assets/68275432/4ff5f5fb-7956-4535-8b85-a50edb898721)
![4-5 3](https://github.com/daum88/opsys2023/assets/68275432/dcdd5ac7-7f57-41e2-9818-876789f3d910)
![4-5](https://github.com/daum88/opsys2023/assets/68275432/cbe7e7c8-bb59-479d-998b-db61942b9971)


4.6



![4-6](https://github.com/daum88/opsys2023/assets/68275432/5d23b1a2-2cd9-47f6-989c-6e612674b04f)
4.7






![4-7](https://github.com/daum88/opsys2023/assets/68275432/54648c55-504e-49c3-a0c1-7425559422a2)



4.8

-------

4.9


![4-9](https://github.com/daum88/opsys2023/assets/68275432/6c5c07f4-d640-491b-9f03-a62f571c327d)




4.10



![4-10](https://github.com/daum88/opsys2023/assets/68275432/4aae7cfe-63b0-470a-b4c0-3d555ed5cdd8)
