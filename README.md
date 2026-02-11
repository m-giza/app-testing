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

### Testowanie manualne - moja główna siła

- **Narzędzia:** Qase.io do organizacji, GitHub do prezentacji
- **Mój styl:**
  - Każdy test case ma jeden cel — nie mieszam funkcjonalności
  - Nie ufam ślepo komunikatom UI — zawsze sprawdzam stan systemu (np. refresh po rejestracji)
  - Zwracam uwagę na UX issues (np. brak redirectu po rejestracji)

### API testing - rozwijam kompetencje

Moja kolekcja Postman demonstruje:
-  Pełny flow CRUD z dynamicznym chainowaniem (`recordId`)
-  Testy asercji w sekcji "Tests"
-  Obsługę różnych kodów statusu (201, 200, 204)

Nie udaję eksperta - posiadam doświadczenie z praktyki na prywatnych kolekcjach (m.in. Trello, ReqRes) 

---

## Ważne uwagi

- Wszystkie dane (`JHwell@32`, `Jnth@n!23`) to fikcyjne konta
- Checklisty zawierają tylko to, co faktycznie przetestowałem
- Aplikacja Buggy Cars to oficjalna platforma szkoleniowa
- Jestem otwarty na naukę automatyzacji testów.


---

## Kim jestem?

Jestem testerem na etapie **junior+/regular**:
-  Potrafię pisać atomowe test cases z precyzyjnymi expected results
-  Rozumiem potrzebę walidacji poza UI
-  Mam pierwsze doświadczenia z API testing (Postman CRUD flow itp.)

---

## Użycie sztucznej inteligencji

AI zostało wykorzystane wyłącznie do:
- Poprawy formatowania plików `.md` (GitHub syntax, tabele, nagłówki)
- Wygładzenia języka w opisach (bez zmiany treści)

Wszystkie testy, dane, logika i walidacje zostały wykonane **100% przeze mnie**.
---
## Kontakt

- **GitHub:** [@m-giza](https://github.com/m-giza)

> Portfolio rozwija się wraz ze mną — planuję dodawać raporty błędów i rozwijać kolekcję Postman. AI zostało wykorzystane do poprawy github syntaxu -> aby pliki były bardziej przejrzyste i github-friendly. Wszelkie testy i kontent zostały wykonane w 100% przeze mnie.
