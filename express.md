
<a name = "cwiczenia"></a>
# Ćwiczenia

### Ćwiczenie 1
Stwórz aplikację Express, która słucha na porcie *3000*, a na wejściu *GET* `/` wyświetla tekst `"Witaj!"`.

### Ćwiczenie 2
Stwórz proste api z następującymi endpointami:
- *GET* `/hello/:name` - wyświetla `"Witaj <name>!"`,
- *GET* `/calc/:a&:b` - wyświetla `"Suma <a> i <b> wynosi <a + b>."`,
- *GET* `/ping` - zwraca *json* `{"status": "ok"}`.

### Ćwiczenie 3
Zaimplementuj proste API do zarządzania to-do listą, przechowywaną w tablicy:
- *GET* `/tasks` - zwraca listę zadań,
- *POST* `/tasks` - dodaje nowe zadanie,
- *DELETE* `/tasks/:id` - usuwa zadanie,
- *PUT* `/taks/:id` - edycja zadania.
Każde z zadań posiada pola *id*, *content*, *isDone*.
