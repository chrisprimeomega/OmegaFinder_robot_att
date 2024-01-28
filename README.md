# ΩFinder

## What is(will be) ΩFinder?
This will be a tool to support me in finding cryptocurrencies worth investing in. Currently it will be adapted to the David part of my David vs Goliath project but I might make it more universal in the future.<br>
For now it looking for cryptocurrencies with market cap between 1 and 5 mln USD, of which there are about a thousand. Going through them on your own would take a lot of time and if you've read what I wrote on my main readme, you know that time is the most important resource for me. <br>
The robot's task is to shorten the time I spend looking for suitable projects by rejecting as many of them as possible based on my subjective criteria. I haven't come up with any objective criteria and I doubt they exist for such projects.<br>
The robot must perform the task as simply and quickly as possible. As my skills improve, I will likely upgrade the robot as well.

## What should the robot do?
### First Full Use
#### Includes five main stages
1. 🤖 Extracting data from the Coingecko ranking - there are 100 cryptocurrencies on each ranking page. I statically set the start of data extracting for a specific page.
2. 🤖 Throwing out cryptos with mcap greater than 5 and less than 1mln - due to the fact that the extraction takes place with an excess, i.e. it may contain cryptos from outside the range that need to be thrown away
3. ~~🤖 Throwing away cryptocurrencies created before 2021 - in my opinion, if the project was created over 3 years ago and still has such a small mcap, there is little chance that you can make money on it. Of course, I realize that I may miss some gems because of this, but I take it into account.~~<br>
*The project pages on Coingecko have changed, so stage 3 has been removed from Workflow. At the moment, I have no plans to develop this robot, so the latest update makes the robot work, but if it were to be made professionally, it would have to be more adapted to the current Coingecko website. I don't plan on doing that though.*
4. 👨‍💻 🤖 Manual rejection only based on the chart - I throw the project myself, assessing only its overall chart, the robot's role is to open the project page on Coingecko and center the image on the maximum chart and open a popup with the YES NO options.
5. 👨‍💻 🤖 Manual rejection based on project assessment - here I delve deeper into the project, go to its website, github, X, etc. The robot's task is only to reopen the page on Coingecko and open the YES/NO popup.

**Output**<br>
Excel file with two sheets
1. _1to5mln_ - containing all crypto that was left after stage 2
2. _Final_ - containing cryptocurrencies that survived until the end

_Why Excel?_ because the data from the Final tab will be used later in the David vs Goliath project, including creating a dashboard in Tableau. And with such a relatively small amount of data, this format will be easiest for me to use.

6. 👨‍💻 Stage that no longer concerns the robot. The next day, I look through the selected projects again and finally decide which ones to keep

### Next Full Use
1. Stage 1
2. Extracting data from an Excel file from the 1to5mln sheet
3. Throwing out cryptos that are already in the 1to5mln sheet
4. Stages 2-5(6)

**Output**
The same as in the First Full Use, in that new cryptos are appended to the existing sheets of the Excel file.

### Resume _saved_ work
The robot also has a function of saving work after the 3rd and 4th stage. If the user decides to save the work, when the robot is restarted, he will be able to return to the point where he finished.

## Time consumption of stages:
~~3~~ > 4 > 5 > 1 > 2

## Work progress
- [x] Let it work.
- [x] Make it look more pro. Extracting stages into separate sequences to make further improvements easier to implement.
- [x] Saves after stages 3 and 4 - these are the most time-consuming steps, especially during the first use, so adding the ability to _save_ work after them and return to them, the next time ΩFinder is turned on, seems justified
- [x] v1 released
- [x] v1.1 released


