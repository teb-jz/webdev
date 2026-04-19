
<a name = "projekty"></a>
# Projekty

## 1. Sygnalizacja świetlna

Aplikacja do sterowania sygnalizacją świetlną, opierająca się na czterofazowym układzie.

![Sygnalizcja czterofazowa](img/sygnalizacja.png "Sygnalizcja czterofazowa")

#### Funkcjonalności:

- Graficzna reprezentacja trzech świateł sygnalizacji - czerwone, żółte i zielone.
- Wyświetlanie obecnego stanu sygnalizacji.
- Tryb ręczny - zmiana stanu sygnalizacji po naciśnięciu przycisku.
- Tryb automatyczny - automatyczna zmiana stanu sygnalizacji po określonym czasie.
- Możliwość wybierania trybu.
- Odliczanie do zmiany stanu w trybie automatycznym.

## 2. Winda

Symulator działania windy w budynku wielopiętrowym. Użytkownik ma możliwość wyboru piętra, na które zostanie wezwana winda.

- Graficzna reprezentacja windy i pięter.
- Przycisk przywoływania windy na każdym piętrze.
- Przyciski odnoszące się do poszczególnych pięter.
- Animacja przejazdu windy.
- Wyświetlanie aktualnego piętra i kierunku jazdy.

## 3. Parking

Symulator parkingu samochodowego, pozwalający na obserwowanie zajętości miejsc.

#### Funkcjonalności:

- Graficzna reprezentacja parkingu, w zależności od wymiarów podanych przez użytkownika.
- Mechanika zwalniania i zajmowania miejsc - zmiana statusu po kliknięciu.
- Licznik zajętych i wolnych miejsc, wyświetlanie obłożenia w procentach.
- Reset parkingu - zwolnienie miejsc i zresetowanie liczników.
- Podział na tryb ręczny i automatyczny. W trybie automatycznym, co kilka sekund, miejsca są losowo zwalniane i zajmowane.

## 4. Lista obecności

Aplikacja do zarządzania listą uczniów i oznaczania ich obecności na zajęciach.

Funkcjonalności:

- Wyświetlanie listy uczniów.
- Dodawanie nowych uczniów poprzez formularz.
- Usuwanie uczniów z listy.
- Możliwość wybrania jednego z trzech stanów - obecność, nieobecność, spóźnienie, przy danym uczniu.
- Licznik obecnych, nieobecnych oraz spóźnionych uczniów.
- Filtrowanie listy uczniów po stanie obecności.

## 5. Dziennik ocen (*)

Symulator prostego dziennika szkolnego.

Funkcjonalności:

- Wyświetlanie listy uczniów oraz ich ocen.
- Możliwość dodawania nowych uczniów poprzez formularz.
- Możliwość usuwania uczniów z listy.
- Możliwość wpisywania ocen o podanej kategorii, wadze, opisie oraz dacie wstawienia. Kategoria powinna być wybierana spośród istniejących. Data powinna pokrywać się z czasem wstawienia oceny, chyba że użytkownik zadecyduje inaczej.
- Możliwość usuwania ocen.
- Obliczanie i wyświetlanie średniej ocen danego ucznia.
- Sortowanie listy uczniów po numerze w dzienniku, alfabetycznie po nazwisku oraz po średniej.
- Filtrowanie listy uczniów po nazwisku lub progu średniej.

## 6. Sterownik klimatyzacji

Aplikacja symulująca panel sterowania klimatyzacją, umożliwiającą użytkownikowi kontrolę temperatury i trybu pracy urządzenia.

Funkcjonalności:

- Wyświetlanie aktualnej temperatury.
- Możliwość ustalenia temperatury docelowej.
- Wybór trybu pracy - chłodzenie, ogrzewanie, wentylacja, wyłączone. Wizualna informacja o stanie - kolor tła zależy od trybu.
- Przycisk resetujący ustawienia.
- Symulacja zmiany temperatury w pomieszczeniu.
- Sterowanie za pomocą klawiatury.

