# geek_off_angular

Replacement for round 1 & 2 of the Geek Off at my employer. A work in progress.

# Initial setup

* Run npm i in the /clientapp folder to get the Angular/Node packages
* Set up the following user secrets in the root folder:

| User secret | Description |
|--|--|
| ConnectionStrings:GeekOff | Postgres database connection |
| Azure:SignalR:ConnectionString | Microsoft Azure SignalR Real time service connection string |

## Required Fonts

Fonts used in the scoreboard are not included for copyright reasons. These fonts can be found as follows:

| Font name | URL | Use |
|--|--|--|
| eggcrate.ttf | http://tpirepguide.com/qwizx/tpirfonts/eggcrate.zip | Round 1 board |
| sportstype.ttf | http://tpirepguide.com/qwizx/tpirfonts/sportstype.zip | Round 3 scores |
| fastmoney3.ttf | https://fontstruct.com/fontstructions/show/1181116/fast_money_three | Round 2 board


# Running the API

Run the app in debug mode in Visual Studio. This will run both the Angular and .NET core apps together.

Swagger can be found at the endpoint `/swagger`. This only runs in the dev hosting environment.

# Automated tests

Automated testing is not enforced or required.

# Work to be completed

## Round 2

1. Store (ngrx) - library installed but that's it
2. Countdown timer screen/component
  * Supports countdown from 20 or 25 seconds
  * Import something and style?
  * Kicks off from control screen
3. Results component - Kristin (people see this - big screen)
  * Shows columns of answers and scores
  * API: /api/round2/bigBoard/{yEvent}/{teamNo}
  * Text should be animated
4. Control screen (behind the scenes) - Grant
  * Show list of questions and answers from database. API: /api/round2/allSurvey/{yEvent}
  * Enter answer that team gives for question and points. API: /api/round2/teamAnswer/text, /api/round2/teamAnswer/survey from button
  * Finalize the round. /api/round2/finalize/{yevent}
5. Host screen (host cellphone) - Dan
  * Show questions on the phone. API: /api/round2/allQuestions/{yEvent}
6. Scoreboard (lower priority)
  * API: /api/round2/scoreboard/{yEvent}

  ## Round 1

Work will be identified after round 2 is completed.
