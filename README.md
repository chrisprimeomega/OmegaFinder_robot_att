# David ΩETF Robot

## Co to jest David ETF?
Jest to cześć projektu David vs Goliath. W skrócie polega ona na tym, że inwestuję w kryptowaluty o mcap z przedziału 1 do 5 mln (David) oraz tych z największym mcap (Goliath). Więcej o projekcie tutaj

## Do czego służy robot?
Kryptowalut o mcap 1 do 5 mln jest około 1 tys. Więc samodzielne ich przeglądanie zajęłoby mnóstwo czasu a jeżeli czytałeś co napisałem na mojej głównej stronie to wiesz, że czas dla mnie jest najważniejszym zasobem. Zadaniem robota jest skrócenie czasu jaki poświęcę na szukanie odpowiednich projektów, poprzez odrzucenie jak największej ich liczby na podstawie moich subiektywnych kryteriów. Na obiektywne kryteria nie wpadłem i wątpię, że takowe istnieją w przypadku takich projektów.
Robot ma wykonać zadanie jak najprościej i być dostosowany do moich obecnych umiejętności.

## Praca jaką wykonuje robot
### Pierwsze użycie
1. Pobranie danych z rankingu Coingecko - na każdej stronie rankingu jest 100 krypto, początek pobierania danych ustalam statycznie na konkretną stronę
2. Odrzucenie krypto z mcap większym niż 5mln i mniejszym niż 1mln - z uwagi że pobieranie następuje z naddatkiem, czyli mogą się w nim znaleźć krytpo z poza przedziału, to trzeba je odrzucić
3. Odrzucenie krypto powstałych przed 2021 - moim zdaniem jeśli projekt powstał ponad 3 lata temu i dalej ma tak mały mcap to jest mała szansa, że można na nim zarobić. Oczywiście zdaję sobię sprawę, że mogę przez to pominąć jakąś perełkę ale liczę się z tym.
4. Manualne odrzucenie tylko na podstawie wykresu - sam odrzucam projekt oceniając tylko i wyłącznie jego całościowy wykres, rola robota to otwarcie strony projektu na Coingecko i wycentrowanie obrazu na maksymalny wykres oraz otworzenie popupu z opcjami YES NO
5. Manualne odrzucenie na podstawie oceny projektu - tu już zagłębiam się bardziej w projekt, wchodzę na jego stronę, githuba, X itp. Robot ma za zadanie tylko ponownie otworzyć stronę na Coingecko i otworzyć YES/NO popup

Output
Plik Excel z dwoma zakładkami/sheetami
1. 1to5mln - zawierający wszystkie krypto jakie zostały po 2 etapie
2. Final - zawierający tylko krypto które dotrwały do końca

Czemu Excel? Ponieważ dane z zakładki Final będą użyte w dalszej części projektu David vs Goliath, w tym między innymi do utworzenia dashboardu w Tableau. A przy takiej ilości danych takiego formatu mi będzie najłatwiej używać.

6. Etap już niedotyczący robota a mianowicie następnego dnia, jeszcze raz przeglądam wybrane projekty i ostatecznie podejmuję decyzję które zostawić

### Kolejne użycia
1. Etap 1 z pierwszego użycia
2. Pobranie danych z pliku Excel z zakładki 1to5mlm
3. Odrzucenie krypto które znajdują się już w zakładce 1to5mln
4. Etapy 2-5(6) z pierwszego użycia

Output
taki sam jak w pierwszym użyciu w tym, że nowe krypto są dopisywane w istniejących już zakłądkach pliku Excel.

## Czasochłonność etapów:
3 > 4 > 5 > 2 > 1

## Postęp prac
- [x] Niech to działa
- [ ] dodanie przerwy po kroku 3 i 4 - są to najbardziej czasochłonne kroki, szczególnie przy pierwszym użyciu, więc dodanie możliwości przerwania pracy po nich i wrócenie do nich po kolejnym włączeniu robota wydaje się uzasadnione
- [ ] zmniejszenie liczby aktywności do minimum

