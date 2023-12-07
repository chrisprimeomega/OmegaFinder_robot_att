# ΩFinder

## What is(will be) ΩFinder?
This will be a tool to support me in finding cryptocurrencies worth investing in. Currently it will be adapted to the David part of my David vs Goliath project but I might make it more universal in the future.<br>
For now it looking for cryptocurrencies with market cap between 1 and 5 mln USD, of which there are about a thousand. Going through them on your own would take a lot of time and if you've read what I wrote on my main readme, you know that time is the most important resource for me. <br>
The robot's task is to shorten the time I spend looking for suitable projects by rejecting as many of them as possible based on my subjective criteria. I haven't come up with any objective criteria and I doubt they exist for such projects.<br>
The robot must perform the task as simply and quickly as possible. As my skills improve, I will likely upgrade the robot as well.

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

### Resume _saved_ work

## Time consumption of stages:
3 > 4 > 5 > 1 > 2

## Work progress
- [x] Let it work.
- [x] Make it look more pro. Extracting stages into separate sequences to make further improvements easier to implement.
- [x] Saves after stages 3 and 4 - these are the most time-consuming steps, especially during the first use, so adding the ability to _save_ work after them and return to them, the next time ΩFinder is turned on, seems justified
- [ ] saves during steps 4 and 5 - so you can return to your work the next time the robot is turned on
- [ ] reducing the number of activities to a minimum

