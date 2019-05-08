# GNU/Linux Podstawy

## Spis Treści
1. [Informacje o repozytorium](#informacje-o-repozytorium)
. [Jak Pomóc?](#jak-pomóc)  
. [Podstawowe informacje](#podstawowe-informacje)
. [Instalacja Linuxa](#instalacja-linuxa)
. [Granie na Linuxie](#granie-na-linuxie)  
. [Słowniczek](#słowniczek)  

## Informacje o repozytorium
Ta instrukcja zawiera podstawowe informacje o systemie GNU/Linux, jego zastosowaniach, instalacji, podstawowej konfiguracji oraz użytkowaniu.

Jest ona przeznaczona dla początkujących osób, chcących zacząć przygodę z systemem, będąc wyposażonym w podstawową wiedzę oraz narzędzia.

## Podstawowe informacje
GNU/Linux jest uniksopodobnym systemem operacyjnym korzystającym z jądra Linux. Jądro to jest najważniejszą składową systemu operacyjnego, mająca pełną kontrolę nad tym urządzeniem.

## Dla kogo Linux?

Linux z racji swojej budowy i modelu licencjonowania nadaje się przede wszystkim dla:
* ludzi dbających o swoją prywatność
* ludzi troszczących się o swoje bezpieczeństwo w sieci
* programistów
* zarządzających sieciami komputerowymi
* zwykłych użytkowników
* retro i niedzielnych graczy

Mimo wszystko istnieją tacy rodzaje użytkowników, dla których Linux jako główny system nie jest wskazany:
* hardcorowi gracze dla których liczy się każda klatka
* użytkownicy korzystający z oprogramowania nieistniejącego na Linuxie lub nie chcących używać Wine do ich uruchomienia

Dla tych wszystkich osób, które nie mogą zainstalować Linuxa jako główny system, zachęcam do jego instalacji w trybie dualboot obok Windowsa

## Mity i fakty
Wiele nieprawdziwych i przestarzałych informacji krąży na temat Linuxa

* Sterowniki na Linuxa są tragicznej jakości - FAŁSZ
Jeszcze kilka/kilkanaście lat temu znaczna część producentów traktowała po macoszemu Linuxa i wydawane przez nich sterowniki były zamknięte oraz czasami słabej jakości. Dzisiaj większość producentów dostarcza kod swoich sterowników razem z kernelem, dzięki czemu razem ze wsparciem społeczności firmy takie jak Intel czy AMD, przygotowują lepsze sterowniki niż na Windowsie, często obsługujące wyższe wersje OpenGL i Vulkan.
* Linux nie jest dobrym systemem dla graczy - CZĘŚCIOWO PRAWDA
Wiele gier, które mają premierę na Windowsie, nigdy nie dostaje portu na Linuxa lecz. Ten problem jest częściowo rozwiązany przez D9VK oraz DXVK, które umożliwia translację odwołań DirectX 9, 10 i 11 na multiplatformowy Vulkan, zapewniając przeważnie 70%-80% wydajności(ciągle są ulepszane). Zdarza się, że starsze gry, które nie wcale uruchamiają się na Windowsie lub działają z błędami, uruchamiają się bez problemów na Linuxie.
* Na Linuxa nie ma komercyjnych programów - CZĘŚCIOWO PRAWDA
Część producentów oprogramowania omija szerokim łukiem Linuxa, mimo, że niektóre firmy pokroju Autodesk od całkiem dawna tworzą oprogramowanie na ten system.
* W Linuxie trzeba korzystać z konsoli - FAŁSZ
Znaczna część dystrybucji, a w szczególności te bazujące na Ubuntu(np. KDE Neon, Linux Mint), zdolna jest obsługi systemu bez konieczności używania terminala. Trzeba jednak dodać, że znajomość podstawowych komend w terminalu, chociaż wydaje się nieco przytłaczająca dla nowych użytkowników, pozwala na sprawniejsze korzystanie z systemu.

## Dystrybucje, wydania LTS, dystrybucja ciągłe i cykliczne

Podstawowym zagadnieniem, na który natkniesz się jest słowo __Dystrybucja__, które oznacza system operacyjny z jądrem Linuxa. Dystrybucje mogą od siebie wywodzić, dzięki czemu przejmują część z ich właściwości. Takim przykładem jest Linux Mint, który wywodzi się od Ubuntu, który to natomiast pochodzi  od Debiana.

Ważną dla wielu użytkowników, jest posiadanie przez niektóre dystrybucje __Wydań LTS__. Takie wydania są wspierane np. w Ubuntu i Linux Mint 5 lub 3 Lata w zależności od wersji, podczas gdy zwykłe wydania są wspierane jedynie przez 9 miesięcy.

W świecie Linuxa panuje podział na dwa typy dystrybucji, ciągłą i cykliczną.
* Dystrybucja Ciągła - Oferuje najnowsze dostępne aktualizacje, lecz nowsze wersje programów mogą powodować różne problemy, nawet takie jak niemożność uruchomienia systemu. Przykładami takich dystrybucji są: Arch Linux czy Manjaro.
* Dystrybucja Cykliczna -  Przykładami takich dystrybucji są: Ubuntu, Linux Mint, Fedora





## Tworzenie Bootowalnego Pendriva
W tej instrukcji posłużę się bardzo przyjazną dystrybucją Kubuntu 18.04.2 LTS z KDE Plasma 5.  
Aby pobrać system w postaci pliku torrent, należy pobrać również oprogramowanie zdolne do jego uruchomienia. [Link do pobrania systemu jako Torrent(zalecany)](http://cdimage.ubuntu.com/kubuntu/releases/18.04/release/kubuntu-18.04.2-desktop-amd64.iso.torrent) oraz [Link do pobrania programu Qbittorrent](https://www.qbittorrent.org/download.php).  
Istnieje również [bezpośredni link do pobrania systemu](http://cdimage.ubuntu.com/kubuntu/releases/18.04/release/kubuntu-18.04.2-desktop-amd64.iso).

Potrzebujemy przygotować pendrive z minimalnym rozmiarem 4GB, by można było uruchomić z niego system.
Część z systemów po wypakowaniu pliku ISO na pendriva powinna działać, lecz my skorzystamy na Windowsie z programu Rufus a alternatywnie możemy skorzystać z programu Etcher wspierającego również Linuxa

UWAGA - wszystkie dane zawarte na pendrive zostaną skasowane
## Testowanie Systemu
Testowanie systemu może odbyć się w dwóch trybach:
* w maszynie wirtualnej(przydatne przy sprawdzaniu wyglądu i funkcji)
* na sprzęcie(przydatne do sprawdzania jak radzi sobie system na urządzeniu)
Uważam, że najlepiej jest sprawdzić Linuxa na "żywym" sprzęcie, otrzrymując dzięki temu

Po pierwsze musimy uruchomić system z pendriva, lecz sposób wejścia do Boot Menu jest zależny od posiadanej płyty głównej. Często są to klawisze F2, F8, F9, F10, F11, F12 czy ESC.
Z menu wyboru wybieramy pendrive. W wypadku gdy na liście są dwa rekordy wybieramy ten z przydomkiem UEFI.

## Instalacja
Aby rozpocząć instalację, robimy dokładnie co w poprzednim punkcie dochodząc do działającego pulpitu, na którym wybieramy instaluj Kubuntu.




W instalatorze na początku wybieramy język polski
Potem łączymy się z siecią bezprzewodową(sieć przewodowa połączy się automatycznie)

W następnym menu wybieramy menu insta
## Konfiguracja


## Granie na linuxie
Jak już wcześniej wspominałem granie na Linuxie jest możliwe mimo pewnych niedogodności.
Do retro gier i gier niewymagających dużej mocy obliczeniowej zwykle nie potrzeba nic instalować oprócz Wine dostępnego w repozytorium lub poprzez Lutris.


## Jak Pomóc?
* __Udostępniaj__ - Byłbym wdzięczny, gdybyś rozpowszechnił ją wśród znajomych, rodziny czy na Facebooku.
* __Zgłaszaj błędy__ - Jeśli znalazłeś błąd w instrukcji, lub jej część jest dla ciebie niejasna, to zgłoś to w zakładce __Issues__
* __Dodawaj i naprawiaj treści__ - Jeśli chcesz naprawić błąd w instrukcji lub dodać/ulepszyć jej część, to stwórz __Pull request__ z potrzebnymi zmianami.




## Słowniczek
* __Linux__ - Kernel stworzony przez Linusa Torwaldsa. Ma dostęp do całego urządzenia.
* __GNU/Linux__ - Kernel Linuxa wraz z wolnym oprogramowaniem GNU
* __Snap, Flatpak, Appimage__ - Paczki z oprogramowaniem, zawierające w sobie niezbędne zależności dzięki temu będące stabilne i niezależne od innych programów zainstalowanych w systemie
* __Terminal__ - Program w którym komendy wpisywane są w formie tekstowej
* __System Operacyjny__ -
* __Dystrybucja__ -
* __Lutris__ -
* __Repozytorium__ -
