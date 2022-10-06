| **Küsimus**                                         | **Linux** | **Windows** | **Linuxis kasutatud käsklus** | **Windowsis kasutatud tööriist** |
|-----------------------------------------------------|-----------|-------------|-------------------------------|----------------------------------|
| Mitu protsessi kokku arvutis käib?                  |    215    |     292     |      ps -aux | wc -l        |      tegumihaldur -> jõudlus     |
| Milline on kõige esimesena käivitatud protsess?     |/sbin/init splash |  smss.exe   |   ps axo pid,cmd,comm,etime  |         process explorer         |
| Mitu ja milliste kasutajate protsesse arvutis käib? |213        |        103  |ps -eo user| sort -k 1 -r| uniq -c|           tegumihaldur           |
| Kui kaua on arvuti järjest töötanud (up time) ?     |           |6 min 36 sek |                               |      tegumihaldur -> jõudlus     |
| Milline protsess käivitati kõige hiljem (viimasena)?|           | rundll32.exe  |                               |       procces explorer           |
|Milline on kõige rohkem protsessoriaega võttev protsess?|    |     MsMpEng.exe |                               | procces explorer|
|Milline on kõige rohkem virtuaalmälu võttev protsess?|  |msedge.exe  |  |  procces explorer |
|Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?|        |MsMpEng.exe |           | procces explorer|
|Kui palju füüsilisest mälust (Physical Memory) on vaba?| |1735884 K||                                              procces explorer -> System information|
|Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt?||0.1 GB 0.3||tegumihaldur -> jõudlus|
|Milline on kõige suurem kõvakettal olev fail ja kõige suurem kaust?|| pagefile.sys  Windows(folder)||winDirStat|
