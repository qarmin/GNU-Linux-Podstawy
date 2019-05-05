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
* W Linuxie trzeba korzystać z konsoli - FAŁSZ

## Dystrybucje


W tej instrukcji posłużę się bardzo przyjazną dystrybucją Kubuntu z KDE Plasma 5.

## Tworzenie Bootowalnego Pendriva
Na początek musimy pobrać obraz systemu ze strony. Zalecam skorzystanie z pliku torrent, oraz wolnego i otwartego programu [QBittorrent](), dzięki czemu będziemy mogli ściągnąć plik ISO całą szerokością łącza.

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
Tekst został przygotowany na systemie Kubuntu z KDE Plasma 5

## Granie na linuxie
Jak już wcześniej wspominałem granie na Linuxie jest możliwe mimo pewnych niedogodności.
Do retro gier i gier niewymagających dużej mocy obliczeniowej zwykle nie potrzeba nic instalować oprócz Wine


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
