# XEUX 
XEUX - Multiprocessing Operating System for Atari XL/XE

-----

Niniejsze repozytorium zawiera kod źródłowy, środowisko, narzędzia i demo produktu, który powstał w ramach mojej pracy inżynierskiej w 2006 roku. 

Tytuł pracy jest odrobinę na wyrost być może, gdyż sporo jeszcze brakuje do tego, żeby można było ten produkt nazwać pełnoprawnym systemem operacyjnym, raczej jest pewnym proof of concept tego, że teoretycznie jakby chcieć, to można. 

Zawiera jednakże:
 - jądro systemu, umożliwiające współbieżną pracę 32 niezależnych procesów
 - wieloprocesowość kooperatywną
 - wywłaszczanie procesów
 - liniowy przydział pamięci RAM i relokowalne pliki binarne
 - sygnały (łącznie z możliwością rejestrowania własnych procedur ich obsługi przez procesy)
 - podstawową komunikację miedzyprocesową
 - wirtualne konsole (z bardzo prymitywnym edytorem, wybaczcie)
 - obsługę pamięci masowej poprzez procedury DOS i semafory

Całość zadziała na stockowej maszynie XL/XE, oczywiście dodatkowy RAM (portb) jest wskazany.
Wielkość pojedynczego segmentu kodu ograniczona jest do 15KB.

Scheduler i jego działanie: 
 - scheduler powieszony jest na przerwaniu VBL
 - zachowuje stos i stronę zerową procesu
 - proces, który oczekuje na I/O sam oddaje zasoby schedulerowi
 - w przypadku przekroczenia przydzielonego czasu proces zostanie wywłaszczony
 - kontekst procesu, dla którego pojawił się rezultat procedury wejścia/wyjścia przywracany jest poza kolejnością

Więcej szczegółów jest rozpisanych w samej pracy właściwej, która również znajduje się w repozytorium, w katalogu doc/

Nawet przez dłuższą chwilę wydawało mi się, że ten proof of concept zostanie przepisany (żeby nie było wstydu), uzupełniony, poprawiony i rozbudowany i ktoś będzie się mógł cieszyć. No ale w międzyczasie mrugnąłem oczami i okazało się, że jest 17 lat później. Nie ma chyba co liczyć, że sytuacja jakoś drastycznie się zmieni, a zestarzałem się już na tyle, żeby nie przejmować się tym, jak bardzo byle jaki kod wygenerowałem w 2006 roku, więc zapraszam zainteresowanych do nurzania się w tym projekcie. 

Mam nadzieję, że nawet jeśli nikomu do niczego się nie przyda, to przynajmniej bedzie stanowić jakąś ciekawostkę.

krap (maciej.grzeszczuk@gmail.com) [github: czeslawsender], 23.03.2023

-----

This repository contains the source code, environment, tools and demo of the product that was created as part of my engineering thesis in 2006.

The title of the work is perhaps a bit exaggerated, because there is still a lot of work to do to call this product a full-fledged operating system, it is rather a proof of concept that theoretically, if you want it, you can do it.

It contains:
  - the kernel of the system, enabling the concurrent operation of 32 independent processes
  - cooperative multiprocessing
  - preemption of processes
  - linear RAM allocation and relocatable binaries
  - signals (including the ability to register their own procedures for handling them by processes)
  - basic interprocess communication
  - virtual consoles (with a very primitive editor, sorry)
  - support for mass storage through DOS routines and semaphores

The whole thing will work on a stock XL/XE machine, of course additional RAM (portb) is recommended.
The size of a single code segment is limited to 15KB.

Scheduler and its operation:
  - scheduler hangs on VBL interrupt
  - preserves the stack and page zero of the process
  - the process that waits for I/O gives resources to the scheduler on its own
  - if the allotted time is exceeded, the process will be preempted
  - the context of the process for which the result of the input/output procedure awaits is restored out of order

More details are provided in the thesis itself, which you can find in this repository in the doc/ directory.

For a long time, I even thought that this proof of concept would be rewritten, supplemented, corrected and expanded, and someone would be able to enjoy it. But in the meantime I blinked and 17 years happened. It's unlikely that the situation will change drastically, and I'm old enough to not care about how sloppy code I generated in 2006, so I invite those interested to explore and enjoy project in whatever state it is.

I hope that even if it is of no use to anyone, it will at least be a nice curiosity.

krap (maciej.grzeszczuk@gmail.com) [github: czeslawsender], March 23, 2023

