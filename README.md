
# MongoDB Kolokwium - Grupa B

Biblioteka posiada książki, które mają następujące właściwości:
- Tytuł książki
- Autor (zagnieżdżony dokument zawierający imię, nazwisko i narodowość autora)
- Rok wydania
- Gatunek
- Dostępność (czy książka jest dostępna do wypożyczenia)
- Recenzje (tablica zagnieżdżonych dokumentów zawierających użytkownika, ocenę i komentarz)

Napisz przykładowy dokument reprezentujący książkę w tej bazie danych.

## Zadanie 1: Komendy CRUD i Wyszukiwanie

Wykonaj następujące operacje CRUD i wyszukiwanie na bazie danych MongoDB dla kolekcji "ksiazki":

a) Wstaw nowy dokument do kolekcji "ksiazki":
```json
{
    "tytul": "Władca Pierścieni",
    "autor": {
        "imie": "J.R.R.",
        "nazwisko": "Tolkien",
        "narodowosc": "Brytyjczyk"
    },
    "rok_wydania": 1954,
    "gatunek": "Fantasy",
    "dostepnosc": true,
    "recenzje": [
        {
            "uzytkownik": "Piotr Zielinski",
            "ocena": 5,
            "komentarz": "Niesamowita książka!"
        },
        {
            "uzytkownik": "Maria Kwiatkowska",
            "ocena": 4,
            "komentarz": "Bardzo dobra, ale trochę długa."
        }
    ]
}
```

b) Zaktualizuj dokument, zmieniając dostępność książki "Władca Pierścieni" na false.\

c) Usuń dokumenty, w których rok wydania jest starszy niż 1980.

## Zadanie 2: Wyszukiwanie

a) Znajdź wszystkie książki autora "J.R.R. Tolkien".

b) Znajdź wszystkie książki, które są dostępne do wypożyczenia.

c) Znajdź wszystkie książki, które mają ocenę recenzji równą 5.

## Zadanie 3: Agregacje

Skorzystaj z frameworku agregacji, aby wykonać następujące zadania na kolekcji "ksiazki":

a) Oblicz liczbę książek dostępnych w każdym gatunku.

b) Znajdź najstarszą książkę w kolekcji.

c) Oblicz średnią ocenę dla każdej książki.

d) Zlicz liczbę książek napisanych przez autorów o narodowości "Brytyjczyk".

e) Znajdź książki, które mają więcej niż jedną recenzję.

## Instrukcje Dodatkowe

- Do wykonania operacji CRUD użyj komend MongoDB: `insertOne()`, `updateOne()`, `deleteMany()`, `find()`.
- Do operacji agregacyjnych użyj komendy `aggregate()`.