## 7. Smart Home (*)

Aplikacja symulująca panel sterowania systemem Smart Home, umożliwiająca sterowanie różnymi urządzeniami oraz monitorowanie ich stanu.

Funkcjonalności:

- Wyświetlanie listy urządzeń - *ikona*, *nazwa* i *status*.
- Możliwość sterowania poszczególnymi urządzeniami. Predefiniowana lista dostępnych urządzeń, z których każde posiada indywidualne opcje.
- Wybór jednego z trybów - *normalny*, *nocny*, *poza domem*. Każdy z trybów cechują inne opcje poszczególnych urządzeń.
- Historia zdarzeń - lista zmian opcji urządzeń.

## 8. System rezerwacji wizyt

Aplikacja umożliwia użytkownikom przeglądanie dostępnych terminów oraz rezerwację wizyt w wybranym przedziale czasowym.

Funkcjonalności:

- Wyświetlanie kalendarza lub listy dostępnych dni. Dostępnie terminy między 08:00, a 16:00, co 30 minut.
- Rezerwacja danego terminu, w ramach pewnej usługi (na przykład strzyżenie, masaż, konsultacja...). Każda usługa może trwać wielokrotność 30 minut (30, 60, 90, 120...). Usługa ma określoną cenę oraz przypisaną ikonkę.
- Możliwość anulowania rezerwacji.
- Możliwość edytowania rezerwacji.

## 9. System kolejkowy

Aplikacja symulująca system kolejkowy stosowany w urzędach. Użytkownik pobiera numer, a stanowisko obsługi wywołuje kolejne osoby.

Funkcjonalności:

- Pobieranie numeru za pomocą przycisku.
- Wyświetlanie oczekujących numerków, wyświetlanie aktualnie obsługiwanego numeru.
- System obsługi klienta.
- Podział na tryb ręczny i automatyczny - obsługa kolejnego klienta przy pomocy przycisku lub po danym czasie.
- Reset systemu.

## 10. System zgłoszeń w helpdesku

Aplikacja symulująca system obsługi zgłoszeń technicznych, w którym użytkownicy zgłaszają problemy, a pracownik wsparcia technicznego obsługuje je w kolejności zgłoszeń.

Funkcjonalności:

- Dodawanie złoszeń poprzez podanie tytułu, predefiniowanej kategorii i krótkiego opisu problemu.
- Wyświetalenie listy zgłoszeń oraz ich statusu (*nowe*, *w trakcie*, *rozwiązane*).
- Obsługa zgłoszeń.
- Filtrowanie zgłoszeń po kategorii i statusie. Sortowanie zgłoszeń alfabetycznie po tytule oraz po czasie dodania.
- Licznik zgłoszeń z podziałem na status.

## 11. Symulator playlisty

Aplikacja symulująca działanie playlisty muzycznej.

Funkcjonalności:

- Dodawanie utworów, podając *tytuł* i *wykonawcę*. Po dodaniu utwór trafia na koniec kolejki.
- Wyświetlanie aktualnie odtwarzanego utworu.
- Kolejka utworów.
- Możliwość przejścia do następnego utworu.
- Usuwanie utworów z kolejki.
- Reset playlisty.
- Możliwość wymieszania playlisty.

## 12. Zarządzanie zadaniami - *Kanban* (*)

Aplikacja umożliwia zarządzanie zadaniami w formie tablicy *Kanban*. Użytkownik może dodawać nowe zadania oraz przypisywać je do odpowiednich kolumn reprezentujących ich status. Dzięki temu możliwe jest śledzenie postępu pracy nad zadaniami w przejrzysty sposób.

### Struktura

Aplikacja składa się z belki górnej, formularza dodawania nowego zadania i tablicy *Kanban* podzielonej na kolumny. Każda z kolumn zawiera nagłówek oraz listę zadań. Oddzielne komponenty dla formularza, tablicy *Kanban* i poszczególnych kolumn.

