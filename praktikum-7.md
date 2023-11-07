1. Miks andmekandjad vajavad lähtestamist?
Andmekandjad vajavad lähtestamist, et süsteem saaks neid õigesti tuvastada ja kasutada. Lähtestamine hõlmab tavaliselt partitsioonide loomist ja formaatimist, mis võimaldab operatsioonisüsteemil salvestada ja lugeda andmeid kettalt. See on oluline samm uue kõvaketta kasutusele võtmisel, et tagada andmete õige struktureerimine ja haldamine.

2. Millised on GPT kasutamise eelised ja puudused võrreldes MBRiga?
GPT (GUID Partition Table) eelised võrreldes MBR (Master Boot Record) süsteemiga on järgmised:

Suurem partitsioonide arv: GPT võimaldab luua peaaegu piiramatu arvu partitsioone, samal ajal kui MBR on piiratud nelja esmase partitsiooniga.
Suuremad kõvakettad: GPT toetab kõvakettaid, mis on suuremad kui 2 TB, mis on MBRi puhul maksimaalne piirang.
Parem andmete taastamise võimekus: GPT salvestab mitu koopiat partitsioonitabelist ketta eri osades, mis võimaldab andmete paremat taastamist kahjustuste korral.
Turvalisem käivitusprotsess: GPT toetab UEFI (Unified Extensible Firmware Interface), mis pakub paremaid turvaelemente käivitusprotsessis, nagu näiteks turvaline käivitus.
Puudused võivad hõlmata GPT väiksemat ühilduvust vanemate operatsioonisüsteemide ja käivitusseadmetega, mis võivad nõuda UEFI asemel traditsioonilist BIOSi.

3.  <img width="469" alt="4tb" src="https://github.com/daum88/opsys2023/assets/68275432/8bc18563-6544-4b94-be56-bef19bf9a748">
Sain errori, et ei saa ligipääsu kettale.
 4. 

 5.
Mount-käsu parameeter -o ro tähistab "read-only" ehk ainult-loetavat kinnitust. See tähendab, et kinnitatud failisüsteemi saab küll lugeda, kuid sinna ei saa kirjutada. See on kasulik kui soovitakse kaitsta andmekandja sisu juhusliku muutmise eest või kui andmekandja on sellises seisus, et kirjutamise toiming võib põhjustada andmekahjustusi.

Parameeter -t auto ütleb mount-käsule, et ta peaks automaatselt tuvastama failisüsteemi tüübi, mida kasutatakse andmekandjal. Kui see parameeter on määratud, siis mount-käsk proovib tuvastada ja kasutada õiget failisüsteemi draiverit andmekandja kinnitamiseks süsteemile. See tähendab, et kasutaja ei pea määrama konkreetset failisüsteemi tüüpi, nagu nt. ext4, ntfs, vfat jne, vaid süsteem püüab ise kindlaks teha, millist failisüsteemi tuleks kasutada.

6.  ext-4
7.  
