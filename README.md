# David ΩETF Robot

## Co to jest David ETF?
Jest to cześć projektu David vs Goliath. W skrócie polega ona na tym, że inwestuję w kryptowaluty o mcap z przedziału 1 do 5 mln (David) oraz tych z największym mcap (Goliath). Więcej o projekcie tutaj

## Do czego służy robot?
Kryptowalut o mcap 1 do 5 mln jest około 1 tys. Więc samodzielne ich przeglądanie zajęłoby mnóstwo czasu a jeżeli czytałeś co napisałem na mojej głównej stronie to wiesz, że czas dla mnie jest najważniejszym zasobem. Zadaniem robota jest skrócenie czasu jaki poświęcę na szukanie odpowiednich projektów, poprzez odrzucenie jak największej ich liczby na podstawie moich subiektywnych kryteriów. Na obiektywne kryteria nie wpadłem i wątpię, że takowe istnieją w przypadku takich projektów.
Robot ma wykonać zadanie jak najprościej i być dostosowany do moich obecnych umiejętności.

## What should the robot do?
### First use
#### Includes five main stages
1. 🤖 Pobranie danych z rankingu Coingecko - na każdej stronie rankingu jest 100 krypto, początek pobierania danych ustalam statycznie na konkretną stronę
2. 🤖 Odrzucenie krypto z mcap większym niż 5mln i mniejszym niż 1mln - z uwagi że pobieranie następuje z naddatkiem, czyli mogą się w nim znaleźć krytpo z poza przedziału, to trzeba je odrzucić
3. 🤖 Odrzucenie krypto powstałych przed 2021 - moim zdaniem jeśli projekt powstał ponad 3 lata temu i dalej ma tak mały mcap to jest mała szansa, że można na nim zarobić. Oczywiście zdaję sobię sprawę, że mogę przez to pominąć jakąś perełkę ale liczę się z tym.
4. 👨‍💻 🤖 Manualne odrzucenie tylko na podstawie wykresu - sam odrzucam projekt oceniając tylko i wyłącznie jego całościowy wykres, rola robota to otwarcie strony projektu na Coingecko i wycentrowanie obrazu na maksymalny wykres oraz otworzenie popupu z opcjami YES NO
5. 👨‍💻 🤖 Manualne odrzucenie na podstawie oceny projektu - tu już zagłębiam się bardziej w projekt, wchodzę na jego stronę, githuba, X itp. Robot ma za zadanie tylko ponownie otworzyć stronę na Coingecko i otworzyć YES/NO popup

**Output**<br>
Excel file with two sheets
1. _1to5mln_ - containing all crypto that was left after stage 2
2. _Final_ - containing cryptocurrencies that survived until the end

_Why Excel?_ because the data from the Final tab will be used later in the David vs Goliath project, including creating a dashboard in Tableau. And with such a relatively small amount of data, this format will be easiest for me to use.

6. 👨‍💻 Etap już niedotyczący robota a mianowicie następnego dnia, jeszcze raz przeglądam wybrane projekty i ostatecznie podejmuję decyzję które zostawić

### Kolejne użycia
1. Etap 1 z pierwszego użycia
2. Pobranie danych z pliku Excel z zakładki 1to5mlm
3. Odrzucenie krypto które znajdują się już w zakładce 1to5mln
4. Etapy 2-5(6) z pierwszego użycia

**Output**
taki sam jak w pierwszym użyciu w tym, że nowe krypto są dopisywane w istniejących już zakładkach pliku Excel.

## Time consumption of stages:
3 > 4 > 5 > 1 > 2

## Work progress
- [x] Let it work
- [ ] saves after stages 3 and 4 - these are the most time-consuming steps, especially during the first use, so adding the ability to _save_ work after them and return to them the next time the robot is turned on, seems justified
- [ ] saves during steps 4 and 5 - so you can return to your work the next time the robot is turned on
- [ ] reducing the number of activities to a minimum

