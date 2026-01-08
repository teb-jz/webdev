
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

<a name = "zadania"></a>
# Zadania

1. Stwórz aplikację Express, która uruchamia serwer na porcie *3000* i wyświetla w przeglądarce tekst *Witaj świecie!*

2. Dodaj do serwera trzy endpointy:
    - `/about` - wyświetla tekst **Informacje o stronie**,
    - `/contact` - wyświetla tekst **Email: xpp<span></span>@xdd.pl**,
    - `/time` - wyświetla aktualny czas.

3. Stwórz endpoint `/hello/:name` przyjmujący parametr *imie* i wyświetlający tekst **Witaj \<imie\>**.

4. Stwórz endpoint `/sum`, przyjmujący w URL parametry `a` i `b` i wyświetlający sumę podanych liczb.

    Przykład użycia: `/sum?a=6&b=7`.

5. Rozszerz poprzednie zadanie, dodając endpointy dla różnicy, iloczynu, ilorazu, kwadratu oraz pierwiastka kwadratowego.

6. Stwórz endpoint `/api/info`, który zwróci obiekt *JSON* o treści:

```json
{
    "nazwa": "Moja aplikacja",
    "wersja": "1.0",
    "autor": "Ja"
}
```

7. Stwórz endpoint `/students`, który zwraca tablicę:

```json
[
    "Adam",
    "Kasia",
    "Ola"
]
```

8. Stwórz *endpoint* `/random` generujący losową liczbę z zakresu *1–100*. Odpowiedź zwróć w formacie *json*.

9. Zmodyfikuj poprzednie zadanie, aby zakres był możliwy do określenia poprzez parametry *URL*.

10. Zmodyfikuj poprzednie zadanie, aby istniała możliwość określenia ilości liczb do wygenerowania. Wynik zwróć w postaci tablicy liczb.
