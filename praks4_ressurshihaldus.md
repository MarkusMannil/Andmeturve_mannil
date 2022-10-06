| **Küsimus**                                         | **Linux** | **Windows** | **Linuxis kasutatud käsklus** | **Windowsis kasutatud tööriist** |
|-----------------------------------------------------|-----------|-------------|-------------------------------|----------------------------------|
| Mitu protsessi kokku arvutis käib?                  |    215    |     292     |      ps -aux \| wc -l        |      tegumihaldur -> jõudlus     |
| Milline on kõige esimesena käivitatud protsess?     |/sbin/init splash |  smss.exe   |   ps axo pid,cmd,comm,etime  |         process explorer         |
| Mitu ja milliste kasutajate protsesse arvutis käib? |213        |        103  |ps -eo user\| sort -k 1 -ru\ps| uniq -c|           tegumihaldur           |
| Kui kaua on arvuti järjest töötanud (up time) ?     |11min|6 min 36 sek |uptime|      tegumihaldur -> jõudlus     |
| Milline protsess käivitati kõige hiljem (viimasena)?|\[kworker/u4:0-events_unbound| rundll32.exe  |   ps -efps |       procces explorer          |
|Milline on kõige rohkem protsessoriaega võttev protsess?|/usr/bin/gnome-shell|     MsMpEng.exe |ps aux\| sort -nrk 3,3\|head -n 5| procces explorer|
|Milline on kõige rohkem virtuaalmälu võttev protsess?|/usr/bin/gnome-shell    |msedge.exe      |ps aux --sort=-%mem \| head|      procces explorer |
|Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?|   /usr/bin/gnome-shell   |MsMpEng.exe      |ps aux --sort=-%mem|      procces explorer|
|Kui palju füüsilisest mälust (Physical Memory) on vaba?|         202084 K            |1735884 K               | vmstat      |procces explorer -> System information|
|Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt?|12.3 Gb 43%  |0.1 GB 0.3 % |df -x squashfs --total|winDirStat|
|Milline on kõige suurem kõvakettal olev fail ja kõige suurem kaust?|/.cache/tracker3/files kaust , 
/snap/firefox/common/.cache/mozilla/firefox/llfgb3pq.default/startupCache/scriptCache.bin| pagefile.sys  Windows(folder)|
kaust : du -Sh \| sort -rh \| head -10 fail : find -type f -exec du -Sh {} + \| sort -rh \| head -n 5
|winDirStat|

Milline protsess kõige rohkem salvestusseadmele kirjutab, kõige rohkem salvestusseadmelt loeb? Millisesse faili antud protsess kõige rohkem kirjutab, millisest failist kõige rohkem loeb?

- procces exploreri järgi IO read bytes ja writes bytes järgi loeb kõige rohkem SearchHost.exe ja kirjutab  taskhostw.exe


Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? Vali antud protsessi poolt kasutatavatest ühendustest üks ning kirjuta välja järgnev: kohalik IP-aadress, kohalik port, ühenduse teise poole IP-aadress, port, latents ja antud ühenduse poolt kasutatav võrguliikluse kogumaht


Sõber kurdab, et tema arvuti on oluliselt aeglasem kui varasemalt. Millise programmiga ja millise parameetrite abil saate tuvastada milline protsess või teenus muudab arvuti aeglaseks?

Kuna enamus inimesed kasutavad Windowsi  operatsiooni süsteemi, siis soovitaks tal vaadata alustuseks task mangeri ning sealt leida mingit taustal jooksvaid protesse mis võivad arvutit aeglustda


Võrrelge terminali käskude: sha1sum /dev/zero | sha1sum /dev/zero ja sha1sum /dev/urandom | sha1sum /dev/urandom protsessori nõudlust. Avage teine terminaliaken ja top samaaegseks käivitamiseks. Uurige millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral? (Ainult Linuxis) Lisa ka ekraanipilt aruande juurde näiteks pärast tabelit.