### Funkcjonalność

- Możliwość dodania zadań składających się z tytułu oraz opisu i przydzielenia ich do jednej z trzech kolumn - *do zrobienia*, *w trakcie*, *zrobione*.
- Możliwość zmiany statusu zadania, usuwania go i modyfikowania treści. Wybór statusu powinien odbywać się poprzez listę wyboru i przyciski *Dalej*/*Wstecz*.
- Liczniki zadań w danej kolumnie, możliwość filtrowania i sortowania zadań.
- Ukryty panel do zarządzania tablicą *Kanban* - możliwość dodawania, usuwania i modyfikowania kolumn (ich koloru tła, tytułu i kolejności wyświetlania)
- *Drag & drop* - możliwość przeciągania zadań do poszczególnych kolumn.

### Dokumentacja

W kodzie źródłowym aplikacji konsolowej za pomocą komentarza utwórz nagłówek głównych funkcji, według wzoru.

```
************************************************************ 
nazwa funkcji:          <nazwa>
opis funkcji:           <krótki opis, co robi metoda>
parametry:              <nazwa i opis pierwszego parametru>
                        <nazwa i opis drugiego parametru>
                        ...
zwracany typ i opis:    <nazwa typu i opis co jest zwracane>
autor:                  <imię, nazwisko i klasa>
************************************************************
```

Komentarz powinien znaleźć się nad lub pod nazwą funkcji. W miejscu nawiasów ostrych (*<>*) należy podać odpowiednie opisy. W sekcji parametry należy umieścić opis wszystkich argumentów metody lub zapisać *brak* w przypadku funkcji bezparametrowej.

## 13. System osiągnięć

Aplikacja umożliwia śledzenie postępów użytkownika poprzez system osiągnięć. Użytkownik może wykonywać różne akcje, które odblokowują kolejne osiągnięcia. System pokazuje aktualny postęp oraz informuje o zdobytych nagrodach.

### Funkcjonalność

- Możliwość dodawania zadań składających się z tytułu oraz opisu. Zadania trafiają na listę i mogą być oznaczane jako wykonane lub niewykonane.
- Możliwość zmiany statusu zadania (niewykonane / wykonane), usuwania go oraz edytowania jego treści.
- System osiągnięć powiązany z aktywnością użytkownika - osiągnięcia odblokowywane są na podstawie:
    - liczby dodanych zadań,
    - liczby wykonanych zadań.
- Wyświetlanie listy osiągnięć wraz z ich statusem (zablokowane / odblokowane) oraz wizualnym wyróżnieniem zdobytych osiągnięć.
- Licznik postępu informujący o liczbie zdobytych osiągnięć oraz możliwością wyświetlenia aktualnych statystyk użytkownika (na przykład liczba wszystkich zadań, liczba wykonanych zadań).
- Możliwość resetowania danych aplikacji, co powoduje usunięcie wszystkich zadań oraz zresetowanie osiągnięć.

### Dokumentacja

W kodzie źródłowym aplikacji konsolowej za pomocą komentarza utwórz nagłówek głównych funkcji, według wzoru.

```
************************************************************ 
nazwa funkcji:          <nazwa>
opis funkcji:           <krótki opis, co robi metoda>
parametry:              <nazwa i opis pierwszego parametru>
                        <nazwa i opis drugiego parametru>
                        ...
zwracany typ i opis:    <nazwa typu i opis co jest zwracane>
autor:                  <imię, nazwisko i klasa>
************************************************************
```

Komentarz powinien znaleźć się nad lub pod nazwą funkcji. W miejscu nawiasów ostrych (*<>*) należy podać odpowiednie opisy. W sekcji parametry należy umieścić opis wszystkich argumentów metody lub zapisać *brak* w przypadku funkcji bezparametrowej.
