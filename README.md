# MIPS_domaci1
Bogdan Mitrovic 619/2020
U ovom projektnom zadatku je odradjena simulacija paljenja i gasenja led-e.
Prvo je izabran port na osnovu broja samoglasnika u imenu, 
posto se ime Bogdan Mitrovic sastoji od 5 samoglasnika a to su o, a, i, o, i,
preostalih 9 slova su suglasnici, 
sto znaci da je broj samoglasnika manji od suglasnika
s tim u vezi biramo port B.
Pin se bira na osnovu broja slova u imenu i prezimenu zajedno po modulu 6.
Bogdan Mitrovic se sastoji od 14 slova, i to po modulu 6 daje 2. Bira se pin 2.
Prva sekvenca ce imati visoki impuls duzine 6 milisekundi zbog duzine imena, i nizak impuls 8 milisekundi zbog duzine prezimena. Ova sekvenca ce se ponoviti 6 puta zbog duzine imena. Nakon koje ce poceti druga sekvenca.
Druga sekvenca ce imati visoki impuls duzine 8 milisekundi zbog duzine prezimena, i nizak impuls 6 milisekundi zbog duzine imena. Ova sekvenca ce se ponoviti 8 puta zbog duzine prezimena.
Nakon zavrsetka druge sekvence, pocece prva sekvenca ponovo i tako u krug.
Na semi smo dodali STM32F103C6 mikrokontroler, i na njegov pin PB2 smo povezali otpornik koji ce da sluzi da ogranici struju kroz diodu ciju anodu smo povezali sa otpornikom i katodu smo povezali sa masom. Tako da ce dioda svetleti kada na pinu PB2 bude visoki impuls od 3.3 volta, a kada je nizak impuls, dioda ce se ugasiti. Kada se simulira kolo, ljudsko oko nece primetiti gasenje diode, jer je sirina impulsa jako kratka. Zato smo na anodu diode dodali osciloskop da bi se uverili da na anodu dolazi sekvenca impulsa koju smo prethodno zadali. 