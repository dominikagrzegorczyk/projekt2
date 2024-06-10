# Projekt 2 - Informatyka Geodezyjna 2
## Wtyczka do aplikacji Qgis
### Wymagania:
- system Windows 11
- program Qgis wersja 3.28 lub nowsza
- python 3.11
### Potrzebne biblioteki:
- os
- qgis.PyQt
- qgis.utils
- qgis.core
##Funkcje wtyczki:
1. Liczenie różnic wysokości między dwoma punktami
Do policzenia przewyższenia między wybranymi punktami, należy wybrać dwa znajdujące się na tej samej warstwie. Program pobierze wtedy wartosc z kolumny o nazwie wysokosc z tabeli atrybutów. Działanie jakie będzie wykonywać program to odjęcie od siebie wysokości (wysokość zaznaczona jako druga - wysokość zaznaczona jako pierwsza). Przewyższenie może przyjmować wartości ujemne oraz dodatnie, w zależności od tego czy na terenie występuje spadek lub wzrost.
Aby wtyczka poprawnie obliczyła wysokość zaznaczone punkty muszą znajdować sie na aktywnej warstwie punktowej oraz w takiej, która posiada w tabeli atrybutów kolumne z odpowiednimi wysokościami o nazwie "wysokosc".
Uzyskany wynik jest wyrażony w metrach [m] z dokładnością do milimetrów [mm].
2. Obliczenie pola powierzchni figury o wierzchołkach w punktach ze współrzędnymi X,Y
Aby obliczyć pole powierzchni powstałej figury należy wybrać najmniej 3 punkty. Na podstawie współrzędnych program policzy pole przy użyciu metody Gaussa.
Uzyskany wynik jest w hektarach [ha] z dokładnością do trzech miejsc.
##Sposób użycia wtyczki:
1. Należy pobrać wtyczkę i umieścić ją w folderze z wtyczkami Qgis
2. Po otworzeniu programu Qgis należy wgrać warstwę z wymienioymi atrybutami X,Y,H
3. Po zainstalowaniu wtyczki i  jej uruchomieniu, pojawi się okno z punktami. 
4. Należy wybrac:
- dwa punkty oraz zaznaczyć "Wysokość", program policzy przewyższenie
- trzy lub wiecej punktów oraz zaznaczyć "Pole", wtedy program policzy pole figury
5. W każdym innym przypadku pojawi sie komunikat o błędzie
