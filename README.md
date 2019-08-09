# GNU/Linux Podstawy

### Spis Treści
1. [Informacje o repozytorium](#informacje-o-repozytorium)
2. [Jak Pomóc?](#jak-pomóc)  
3. [Podstawowe informacje](#podstawowe-informacje)
4. [Instalacja Linuxa](#instalacja-linuxa)
5. [Granie na Linuxie](#granie-na-linuxie)  
6. [Słowniczek](#słowniczek)  

### Informacje o repozytorium
Ta instrukcja zawiera podstawowe informacje o systemie GNU/Linux, jego zastosowaniach, instalacji, podstawowej konfiguracji oraz użytkowaniu.

Jest ona przeznaczona dla początkujących osób, chcących zacząć przygodę z systemem, będąc wyposażonym w podstawową wiedzę oraz narzędzia.

### Podstawowe informacje
GNU/Linux jest uniksopodobnym systemem operacyjnym korzystającym z jądra Linux. Jądro to jest najważniejszą składową systemu operacyjnego, mającym pełną kontrolę nad tym urządzeniem.
W przeciwieństwie do Windowsa nie istnieją w nim litery dysków, wszystkie foldery i pliki znajdują się w głównym katalogu / i np. pulpit użytkownika qarmin znajduje się w lokalizacji /home/qarmin/Pulpit

### Dla kogo Linux?

Linux z racji swojej budowy i modelu licencjonowania nadaje się przede wszystkim dla:
* ludzi dbających o swoją prywatność
* ludzi troszczących się o swoje bezpieczeństwo w sieci
* programistów
* zarządzających sieciami komputerowymi
* zwykłych użytkowników
* retro i niedzielnych graczy
* graczy, którym nie straszne są wyzwania

Mimo wszystko istnieją takie grupy użytkowników, dla których Linux jako główny system po prostu nie nadaje się:
* hardcorowi gracze dla których liczy się każda klatka
* użytkownicy korzystający z oprogramowania nieistniejącego na Linuxie lub niepoprawnie działającego poprzez WINE

Dla tych wszystkich osób, które nie mogą zainstalować Linuxa jako główny system, zachęcam do jego instalacji w trybie dualboot obok Windowsa

### Mity i fakty
Wiele nieprawdziwych i przestarzałych informacji krąży na temat Linuxa

* Sterowniki na Linuxa są tragicznej jakości - FAŁSZ  
Jeszcze kilka/kilkanaście lat temu znaczna część producentów traktowała po macoszemu Linuxa i wydawane przez nich sterowniki były zamknięte oraz czasami słabej jakości. Dzisiaj większość producentów dostarcza kod swoich sterowników razem z kernelem, dzięki czemu razem ze wsparciem społeczności firmy takie jak Intel czy AMD, przygotowują lepsze sterowniki niż na Windowsie, często obsługujące wyższe wersje OpenGL i Vulkan.
* Linux nie jest dobrym systemem dla graczy - PRAWDA(Lecz zmienia się to coraz bardziej)  
Wiele gier, które mają premierę na Windowsie, nigdy nie dostaje portu na Linuxa lecz. Ten problem jest częściowo rozwiązany przez D9VK, DXVK oraz VKD3D, które umożliwiają translację odwołań DirectX 9, 10, 11 i 12 na multiplatformowy Vulkan, zapewniając przeważnie 70% - 90% wydajności, a niekiedy wydajność na Linuxie jest większa z powodu mniejszego narzutu sterowników. Zdarza się, że starsze gry, które nie wcale uruchamiają się na Windowsie lub działają z błędami, uruchamiają się bez problemów na Linuxie.
* Na Linuxa nie ma wcale komercyjnych programów - FAŁSZ  
Część producentów oprogramowania omija szerokim łukiem Linuxa, mimo, że niektóre firmy pokroju Autodesk od całkiem dawna tworzą oprogramowanie na ten system.
* W Linuxie trzeba korzystać z konsoli - FAŁSZ  
Znaczna część dystrybucji, a w szczególności te bazujące na Ubuntu(np. KDE Neon, Linux Mint), zdolna jest obsługi systemu bez konieczności używania terminala. Trzeba jednak dodać, że znajomość podstawowych komend w terminalu, chociaż wydaje się nieco przytłaczająca dla nowych użytkowników, pozwala na sprawniejsze korzystanie z systemu.
* Na Linuxa nie ma wirusów - FAŁSZ
Zwykły użytkownik Linuxa, prawdopodobnie nigdy nie spotka się z wirusem ponieważ tworzone robaki na ten system zwykle są dedykowane serwerom, gdyż na rynku komputerów Linux posiada jedynie niewielki procent rynku. Dodatkowo, zainstalowanie robaka w systemie wymagałoby świadomego wpisania hasła.  

### Dystrybucje, wydania LTS, dystrybucja ciągłe i cykliczne

Podstawowym zagadnieniem, na który natkniesz się jest słowo __Dystrybucja__, które oznacza system operacyjny z jądrem Linuxa. Dystrybucje mogą od siebie wywodzić, dzięki czemu każda przejmuje część z ich właściwości. Takim przykładem jest Linux Mint, który wywodzi się od Ubuntu, który to natomiast pochodzi  od Debiana.

Ważną dla wielu użytkowników, jest posiadanie przez niektóre dystrybucje __Wydań LTS__. Takie wydania są wspierane np. w Ubuntu i Linux Mint 5 lub 3 Lata w zależności od wersji, podczas gdy zwykłe wydania są wspierane jedynie przez 9 miesięcy.

W świecie Linuxa panuje podział na dwa typy dystrybucji, ciągłą i cykliczną.
* Dystrybucja Ciągła - Oferuje najnowsze dostępne aktualizacje, lecz nowsze wersje programów mogą powodować różne problemy, nawet takie jak niemożność uruchomienia systemu. Przykładami takich dystrybucji są: Arch Linux czy Manjaro.
* Dystrybucja Cykliczna -  Przykładami takich dystrybucji są: Ubuntu, Linux Mint, Fedora

### Tworzenie Bootowalnego Pendriva
W tej instrukcji posłużę się bardzo przyjazną dystrybucją dla początkujących i nie tylko - KDE Neon z KDE Plasma 5.  
Najnowszą dostępną wersję systemu należy [pobrać tutaj](https://files.kde.org/neon/images/user/current/neon-user-current.iso).

Potrzebujemy przygotować pendrive z minimalnym rozmiarem 4GB, by można było uruchomić z niego system.  
Część z systemów po wypakowaniu pliku ISO na pendriva powinna działać, lecz my skorzystamy na Windowsie z programu [Etcher](https://www.balena.io/etcher/) wspierającego również Linuxa.  

Na początek uruchamiamy Etcher i naciskamy na przycisk *Select Image*, aby wybrać pobrany wcześniej plik ISO z systemem KDE Neon.  
Potem klikamy na *Select target*, aby wybrać pendrive na który chcemy zrzucić obraz(minimum 4 GB).  
**UWAGA - wszystkie dane zawarte na pendrive zostaną skasowane**
Na koniec naciskamy Flash by rozpocząć proces wgrywania plików na pendriva.
### Testowanie na maszynie wirtualna czy może na sprzęcie?
Testowanie systemu może odbyć się w dwóch trybach:
* w maszynie wirtualnej(przydatne przy sprawdzaniu wyglądu i funkcji)
* na sprzęcie(przydatne do sprawdzania jak radzi sobie system na urządzeniu)
Uważam, że najlepiej jest sprawdzić Linuxa na "żywym" sprzęcie, gdyż da to nam informacje czy na takiej konfiguracji, nie występują żadne problemy

### Instalacja i Testowanie
Po pierwsze musimy uruchomić system z pendriva, lecz sposób wejścia do Boot Menu jest zależny od posiadanej płyty głównej. Informacja powinna być podana na ekranie podczas włączania komputera, instrukcji lub na stronie płyty głównej. Często są to klawisze F2, F8, F9, F10, F11, F12 czy ESC, więc można eksperymentować, dopóki nie naciśnie się odpowiedniego klawisza/kombinacji klawiszy.  
Dostępnego menu menu wyboru wybieramy pendrive. W wypadku gdy na liście są dwa rekordy wybieramy ten z przydomkiem UEFI.  

Naszym oczom powinien ukazać się pulpit systemu KDE Neon.
Teraz możemy dowolnie sprawdzać i używać Linuxa w trybie LiveCD i wszystkie dane po wyłączeniu tego systemu zostaną usunięte.

Aby zacząć instalację należy na pulpicie włączyć plik **Install neon user**.  
**UWAGA Domyślnie pliki na pulpicie i eksploratorze plików w Plazmie uruchamia się za pomocą pojedynczego kliknięcia**
Na początek wybieramy z menu języków wybieramy język polski.

Potem jeśli chcemy to łączymy się z siecią bezprzewodową(sieć przewodowa łączy się automatycznie). Jest to bardzo przydatne, ponieważ dostęp do internetu umożliwi pobranie własnościowych sterowników oraz aktualizacji pakietów.

W następnym menu wybieramy układ klawiatury.

Następnie zalecam zaznaczenie opcji **Pobierz aktualizacje podczas instalowania neon** aby zainstalować aktualizacje systemu w czasie jego instalowania oraz **Install third-party software for graphics and Wi-Fi hardware and additional media formats** by zainstalować własnościowe sterowniki do poprawnego działania systemu.

W kolejnym kroku, przechodzimy do konfiguracji dysków.
Jeśli na dysku nie znajdują się żadne dane, lub usunięcie ich nie jest problemem, wtedy należy wybrać opcję **Przewodnik - cały dysk** oraz niżej wybrać dysk na jakim ma być system zainstalowany.
W przypadku konieczności zainstalowania systemu obok Windowsa albo innego Linuxa lub koniecznością stworzenia niestandardowych partycji, należy wybrać opcję **Ręcznie**. Niestety jest to nieco skomplikowane oraz zależne od indywidualnej konfiguracji, dlatego polecam stworzenie wątku na forum lub tagu wspomnianym w paragrafie [Strony, fora, działy i tagi]().
Pragnę jedynie wspomnieć o podstawowych rzeczach związanych z tworzeniem partycji w tym trybie
- Punkt montowania / określa lokalizację w której zostanie zainstalowany systemy
- /home określa gdzie będą zapisywane informacje o użytkownikach, nie trzeba wtedy kopiować danych gdy system będzie ponownie instalowany
- Podstawowym systemem plików dla Linuxa jest EXT4 z księgowaniem
- Aby partycje były automatycznie montowane, należy je zamontować w lokalizacji /mnt/nazwa_partycji
- Ubuntu 17.04 i wzwyż i dystrybucje na nim bazujące tj. KDE Neon, nie tworzą już podczas instalacji osobnej partycji swap, gdyż od tej pory używa się pliku wymiany

Po zatwierdzeniu zmian w menedżerze dysków, rozpocznie się w tle proces instalacji systemu.
Musimy następnie wybrać naszą strefę czasową.

Na następnym ekranie tworzymy administratora urządzenia
Począwszy od góry wypełniamy
Imię i Nazwisko lub Pseudonim
Nazwę użytkownika pisaną małymi literami
Hasło wpisywane dwukrotnie aby uniknąć pomyłek(najlepiej będące zlepkiem kilku słów i znaków)
Nazwę Komputera(dobrze by było gdyby coś oznaczała)
Typ logowania - czy chcemy wpisywać hasło przy logowaniu, czy automatycznie ma się komputer logować na nasze konto

Po tym kroku czekamy na zakończenie instalacji, po której możemy wybrać, czy dalej chcemy testować system czy chcemy uruchomić ten zainstalowany.

Powinna po próbie uruchomienia ponownie komputera wyskoczyć informacja o konieczności wysunięcia pendriva i naciśnięciem Entera

### Konfiguracja Systemu
Po zakończeniu instalacji systemu, możemy w końcu zalogować się na swoje konto. Użytkownicy kart graficznych AMD i Intela(zintegrowanych), mogą po lewej stronie na dole wybrać opcję Plasma Wayland, która zapobiega występowania "rwania" obrazu.

Naszym oczom powinien ukazać się pulpit, przypominający wyglądem i działaniem ten z Windowsa.
Po lewej stronie na dole widzimy aktywator programów, umożliwiający przeglądanie zainstalowanych programów, można go również otworzyć klawiszem Super znajdującym się obok lewego klawisza Ctrl oraz prawego Alt.
Po prawej stronie na dole znajduje się pasek zadań, w którym to znajdują się opcje umożliwiające połączenie z siecią, sprawdzenie jasności czy połączenie komputera z telefonem.
Po skierowaniu myszy na lewy górny róg, w czasie gdy mamy uruchomione kilka okien, powinniśmy zobaczyć podgląd ich wszystkich
Po prawej stronie u góry znajduje się menu opcji Pulpitu w którym możemy choćby zmienić tapetę.

Mimo, że system jest już wstępnie skonfigurowany, to niektóre rzeczy według mnie wymagają zmiany
#### Ciągłe pytanie o hasło do WiFi
System z domyślnymi ustawieniami zapisze hasło do WiFi w Portfelu będącym menedżerem haseł. Przy każdym uruchomieniu systemu, będzie trzeba podać hasło do portfela celem uruchomienia WiFi. Hasło może być przechowywane poza portfelem dzięki czemu nie potrzeba ciągle do niego wpisywać hasła.
Aby to zrobić należy uruchomić Aktywator Programów i wyszukać i uruchomić program **Połączenia**.
Wybieramy z lewej strony połączenie WiFi o które nam chodzi, wtedy po prawej przechodzimy do zakładki **Zabezpieczenie Wi-Fi**, wpisujemy tam hasło i wybieramy opcję *Zachowaj dla wszystkich użytkowników (nieszyfrowane)*
Zatwierdź to klikając OK.
#### Ciemny Motyw
Domyślny motyw jest dla mnie, jak i wielu zbyt jasny.
Aby to zmienić należy uruchomić Aktywator Programów i wyszukać i uruchomić ustawienia systemowe.
W zakładce *Wrażenia wzrokowe i dotykowe* wybieramy motyw **Ciemna bryza** i zatwierdzamy to za pomocą przycisku Zastosuj.
Dodatkowo programy GTK wymagają aby zmienić również w zakładce *Wygląd Programów* -> *Wygląd aplikacji GNOME/GTK* ustawienia *Wygląd GTK2* i *Wygląd GTK3* na **Breeze-dark** oraz nieco niżej *Zestaw ikon* oraz *Zestaw Zapasowy* na **Ciemna Bryza**
#### Jeden klik zamiast dwóch otwiera foldery/pliki
Domyślnie jeden klik w przeciwieństwie do Windowsa i innych środowisk otwiera plik. Aby to zmienić należy przejść do zakładki w ustawieniach systemowych *Zachowanie Pulpitu* -> *Przestrzeń Robocza* i zaznaczyć opcję **Dwukrotne kliknięcie otwiera pliki i katalogi**
#### Przywracanie okien po wyłączeniu komputera
KDE Plasma przywraca sesję po ponownym uruchomieniu komputera, która to przywraca wszystkie okna sprzed restartu. Aby temu zapobiec, należy w ustawieniach w zakładce *Uruchamianie i wyłączanie* -> *Sesja pulpitu* zaznaczyć opcję w sekcji *Przy logowaniu* opcję **Rozpocznij pustą sesję**
#### Niepełne wsparcie dla języka polskiego
Aby dodać pełne wsparcie dla języka polskiego, należy w ustawieniach systemowych w zakładce *Ustawienia regionalne* -> *Język* dodać język polski, zatwierdzić zmiany oraz wylogować się//uruchomić ponownie komputera
#### Instalacja Programów
Aby zainstalować różne aplikacje, należy skorzystać z programu *Odkrywca*, który można znaleźć w Aktywatorze programów.
Listę dostępnego darmowego oprogramowania znajdziesz tutaj [Rewelacyjne OpenSource](https://github.com/qarmin/Rewelacyjne-OpenSource) 

#### Aktualizacja systemu i Programów



### Granie na Linuxie
Jak już wcześniej wspominałem granie na Linuxie niegdyś wymagało by gracz posiadał duże umiejętności aby zainstalować grę, która, jeśli się uruchamiała, działała z bardzo małą wydajnością.
Te czasy się na szczęście zmieniły dzięki takim firmom jak AMD i Intel, udostępniającymi otwartoźródłowe sterowniki czy Valve oraz Codewavers tworzącymi narzędzia emulujące gry Windowsowe i ulepszającymi poszczególne komponenty kernela
Do retro gier i gier niewymagających dużej mocy obliczeniowej zwykle nie potrzeba nic instalować oprócz Wine dostępnego w repozytorium lub poprzez Lutris.


### Jak Pomóc?
* __Udostępniaj__ - Byłbym wdzięczny, gdybyś rozpowszechnił ją wśród znajomych, rodziny czy na Facebooku.
* __Zgłaszaj błędy__ - Jeśli znalazłeś błąd w instrukcji, lub jej część jest dla ciebie niejasna, to zgłoś to w zakładce __Issues__
* __Dodawaj i naprawiaj treści__ - Jeśli chcesz naprawić błąd w instrukcji lub dodać/ulepszyć jej część, to stwórz __Pull Request__ z potrzebnymi zmianami.


### Słowniczek
* __Linux__ - Kernel stworzony przez Linusa Torwaldsa. Odpowiedzialny jest za wszystkie zadania systemu operacyjnego.
* __GNU/Linux__ - Kernel Linuxa wraz dystrybuowany z wolnym oprogramowaniem GNU
* __Snap, Flatpak, Appimage__ - Paczki z oprogramowaniem, zawierające w sobie niezbędne zależności dzięki temu będące stabilne i niezależne od innych programów zainstalowanych w systemie
* __Terminal__ - Program w którym komendy wpisywane są w formie tekstowej
* __System Operacyjny__ - Oprogramowanie zarządzające fizycznymi elementami komputera i zapewniające funkcje do uruchamiania programistów
* __Dystrybucja__ -
* __Lutris__ - Program do zarządzania grami/aplikacjami, uproszczający używanie WINE, DXVK czy Esync
* __Repozytorium__ - Jest to miejsce, gdzie znajdują się różne programy.
* __

### Strony, fora, działy i tagi związane z tematyką Linuxa gdzie możecie znaleźć pomoc
* wykop.pl - [tag Linux](https://www.wykop.pl/tag/linux)
* forum.dobreprogramy.pl - [kategoria GNU/Linux](https://forum.dobreprogramy.pl/c/oprogramowanie-komputerowe/gnu-linux)

### Zaawansowane strony z materiałami do nauki
* [Linux Jouney](https://www.linuxjourney.com)
