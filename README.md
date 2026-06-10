# Section 1: Foundations of Data Structures & Algorithms

## Question 1: The Theoretical Matchup: Arrays vs. Linked Lists

Polja pohranjuju elemente na uzastopnim memorijskim lokacijama, pa učitavanje jednog elementa često dovodi i susjedne elemente u CPU cache. Zbog dobrog „spatial locality-a“ i mogućnosti predučitavanja podataka (end. prefetching), pristup elementima je vrlo brz.
Dvostruko povezane liste pohranjuju čvorove na različitim lokacijama povezanim pokazivačima. Prolazak kroz listu zahtijeva praćenje pokazivača za svaki element, što često uzrokuje „cache miss“ i dohvaćanje podataka iz RAM-a, koje je znatno sporije od pristupa cacheu. Takav način pristupa također otežava prefetching i smanjuje paralelno odrađivanje instrukcija.
Zato, iako obje strukture zahtijevaju N koraka, polja mnogo bolje iskorištavaju CPU cache i memorijsku hijerarhiju, zbog čega su u praksi često 10–100 puta brža od povezanih lista.

## Question 2: The Space Complexity Trap in Recursion

Program se srušio zbog stack overflowa, a ne zbog nedostatka RAM-a. Rekurzivni DFS koristi prostornu složenost O(H), gdje je H maksimalna dubina stabla, pri čemu svaki rekurzivni poziv stvara novi stack frame na call stacku. U vrlo dubokoj strukturi direktorija broj poziva premašio je maksimalnu veličinu stacka dodijeljenu procesu ili dretvi, zbog čega je operacijski sustav prekinuo program segmentation faultom. Slobodnih 64 GB RAM-a nije pomoglo jer je stack zasebno i ograničeno memorijsko područje, često od nekoliko MB, odvojeno od heapa.
