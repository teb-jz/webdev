# Pobieranie elementu

Do odniesienia się do pojedynczych elementów można wykorzystać metody obiektu `document`:
- `querySelector` &ndash; jako parametr podajemy selektor znany z `css`,
- `getElementById` &ndash; parametrem jest **id** elementu.

```js
const e1 = document.querySelector('#sampleId');
const e2 = document.getElementById('sampleId');
```

W przypadku zbioru elementów &ndash; kolekcji:
- `querySelectorAll` &ndash; jak wyżej, selektor `css`,
- `getElementsByClassName` &ndash; parametrem jest nazwa **klasy** elementów.

```js
const e1 = document.querySelectorAll('.sampleClass');
const e2 = document.getElementsByClassName('sampleClass');
```

# Obsługa zdarzeń

Chcąc obsłużyć dane **zdarzenie** należy odwołać się do interesującego nas elementu i dodać **nasłuch zdarzenia** za pomocą metody `addEventListener`, określając jego typ, na przykład `click`, oraz precyzując co ma się wykonać po jego wystąpieniu, podając funkcję, która ma się wtedy wykonać.

```js
function clicked () {

    console.log('clicked');
}

const button = document.querySelector('button');

button.addEventListener('click', clicked);
```

Przykładowe zdarzenia:
- `click` &ndash; naciśnięcie,
- `mouseover` &ndash; najechanie kursorem,
- `input` &ndash; wprowadzanie danych (tylko `input`).

# Zmiana elementów

## Klasy

Korzystając z pola `classList` jesteśmy w stanie edytować listę klas danego elementu:
- `add` &ndash; dodawanie,
- `remove` &ndash; usuwanie,
- `toggle` &ndash; przełączanie.

```js
const block = document.querySelector('div');

block.classList.add('sampleClass');
block.classList.remove('sampleClass');
block.classList.toggle('sampleClass');
```

## Zawartość

Do zawartości elementów możemy odnieść się przy pomocy `textContent`, `innerText` oraz `innerHTML`. Ostatnie pole, w przeciwieństwie do pozostałych, rozróżnia znaczniki **HTML**, pozwalając na prymitywne tworzenie struktury dokumentu.

```js
const span = document.querySelector('span');

span.textContent = "new text";
span.innerText = "new text";

span.innerHTML = "<p>new text</p>";
```

## Style

Pole `style` pozwala na nadawanie stylów wybranym elementom. Posiada wbudowane odwołania do atrybutów znanych z `css`.

```js
const paragraph = document.querySelector('p');

paragraph.style.color = 'purple';
paragraph.style.fontSize = '32px';

paragraph.style.cssText = "text-decoration: underline; font-style: italic;";
```

Do dyspozycji mamy również pole `cssText`, dzięki któremu jesteśmy w stanie sprecyzować wiele styli na raz.
