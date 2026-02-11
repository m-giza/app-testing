#  Moje portfolio testowe

To moje miejsce na dokumentowanie tego, czego się uczę i jak pracuję jako tester oprogramowania. Wszystkie przypadki testowe zostały ręcznie wykonane na demo aplikacji [Buggy Cars Rating](https://buggy.justtestit.org/) - darmowej platformie szkoleniowej dla QA.

---

## Co tutaj znajdziesz?

###  Test Cases (Manualne)

| ID | Nazwa | Typ | Status |
|----|-------|-----|--------|
| TC-Reg-001 | Walidacja słabego hasła | Functional (Negative) | ✅ Gotowy |
| TC-Reg-002 | Walidacja niezgodności haseł | Functional (Negative) | ✅ Gotowy |
| TC-Reg-003 | Udana rejestracja | Functional (Positive) | ✅ Gotowy |
| TC-Login-001 | Logowanie po rejestracji | Functional (Positive) | ✅ Gotowy |
| TC-Logout-001 | Wylogowanie | Functional (Positive) | ✅ Gotowy |
| TC-Vote-001 | Głosowanie na model samochodu | Smoke | ✅ Gotowy |

###  Checklisty

| ID | Zakres | Status |
|----|--------|--------|
| CL-Reg-001 | Rejestracja użytkownika | ✅ Gotowy |
| CL-Vote-001 | Głosowanie na samochód | ✅ Gotowy |

### API Testing

| Artefakt | Opis | Status |
|----------|------|--------|
| [`API-CRUD-Orders.postman_collection.json`](assets/API-CRUD-Orders.postman_collection.json) | Pełny flow CRUD na ResReq API:<br>• POST → extract ID → GET → DELETE<br>• Asertywy w testach<br>• Dynamiczne zmienne środowiskowe | ✅ Gotowy |

---

## Jak pracuję?

### Testowanie manualne - moje podejście

W codziennej pracy stawiam na **czytelność i precyzję dokumentacji**. W tym portfolio:
- Każdy test case ma **jeden cel** - nie mieszam rejestracji, logowania i głosowania w jednym scenariuszu.
- **Nie ufam ślepo komunikatom UI** - zawsze waliduję stan systemu (np. refresh po rejestracji, aby potwierdzić, że konto faktycznie powstało).
- Zwracam uwagę na **UX issues**, nawet jeśli nie są to błędy funkcjonalne (np. brak redirectu po rejestracji).

### API testing - pierwsze publiczne kroki

Kolekcja Postman (`API-CRUD-Orders`) to moja pierwsza udostępniona praca w tym zakresie. Demonstruje:
- Flow C-R-D (Create, Read, Delete) na ReqRes API,
- Dynamiczne chainowanie zmiennych (`recordId`),
- Proste asercje w sekcji "Tests".

To nie jest produkcja - to **dowód zrozumienia podstaw**, które rozwijam dalej.

### Dlaczego te artefakty są „proste”?

Nie pokazuję tu złożonych przypadków z mojej pracy zawodowej (np. eDiscovery, AI modules), ponieważ:
- Chciałem stworzyć **przejrzysty punkt wejścia** dla rekrutera,
- Portfolio skupia się na **podstawach testowania manualnego**, które są uniwersalne,
- Złożone przypadki często zawierają poufne dane - te są **100% publiczne i bezpieczne**.

---

## Ważne uwagi

- Wszystkie dane (`JHwell@32`, `Jnth@n!23`) to fikcyjne konta
- Checklisty zawierają tylko to, co faktycznie przetestowałem
- Aplikacja Buggy Cars to oficjalna platforma szkoleniowa

---

## Użycie sztucznej inteligencji

AI zostało wykorzystane wyłącznie do:
- Poprawy formatowania plików `.md` (GitHub syntax, tabele, nagłówki)
- Wygładzenia języka w opisach (bez zmiany treści)

Wszystkie testy, dane, logika i walidacje zostały wykonane **100% przeze mnie**.
---
## Kontakt

- **GitHub:** [@m-giza](https://github.com/m-giza)

> Portfolio rozwija się wraz ze mną - planuję dodawać raporty błędów i rozwijać kolekcję Postman.
