
<a name = "wprowadzenie"></a>
# Wprowadzenie

## Tworzenie projektu

Należy stworzyć katalog, w którym ma znajdować się projekt i zainstalować w nim *Express.js*:

```console
npm init -y
npm install express
```

Następnie utworzyć główny plik `index.js`:

```js
import express from 'express';

const app = express();

app.listen(3000, () => {
    console.log('Serwer działa na porcie 3000');
});
```

Dodatkowo, w pliku `package.json`, należy dodać linijkę:

```json
"type": "module",
```

Aby uruchomić serwer należy wpisać

```console
node index.js
```

i przejść pod odpowiedni adres.

## Endpointy

Aby odpowiedzieć na żądanie `GET` pod adresem `/`, dodaj:

```js
app.get('/', (req, res) => {
    res.send('Przykładowy tekst');
});
```

Przy pomocy `res.send` możemy przesyłać między innymi tekst i kod HTML. Jeżeli chcemy przesłać dane w formacie json, korzystamy z `res.json`.

```js
res.json({
    x: 6,
    y: 7
});
```

## Parametry ścieżki

Służą do przekazywania danych bezpośrednio w adresie *URL*.

```js
app.get('/api/:x', (req, res) => {

    const x = req.params.x;
    res.send(`Parametr: ${x}`);

});
```

Jeśli odwiedzimy adres `/api/3`, otrzymamy tekst **Parametr: 3**. Dostęp do parametrów uzyskujemy przez `req.params`.

## Parametry zapytania

```js
app.get('/api', (req, res) => {

    const { x, y } = req.query;

    res.send(`Parametry: ${x} i ${y}`);
});
```

Występują po znaku `?` w *URL*, na przykład `/api?x=6&y=7`. Odczytujemy je przez `req.query`.

## Obsługa formularza

W celu obsługi formularzy należy skonfigurować *middleware*.

```js
app.use(express.urlencoded({ extended: true }));
app.use(express.json());
```

I *middleware* odpowiedzialny za pliki statyczne.

```js
app.use(express.static('public'));
```

A następnie w folderze `/public` przygotować sam formularz.

```html
<form action = "/form" method = "POST">
    <input type = "number" name = "a">
    <button type = "submit">Wyślij</button>
</form>
```

Oraz *endpoint* odpowiedzialny za odebranie z niego danych.

```js
app.post('/form', (req, res) => {

    const { x } = req.body;

    res.send(`x = ${x}`);
});
```

## Ręczne serwowanie stron

W przypadku gdy nie chcemy udostępniać całego folderu, chcemy wskazać konkretny plik lub kontrolować ścieżkę skorzystamy z `sendFile`.

```js
app.get('/', (req, res) =>

    res.sendFile('public/index.html', { root: '.' });
);
```

<a name = "zadania"></a>
# Zadania

1.1. Stwórz aplikację Express, która uruchamia serwer na porcie *3000* i wyświetla w przeglądarce tekst *Witaj świecie!*

1.2. Dodaj do serwera trzy endpointy:
    - `/about` - wyświetla tekst **Informacje o stronie**,
    - `/contact` - wyświetla tekst **Email: xpp<span></span>@xdd.pl**,
    - `/time` - wyświetla aktualny czas.

1.3. Stwórz endpoint `/hello/:name` przyjmujący parametr *imie* i wyświetlający tekst **Witaj \<imie\>**.

1.4. Stwórz endpoint `/sum`, przyjmujący w URL parametry `a` i `b` i wyświetlający sumę podanych liczb.

    Przykład użycia: `/sum?a=6&b=7`.

1.5. Rozszerz poprzednie zadanie, dodając endpointy dla różnicy, iloczynu, ilorazu, kwadratu oraz pierwiastka kwadratowego.

1.6. Stwórz endpoint `/api/info`, który zwróci obiekt *JSON* o treści:

```json
{
    "nazwa": "Moja aplikacja",
    "wersja": "1.0",
    "autor": "Ja"
}
```

1.7. Stwórz endpoint `/students`, który zwraca tablicę:

```json
[
    "Adam",
    "Kasia",
    "Ola"
]
```

1.8. Stwórz *endpoint* `/random` generujący losową liczbę z zakresu *1–100*. Odpowiedź zwróć w formacie *json*.

1.9. Zmodyfikuj poprzednie zadanie, aby zakres był możliwy do określenia poprzez parametry *URL*.

1.10. Zmodyfikuj poprzednie zadanie, aby istniała możliwość określenia ilości liczb do wygenerowania. Wynik zwróć w postaci tablicy liczb.

---

2.1. Stwórz stronę HTML z formularzem złożonym z pól:

    - imię,

    - email,

    - wiadomość.

Wyślij dane metodą POST na `/kontakt`. Serwer ma wyświetlić podsumowanie:

```
Wiadomość od <imię> (<email>):
<treść>
```

2.2. Kalkulator prosty. Formularz HTML z dwoma polami odpowiadającymi liczbom. Po wysłaniu na `/calc` serwer zwraca wynik dodawania tych liczb.

2.3. Dodawanie elementu do tablicy. Utwórz tablicę `produkty`. Stwórz formularz *POST* `/dodaj` z polem **nazwa**

Po wysłaniu dodaj produkt do tablicy,

Przygotuj endpoint `/wyswietl`, który wyświetli zaktualizowaną listę produktów w formacie **json**.

---

3.1. Stwórz aplikację, która po wejściu na adres `/` odpowiada plikiem `index.html` z katalogu **public**.

3.2 Utwórz `form.html` z polem `age` oraz metodą **POST** dla `/submit`. W route `/submit` odbierz dane za pomocą `req.body`. Jeśli wartość pola `age >= 18`, zwróć plik `adult.html`. Jeśli `age < 18`, zwróć `child.html`.

3.3 Stwórz `login.html` z polami **login** i **password**. Jeśli użytkownik wpisze hasło **admin123**, wyślij plik `dashboard.html`
W przeciwnym razie wyślij plik `error.html`.

3.4 Stwórz formularz zawierający pola `a` i `b` oraz metodę POST dla `/calc`. wybór działania (select z opcjami: dodawanie, odejmowanie, mnożenie, dzielenie).

- Jeśli wynik jest dodatni zwróć `positive.html`.
- Jeśli wynik jest zero zwróć `zero.html`.
- Jeśli wynik jest ujemny zwróć `negative.html`.

<a name = "Projekty"></a>
# Projekty

Użytkownik może się rejestrować wpisując *imię*, *nazwisko*, *datę urodzenia*, *adres email* oraz *hasło* i *powtórzone hasło*. Imię*, i *nazwisko* powinny mieć przynajmniej trzy znaki, data powinna być wprowadzona, hasło ma mieć przynajmniej osiem znaków. Dane są walidowane po stronie serwera. Jeżeli walidacja przebiegła pomyślnie, dane są dodawane do tablicy. Podczas logowania, przy pomocy *emaila* i *hasła* sprawdzamy czy taki użytkownik jest obecny w tablicy. Odpowiedź zwracana jest jako plik HTML przez `sendFile()`.
