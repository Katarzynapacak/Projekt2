# Projekt2 Katarzyna Pacak 204119
Wizualizacja procesu przepływu cieczy

Opis projektu
Projekt przedstawia uproszczony system typu SCADA/HMI, służący do wizualizacji
i symulacji procesu przemysłowego z udziałem czterech zbiorników, rurociągów,
pompy oraz grzałki.  
Aplikacja została napisana w języku Python z wykorzystaniem biblioteki PyQt5
oraz matplotlib.

Proces przebiega automatycznie, a użytkownik ma możliwość zadania jedynie
parametrów początkowych instalacji przed uruchomieniem symulacji.

 Działania
- wizualizacja poziomów cieczy w czterech zbiornikach (Z1–Z4),
- wizualizacja przepływu cieczy w rurociągach z zakrętami 90° i rozgałęzieniem,
- wizualizacja pracy pompy oraz grzałki,
- symulacja temperatury w zbiorniku Z3,
- automatyczna logika procesu- bilans przepływów i temperatury,
- obsługa alarmów procesowych: przepełnienie, wysoka temperatura, awaria pompy,
- prezentacja trendów czasowych- wykresów zmiany poziomów i temperatury,
- interfejs użytkownika w postaci zakładek:
  - Instalacja
  - Alarmy
  - Trendy

Struktura projektu
Projekt został podzielony na pliki:
- main.py - Punkt startowy aplikacji
- okno_glowne.py - Interfejs użytkownika (GUI)
- model.py -Logika procesu i obiekty instalacji

  Zasada działania
1. Po uruchomieniu programu wyświetlany jest dialog startowy,
   w którym użytkownik ustawia parametry początkowe (poziomy, temperatura,
   prędkość pompy, moc grzałki).
2. Po zatwierdzeniu parametrów uruchamiane jest okno główne SCADA.
3. Proces jest symulowany automatycznie w krokach czasowych
   wywoływanych przez `QTimer`.
4. Aktualny stan instalacji jest wizualizowany w czasie rzeczywistym.
5. W przypadku przekroczenia zadanych progów aktywowane są alarmy,
   widoczne w osobnej zakładce.
6. Zmiany poziomów i temperatury są zapisywane i prezentowane
   w postaci trendów czasowych.

Zastosowane technologie
- Python 3
- PyQt5 – interfejs graficzny (GUI)
- matplotlib – wykresy trendów
- programowanie obiektowe (OOP)

  

