# Notatki — prywatny dziennik (wersja startowa)

To jest pierwsza, rozszerzalna wersja aplikacji w formie PWA. Można ją dodać do ekranu głównego Androida z przeglądarki, jeśli pliki zostaną opublikowane pod adresem HTTPS. To **nie jest jeszcze plik APK**.

## Funkcje
- PIN 6–12 cyfr; lokalne szyfrowanie danych AES-GCM, klucz wyprowadzany przez PBKDF2.
- Dziennik konkretnego dnia: przemyślenia, osiągnięcia, wnioski, nastrój i rodzaj dnia.
- Aktywności z wynikiem liczbowym i listą możliwą do rozbudowy.
- Cele z terminem i następnym krokiem.
- Kalendarz i wydarzenia.
- Wyszukiwanie historii oraz filtrowanie po aktywności.
- Podsumowania tygodniowe i miesięczne.
- Prosty rejestr finansów i wyników transakcji.
- Zaszyfrowany eksport i import kopii.
- Tryb offline po pierwszym uruchomieniu i cache zasobów.

## Jak uruchomić
PWA musi być udostępniona przez HTTPS albo uruchomiona na localhost. Samo otwarcie pliku `index.html` z menedżera plików Androida nie wystarczy do działania wszystkich funkcji bezpieczeństwa/offline.

1. Opublikuj folder na hostingu obsługującym HTTPS (np. własny hosting statyczny).
2. Otwórz adres w Chrome na Androidzie.
3. W menu Chrome wybierz „Dodaj do ekranu głównego” lub „Zainstaluj aplikację”.
4. Ustaw PIN przy pierwszym uruchomieniu.
5. Zrób zaszyfrowaną kopię w Ustawieniach.

## Ważne
- Jeśli zapomnisz PIN-u, nie ma odzyskiwania danych bez prawidłowego PIN-u. Zachowuj zaszyfrowaną kopię.
- To wersja 0.1 — należy ją przetestować przed przechowywaniem bardzo ważnych danych. Przeglądarka/urządzenie mogą usuwać dane witryny, więc kopie zapasowe są istotne.
- Powiadomienia systemowe, biometria Androida i synchronizacja między urządzeniami nie są jeszcze zaimplementowane.
- Podsumowania są wyliczane z zapisanych wpisów, bez generowania fikcyjnych danych.
- Kod jest celowo prosty i rozdzielony na pliki, żeby dało się rozwijać funkcje dalej.
