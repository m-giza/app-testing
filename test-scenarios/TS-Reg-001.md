# TS-Reg-001: User Registration End-to-End Flow

## Cel
Zweryfikować kompletny proces rejestracji nowego użytkownika, w tym walidację danych, obsługę błędów i potwierdzenie utworzenia konta.

## Zakres obejmowany
- Walidacja hasła (minimalna długość, znak specjalny, wielka litera)
- Walidacja zgodności pól hasła
- Obsługa błędów UI (komunikaty)
- Potwierdzenie utworzenia konta (nie tylko komunikat, ale stan systemu)
- Zachowanie formularza po błędzie/sukcesie

## Powiązane przypadki testowe
- TC-Reg-001: Password validation fails with weak password
- TC-Reg-002: Password mismatch validation  
- TC-Reg-003: Successful registration with valid credentials

## Warunki wstępne
- Użytkownik nie jest zarejestrowany w systemie
- Dostęp do aplikacji Buggy Cars Rating

## Kryteria akceptacji
- Wszystkie powiązane TC przechodzą  
- Użytkownik może zalogować się po rejestracji  
- System blokuje próbę ponownej rejestracji tym samym loginem

## Uwagi
- Scenariusz nie obejmuje logowania - to osobny flow (TS-Login-001)
- UX issue: formularz pozostaje widoczny po sukcesie - nie blokujący, ale wart uwagi
