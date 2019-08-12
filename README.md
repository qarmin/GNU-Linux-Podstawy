# GNU/Linux Podstawy

### Spis Treści
1. [Informacje o repozytorium](#informacje-o-repozytorium)
2. [Czym jest Linux i czy będzie dla mnie odpowiedni?](#czym-jest-linux-i-czy-będzie-dla-mnie-odpowiedni)
3. [Mity i Fakty](#mity-i-fakty)
4. [Dystrybucje, wydania LTS, dystrybucja ciągłe i cykliczne](#dystrybucje-wydania-lts-dystrybucja-ciągłe-i-cykliczne)
5. [Tworzenie Bootowalnego Pendriva](#tworzenie-bootowalnego-pendriva)
6. [Instalacja i Testowanie](#instalacja-i-testowanie)
7. [Konfiguracja Systemu](#konfiguracja-systemu)
8. [Granie na Linuxie](#granie-na-linuxie)
9. [Słowniczek](#słowniczek)
10. [Strony gdzie można znaleźć pomoc](#strony-fora-działy-i-tagi-związane-z-tematyką-linuxa-gdzie-możecie-znaleźć-pomoc)
11. [Strony z zaawansowanymi materiałami do nauki](#strony-z-zaawansowanymi-materiałami-do-nauki)
12. [Jak Pomóc](#jak-pomóc)

![800px-Neon-logo svg](https://user-images.githubusercontent.com/41945903/62884778-a4f6cf00-bd37-11e9-8120-873955186520.png)

### Informacje o repozytorium
To zawiera podstawowe informacje o jądrze Linux, bazującym na nim dystrybucjach, mitach i faktach itp.
Opisuję w nim również instrukcję instalacji oraz podstawowej konfiguracji systemu KDE Neon, którego sercem jest kernel Linux.

Jest ona przeznaczona dla początkujących osób, chcących zacząć przygodę z tym systemem.

### Czym jest Linux i czy będzie dla mnie odpowiedni?

Linux jest to jądro będące sercem systemu operacyjnego GNU/Linux i odpowiedzialne jest za obsługę sprzętu. Stworzone zostało w 1991 roku przez Linusa Torwaldsa, który ciągle współtworzy je wraz z tysiącami deweloperów z całego świata.

Linux jest dystrybuowany na licencji GPL 2, dzięki czemu można go używać kompletnie za darmo zarówno na użytek osobisty jak i komercyjny.

**Z racji swojej budowy i modelu licencjonowania nadaje się dla:**
* osób dbających o swoją prywatność
* ludzi troszczących się o swoje bezpieczeństwo w sieci
* programistów
* zarządzających sieciami komputerowymi
* zwykłych użytkowników
* retro i niedzielnych graczy
* graczy, którym nie straszne są wyzwania
* ludzi, którzy nie chcą wydawać pieniędzy na system operacyjny

**Mimo wszystko istnieją takie grupy użytkowników, dla których Linux jako główny system po prostu nie nadaje się:**
* hardcorowi gracze dla których liczy się każda klatka
* użytkownicy korzystający z oprogramowania nieistniejącego na Linuxie lub niepoprawnie działającego poprzez WINE
* osoby korzystające ze sterowników do urządzeń, których nie ma na Linuxie

### Mity i fakty
Wiele nieprawdziwych i przestarzałych informacji krąży na temat Linuxa

* **Sterowniki na Linuxa są tragicznej jakości** - **FAŁSZ**  
Jeszcze kilka/kilkanaście lat temu znaczna część producentów traktowała po macoszemu Linuxa i wydawane przez nich sterowniki były zamknięte oraz czasami słabej jakości. Dzisiaj większość czołowych producentów dostarcza kod swoich sterowników razem z kernelem, dzięki czemu razem ze wsparciem społeczności firmy takie jak Intel czy AMD, często przygotowują sterowniki, które obsługują np. wyższe wersje OpenGL i Vulkan lub likwidują błędy urządzeniach, które są już niewspierane na Windowsie.

* **Linux nie jest dobrym systemem dla graczy** - **Częściowo PRAWDA**  
Na początek trzeba rozgraniczyć trzy kategorie graczy:
 * Pierwszą z nich są tzw. retro gracze korzystający z różnej maści emulatorów różnych konsol do grania, takich jak Playstation 1, SNES czy Gamecube. Ogromna ilość takich narzędzi sprawia, że system Linux jest bardzo dobrym wyborem dla takich użytkowników.
 * Drugą z nich są osoby grające w gry nie oferujące zaawansowanej grafiki. Znaczna większość takich gier powinna bez większych problemów działać poprzez WINE i w zależności od tytułu wydajność powinna być porównywalna do gry uruchomionej na maszynie z Windowsem. Polski sklep [GOG](https://gog.com) oferuje ogromną ilość gier bez DRM, przeważnie świetnie działających pod Linuxem. Warto wspomnieć, że część gier, które nie działają poprawnie pod Windowsem 10, działa poprawnie na Linuxie.
 * Trzecią i ostatnią jest grupa zwykłych i hardkorowych graczy, którzy używają swojego sprzętu do uruchamiania zaawansowanych graficznie gier. Do czasu ogłoszenia Vulkan API, nie istniała technologia, za pomocą której można by było uruchamiać gry na Linuxie z wysoką wydajnością. Wszystko się zmieniło z jego wydaniem, które przyczyniły się do wydania takich programów jak D9VK, DXVK oraz VKD3D umożliwiających tłumaczenie odwołań DirectX 9, 10, 11 i 12 na multi-platformowego Vulkana, przeważnie zapewniając grom 70% - 90% wydajności z Windowsa a czasami działając na Linuxie płynniej i szybciej z powodu mniejszego narzutu sterowników.  
 Znacznym problemem jest używanie systemów anti-cheat niekompatybilnych z Linuxem ponieważ gry je używające, często banują błędnie banują graczy linuksowych lub nie pozwalają się uruchomić.

* **Na Linuxa nie ma komercyjnych programów** - **FAŁSZ**  
Część producentów komercyjnego oprogramowania jak np. Adobe od samego początku omija szerokim łukiem Linuxa, jednak znaczna część firm na czele z Autodesk widząc potencjał drzemiący w tym systemie oferuje na niego ogromną ilość programów. Rynek serwerowy, na którym króluje Linux, przynosi ogromne zyski dla wydawców takiego oprogramowania.

* **W Linuxie trzeba korzystać z konsoli** - **FAŁSZ**  
Znaczna część dystrybucji, a w szczególności te bazujące na Ubuntu(np. KDE Neon, Linux Mint), zdolna jest do obsługi systemu bez konieczności używania terminala. Trzeba jednak dodać, że znajomość podstawowych komend w terminalu, chociaż wydaje się nieco przytłaczająca dla nowych użytkowników, pozwala na sprawniejsze korzystanie z systemu.

* **Na Linuxa nie ma wirusów** - **FAŁSZ**  
Zwykły użytkownik Linuxa, prawdopodobnie nigdy nie spotka się z wirusem ponieważ tworzone robaki na ten system zwykle są dedykowane serwerom, gdyż na rynku komputerów Linux posiada jedynie niewielki procent rynku. Dodatkowo, zainstalowanie robaka w systemie wymagałoby świadomego jego uruchomienia.  
Aktualny system i oprogramowanie chroni również przed już załatanymi lukami, które cyberprzestępcy próbują użyć przeciwko niezałatanym systemom.

* **Linux to najczęściej używany system na świecie** - **PRAWDA**  
Linux jest obecny wszędzie, ogromna ilość komputerów, smartfonów, routerów, komputerów jedno-płytkowych, kamer, telewizorów posiada go wewnątrz siebie.  
System Android, znajdujący na większości telefonów, jest zbudowany wokół jądra Linux i jest obecny na ponad 2 miliardach urządzeń.

### Dystrybucje, wydania LTS, dystrybucja ciągłe i cykliczne

Podstawowym zagadnieniem, na który natkniesz się jest słowo **Dystrybucja**, które oznacza system operacyjny z jądrem Linuxa. Dystrybucje mogą od siebie wywodzić, dzięki czemu każda przejmuje część z ich właściwości. Takim przykładem jest Linux Mint, który wywodzi się od Ubuntu, który to natomiast pochodzi od Debiana.

Ważną informacją dla wielu użytkowników jest to, czy dana dystrybucja wspiera model wydań **LTS**. Takie wydania są obecne np. w Ubuntu i Linux Mint, 3 lub 5 lat w zależności od wersji, podczas gdy zwykłe wydania są wspierane jedynie przez 9 miesięcy.

W świecie Linuxa panuje podział na dwa typy dystrybucji, ciągłe i cykliczne.
* **Dystrybucja Ciągła** - Oferuje najnowsze dostępne programy i funkcje, lecz czasami nowsze wersje pakietów mogą powodować niestabilność systemu lub jego całkowite uszkodzenie. Korzystając z takich dystrybucji niemal jest konieczne posiadanie kopii zapasowej. Przykładami takich dystrybucji są: Arch Linux, Manjaro.
* **Dystrybucja Cykliczna** - Kolejne wersje systemu wydawane są co określony czas. Aktualizacje dotykają jedynie podstawowych pakietów i często dotyczą jedynie poprawek bezpieczeństwa. Przykładami takich dystrybucji są: Ubuntu, Linux Mint, Fedora

### Tworzenie Bootowalnego Pendriva
W tej instrukcji posłużę się bardzo przyjazną dystrybucją dla początkujących i nie tylko - KDE Neon z pulpitem KDE Plasma 5 bazującym na Ubuntu 18.04.  
Najnowszą dostępną wersję systemu należy [pobrać tutaj](https://files.kde.org/neon/images/user/current/neon-user-current.iso).

Potrzebujemy przygotować pendrive o minimalnym rozmiarze 4GB, by można było uruchomić z niego system.  
Część z systemów po wypakowaniu pliku ISO na pendriva powinna działać, lecz my dla pewności skorzystamy z programu [Etcher](https://www.balena.io/etcher/) obecnego na Linuxie, Windowsie i macOS.

Na początek uruchamiamy Etchera i naciskamy na przycisk **Select Image**, aby wybrać pobrany wcześniej plik ISO z systemem KDE Neon.  
Potem klikamy na **Select target**, aby wybrać pendrive na który chcemy zrzucić obraz(minimum 4 GB).  

**UWAGA** - *Wszystkie dane zawarte na pendrive zostaną skasowane*

Na koniec naciskamy **Flash** by rozpocząć proces wgrywania plików na pendriva.
![Screenshot_20190809_182443](https://user-images.githubusercontent.com/41945903/62882986-5e9f7100-bd33-11e9-825a-f4f8ccf9e3d5.png)
### Testowanie na maszynie wirtualna czy może na sprzęcie?
Testowanie systemu może mieć miejsce na:
* **Maszynie Wirtualnej** - System instalujemy, w programie typu VirtualBox, który umożliwia nam bezpieczne przetestowanie systemu.  
Plusem takiego rozwiązania, jest szybka możliwość przetestowania nawet wielu dystrybucji.
Minusem jednak jest konieczność posiadania wydajnego komputera, który umożliwiwi na uruchomienie dodatkowego systemu. Dodatkowo testując go na maszynie wirtualnej, nie mamy pewności jak dokładnie system będzie działał i czy będzie posiadał jakiekolwiek problemy
* **Na Sprzęcie** - System uruchamiamy z pendriva w trybie LiveCD, umożliwiającym nam dokładne przetestowanie systemu, bez konieczności jego instalacji. Do przetestowania kilku dystrybucji wymaga za każdym razem tworzenia nowego obrazu na pendrive i ponownego uruchomienia systemu.

### Instalacja i Testowanie
Po pierwsze musimy uruchomić system z pendriva, lecz sposób wejścia do Boot Menu jest zależny od posiadanej płyty głównej. Informacja ta powinna być podana na ekranie podczas włączania komputera, w instrukcji lub na stronie płyty głównej. Często są to klawisze F2, F8, F9, F10, F11, F12 czy ESC, więc można eksperymentować, aby znaleźć ich odpowiednią kombinację.  
Dostępnego menu menu wyboru wybieramy pendrive. W wypadku gdy na liście są dwa rekordy wybieramy ten z przydomkiem UEFI.

Naszym oczom powinien ukazać się pulpit systemu KDE Neon.

Teraz możemy dowolnie sprawdzać i używać Linuxa w trybie LiveCD i wszystkie dane po wyłączeniu tego systemu zostaną usunięte.

Aby zacząć instalację należy na pulpicie włączyć plik **Install neon user**.

Na początek wybieramy z menu języków wybieramy język polski.
![Screenshot_20190809_211817](https://user-images.githubusercontent.com/41945903/62882674-b689a800-bd32-11e9-8640-5c80ff75f739.png)
Potem jeśli chcemy to łączymy się z siecią bezprzewodową(sieć przewodowa łączy się automatycznie). Jest to bardzo przydatne, ponieważ dostęp do internetu umożliwi pobranie własnościowych sterowników oraz aktualizacji pakietów.

W następnym menu wybieramy układ klawiatury.
![Screenshot_20190809_212546](https://user-images.githubusercontent.com/41945903/62882677-b9849880-bd32-11e9-9c63-9a8766624702.png)

Następnie zalecam zaznaczenie opcji **Pobierz aktualizacje podczas instalowania neon** aby zainstalować aktualizacje systemu w czasie jego instalowania oraz **Install third-party software for graphics and Wi-Fi hardware and additional media formats** by zainstalować własnościowe sterowniki do poprawnego działania systemu.
![Screenshot_20190809_212639](https://user-images.githubusercontent.com/41945903/62882714-cef9c280-bd32-11e9-901e-efebdb90407c.png)

W kolejnym kroku, przechodzimy do konfiguracji dysków.  
Jeśli na dysku nie znajdują się żadne dane, lub usunięcie ich nie jest problemem, wtedy należy wybrać opcję **Przewodnik - cały dysk** oraz niżej wybrać dysk na jakim ma być system zainstalowany.  
W przypadku konieczności zainstalowania systemu obok Windowsa albo innego Linuxa lub koniecznością stworzenia niestandardowych partycji, należy wybrać opcję **Ręcznie**. Niestety jest to nieco skomplikowane oraz zależne od indywidualnej konfiguracji, dlatego polecam stworzenie wątku na forum lub tagu wspomnianym w paragrafie [Strony, fora, działy i tagi](#strony-fora-działy-i-tagi-związane-z-tematyką-linuxa-gdzie-możecie-znaleźć-pomoc).
Pragnę jedynie wspomnieć o podstawowych rzeczach związanych z tworzeniem partycji w tym trybie
- Punkt montowania / określa lokalizację w której zostanie zainstalowany systemy
- /home określa gdzie będą zapisywane informacje o użytkownikach, nie trzeba wtedy kopiować danych gdy system będzie ponownie instalowany
- Podstawowym systemem plików dla Linuxa jest EXT4 z księgowaniem
- Aby partycje były automatycznie montowane, należy je zamontować w lokalizacji /mnt/nazwa_partycji
- Ubuntu 17.04 i wzwyż i dystrybucje na nim bazujące tj. KDE Neon, nie tworzą już podczas instalacji osobnej partycji swap, gdyż od tej pory używa się pliku wymiany

![Screenshot_20190809_212702](https://user-images.githubusercontent.com/41945903/62882711-cdc89580-bd32-11e9-9b25-809661ebd89c.png)

Po zatwierdzeniu zmian w menedżerze dysków, rozpocznie się w tle proces instalacji systemu.
Musimy następnie wybrać naszą strefę czasową.
![Screenshot_20190809_214638](https://user-images.githubusercontent.com/41945903/62882801-f0f34500-bd32-11e9-88fa-45ebc473e752.png)

Na następnym ekranie tworzymy administratora urządzenia
Począwszy od góry wypełniamy
Imię i Nazwisko lub Pseudonim
Nazwę użytkownika pisaną małymi literami
Hasło wpisywane dwukrotnie aby uniknąć pomyłek(najlepiej będące zlepkiem kilku słów i znaków)
Nazwę Komputera(dobrze by było gdyby coś oznaczała)
Typ logowania - czy chcemy wpisywać hasło przy logowaniu, czy automatycznie ma się komputer logować na nasze konto
![Screenshot_20190809_214728](https://user-images.githubusercontent.com/41945903/62882806-f2247200-bd32-11e9-9516-9c814ba9228b.png)

Po tym kroku czekamy na zakończenie instalacji, po której możemy wybrać, czy dalej chcemy testować system czy chcemy uruchomić ten zainstalowany.
![Screenshot_20190809_225353](https://user-images.githubusercontent.com/41945903/62882892-2c8e0f00-bd33-11e9-865b-06ef4aa98050.png)

Powinna po próbie uruchomienia ponownie komputera wyskoczyć informacja o konieczności wysunięcia pendriva i naciśnięciem Entera

### Konfiguracja Systemu
Po zakończeniu instalacji systemu, możemy w końcu zalogować się na swoje konto. Użytkownicy kart graficznych AMD i Intela(zintegrowanych), mogą po lewej stronie na dole wybrać opcję Plasma Wayland, która zapobiega występowania "rwania" obrazu.
![Screenshot_20190809_233033](https://user-images.githubusercontent.com/41945903/62882913-3adc2b00-bd33-11e9-9081-7197f336f3eb.png)
Naszym oczom powinien ukazać się pulpit, przypominający wyglądem i działaniem ten z Windowsa.
Po lewej stronie na dole widzimy aktywator programów, umożliwiający przeglądanie zainstalowanych programów, można go również otworzyć klawiszem Super znajdującym się obok lewego klawisza Ctrl oraz prawego Alt.
Po prawej stronie na dole znajduje się pasek zadań, w którym to znajdują się opcje umożliwiające połączenie z siecią, sprawdzenie jasności czy połączenie komputera z telefonem.
Po skierowaniu myszy na lewy górny róg, w czasie gdy mamy uruchomione kilka okien, powinniśmy zobaczyć podgląd ich wszystkich
Po prawej stronie u góry znajduje się menu opcji Pulpitu w którym możemy choćby zmienić tapetę.
![Screenshot_20190812_190234](https://user-images.githubusercontent.com/41945903/62883195-c8b81600-bd33-11e9-8b3a-ff9405b76ffe.png)

Mimo, że system jest już wstępnie skonfigurowany, to niektóre rzeczy według mnie wymagają zmiany
#### Ciągłe pytanie o hasło do WiFi
System z domyślnymi ustawieniami zapisze hasło do WiFi w Portfelu będącym menedżerem haseł. Przy każdym uruchomieniu systemu, będzie trzeba podać hasło do portfela celem uruchomienia WiFi. Hasło może być przechowywane poza portfelem co oszczędzi nam nerwów podczas kolejnej próby wpisywania hasła.
Aby to zrobić należy uruchomić Aktywator Programów, wyszukać i uruchomić program **Połączenia**.
Wybieramy z lewej strony połączenie WiFi o które nam chodzi, wtedy po prawej przechodzimy do zakładki **Zabezpieczenie Wi-Fi**, wpisujemy tam hasło i wybieramy opcję *Zachowaj dla wszystkich użytkowników (nieszyfrowane)*
Zatwierdź to klikając OK.
![Screenshot_20190809_234417](https://user-images.githubusercontent.com/41945903/62883393-41b76d80-bd34-11e9-8401-50b051da5ca2.png)
#### Ciemny Motyw
Domyślny motyw jest dla mnie, jak i wielu zbyt jasny.
Aby to zmienić należy uruchomić Aktywator Programów i wyszukać i uruchomić ustawienia systemowe.
W zakładce *Wrażenia wzrokowe i dotykowe* wybieramy motyw **Ciemna bryza** i zatwierdzamy to za pomocą przycisku Zastosuj.
Dodatkowo programy GTK wymagają aby zmienić również w zakładce *Wygląd Programów* -> *Wygląd aplikacji GNOME/GTK* ustawienia *Wygląd GTK2* i *Wygląd GTK3* na **Breeze-dark** oraz nieco niżej *Zestaw ikon* oraz *Zestaw Zapasowy* na **Ciemna Bryza**
#### Jeden klik zamiast dwóch otwiera foldery/pliki
Domyślnie jeden klik w przeciwieństwie do Windowsa i innych środowisk otwiera plik. Aby to zmienić należy przejść do zakładki w ustawieniach systemowych *Zachowanie Pulpitu* -> *Przestrzeń Robocza* i zaznaczyć opcję **Dwukrotne kliknięcie otwiera pliki i katalogi**
#### Przywracanie okien po wyłączeniu komputera
KDE Plasma przywraca sesję po ponownym uruchomieniu komputera, która to przywraca wszystkie okna sprzed restartu. Aby temu zapobiec, należy w ustawieniach w zakładce *Uruchamianie i wyłączanie* -> *Sesja pulpitu* zaznaczyć opcję w sekcji *Przy logowaniu* opcję **Rozpocznij pustą sesję**
![Screenshot_20190812_190738](https://user-images.githubusercontent.com/41945903/62883499-79261a00-bd34-11e9-9892-8700975a8840.png)
#### Potwierdzanie wyjścia z systemu
Domyślnie Plasma, po próbie zamknięcia lub wylogowania się z systemu, pokazuje 30-sekundowe okno, podczas gdy jest wyświetlone, możemy jeszcze zmienić decyzję.
Aby je wyłączyć należy przejść do Ustawień systemowych i w zakładce **Uruchamianie i wyłączanie**->**Sesja pulpitu** odznaczyć opcję **Wylogowuj za potwierdzeniem** oraz zaznacz opcję **Wyłącz Komputer** w dziale **Przy Wychodzeniu**
#### Niepełne wsparcie dla języka polskiego
Aby dodać pełne wsparcie dla języka polskiego, należy w ustawieniach systemowych w zakładce *Ustawienia regionalne* -> *Język* dodać język polski, zatwierdzić zmiany oraz wylogować się//uruchomić ponownie komputera
#### Instalacja Programów
Aby zainstalować różne aplikacje, należy skorzystać z programu *Odkrywca*, który można znaleźć w Aktywatorze programów.
Listę dostępnego darmowego oprogramowania znajdziesz tutaj [Rewelacyjne OpenSource](https://github.com/qarmin/Rewelacyjne-OpenSource)
![Screenshot_20190809_234417](https://user-images.githubusercontent.com/41945903/62883545-91963480-bd34-11e9-9ab0-114726e73c4f.png)
#### Aktualizacja systemu i Programów
Podstawą bezpiecznego systemu jest jego częste aktualizowanie.
W Linuxie aktualizacja systemu jest powiązana z aktualizacją programów, dzięki czemu nie będziemy posiadać niebezpiecznego nieaktualnego oprogramowania.
Aby zaktualizować system musimy najpierw otworzyć program *Odkrywca*, który otwieramy poprzez Aktywator Programów. Następnie przechodzimy do zakładki *Uaktualnienia* znajdującej się w lewym dolnym rogu programu.
Po odczekaniu chwili potrzebnej na pobranie informacji na temat dostępnych aktualizacji, należy w prawym górnym rogu nacisnąć na przycisk *Uaktualnij wszystko*
Będziemy musieli podać hasło do konta, aby umożliwić instalacje pakietów.
**UWAGA** - *Zalecane jest, aby uruchomić ponownie komputer po aktualizacji, aby uniknąć niepożądanych zachowań systemu*
**UWAGA** - *Aktualizację systemu powinno się wykonywać co najmniej 1 raz w miesiącu(im częściej, tym lepiej)*
![Screenshot_20190810_091702](https://user-images.githubusercontent.com/41945903/62883565-9f4bba00-bd34-11e9-93d9-a58b3e1a5ecc.png)
#### Sterowniki do karty graficznej
Intel oraz AMD domyślnie posiadają sterowniki do swoich kart graficznych w bilbiotece graficznej Mesa, dostępnej domyślnie na większości dystrybucji, w tym w KDE Neon, których aktualizacja przebiega wraz z aktualizacją systemu.

Do kart Nvidii również został przygotowany otwartoźródłowy sterownik *nouveau*, lecz poprzez szereg decyzji Nvidii, mających na celu zablokowanie jego rozwoju, *nouveau* nie nadaje się do codziennego użytku na nowszych kartach graficznych, dlatego trzeba posłużyć się zamkniętym sterownikiem.
Jego instalacja jest prosta, lecz wymaga otworzenia konsoli, którą można uruchomić z Aktywatora Programów lub za pomocą skrótu klawiszowego **CTRL + ALT + T**
//TODO

### Granie na Linuxie
Granie na Linuxie niegdyś wymagało by gracz posiadał duże umiejętności aby zainstalować grę, która, jeśli się uruchamiała, działała często z niewielką wydajnością.
Te czasy się na szczęście minęły dzięki takim firmom jak AMD i Intel, które udostępniły otwartoźródłowe sterowniki do swoich kart graficznych i umożliwiły wprowadzanie do nich łatek przez zewnętrznych deweloperów, czy Valve oraz Codewavers tworzącymi narzędzia emulujące gry Windowsowe i ulepszającymi poszczególne komponenty kernela poprawiając osiągi gier.

Najprostszym, niewymagającym żadnej wiedzy i najczęściej stosowanym rozwiązaniem jest zainstalowanie [Steama](https://store.steampowered.com/about/). Firma Valve bardzo przysłużyła się Linuxowej społeczności graczy, tworząc szereg narzędzi na czele z Protonem, umożliwiających w granie w gry przeznaczone na system Windows za pomocą jednego kliknięcia. Listę działających gier z użyciem tego narzędzia można [znaleźć tutaj](https://www.protondb.com/).

Do starszych lub niewymagających dużej mocy obliczeniowej gier zwykle nie potrzeba nic instalować oprócz Wine dostępnego w repozytorium - Instalacja wymagająca skopiowania kilku poleceń w języku angielskim [znajduje się tutaj](https://wiki.winehq.org/Ubuntu).

W przypadku zainstalowania [Lutris](https://lutris.net/) do zarządzania grami, również potrzebna będzie instalacja Wine. Za jego pomocą, możemy prosto instalować zoptymalizowane wersje Wine, używać Esync poprawiającego wydajność gier czy DXVK umożliwianego uruchamianie gier DX11 z pomocą Vulkan API. Szczegółowe instrukcje [znajdują się tutaj](https://github.com/lutris/lutris/wiki)
![Screenshot_20190810_101842](https://user-images.githubusercontent.com/41945903/62883919-8a235b00-bd35-11e9-80ed-af615037b15c.png)
### Słowniczek
* **Linux** - Kernel stworzony przez Linusa Torwaldsa. Odpowiedzialny jest za wszystkie zadania systemu operacyjnego.
* **GNU/Linux** - Kernel Linuxa dystrybuowany z wolnym oprogramowaniem GNU
* **Snap, Flatpak, Appimage** - Paczki z oprogramowaniem, zawierające w sobie niezbędne zależności dzięki temu będące niezależne od innych programów zainstalowanych w systemie.
* **Terminal** - Program w którym można wydawać polecenia bez konieczności korzystania z graficznego interfejsu użytkownika
* **System Operacyjny** - Oprogramowanie zarządzające fizycznymi elementami komputera, bez którego nie możnaby było uruchomić żadnych programów.
* **Dystrybucja** - Jest to system operacyjny dystrybuowany z jądrem Linuxa, posiadający szereg wbudowanych programów.
* **Lutris** - Program do zarządzania grami/aplikacjami, uproszczający używanie WINE, DXVK czy Esync.
* **Repozytorium** - Jest to miejsce, gdzie znajdują się różne programy.
* **PPA** - Są to repozytoria tworzone przez np. twórcy aplikacji, by zapewnić użytkownikowi najnowszą wersję programów.

### Strony, fora, działy i tagi związane z tematyką Linuxa gdzie możecie znaleźć pomoc
* wykop.pl - [tag Linux](https://www.wykop.pl/tag/linux)
* forum.dobreprogramy.pl - [kategoria GNU/Linux](https://forum.dobreprogramy.pl/c/oprogramowanie-komputerowe/gnu-linux)
* forum.linux.pl - [forum Linux](https://forum.linux.pl/)
* linuxiarze.pl - [forum Linuxiarze](https://linuxiarze.pl/forum/)

### Strony z zaawansowanymi materiałami do nauki
* [Linux Jouney](https://www.linuxjourney.com)

### Jak Pomóc?
* **Udostępniaj** - Byłbym wdzięczny, gdybyś rozpowszechnił ją wśród znajomych, rodziny czy na Facebooku.
* **Zgłaszaj błędy** - Jeśli znalazłeś błąd w instrukcji, lub jej część jest dla ciebie niejasna, to zgłoś to w zakładce **Issues**
* **Dodawaj i naprawiaj treści** - Jeśli chcesz naprawić błąd w instrukcji lub dodać/ulepszyć jej część, to stwórz **Pull Request** z potrzebnymi zmianami.
