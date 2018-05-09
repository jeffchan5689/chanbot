# Intro
Chanbot is a general purpose [Slack](https://slack.com/) bot. 

This has been developed with Python 2.7 in mind. 

![screenshot](screenshot.png)

## Installation

1. Clone the repo
2. `pip install -r requirements.txt`
3. Host the web app on [Heroku](http://heroku.com):

    ```
    heroku create
    git push heroku master
    heroku ps:scale web=1
    heroku logs
    ```
4. Set up some config variables using `heroku config:set VARIBLE=value`:
   - `TOKEN`: your team's Slack API token. (required)
   - `USERNAME`: your bot's username. (optional; defaults to `'Chanbot'`)
   - `ICON_EMOJI`: the emoji used in the bot's icon. (optional; defaults to `':coffee:'`)
   - `CHANNEL`: the channel in which you stand up. (optional; defaults to `'#standup'`)
   - `IGNORE_USERS`: a string representing a comma-separated array of strings representing active channel users who never stand up. (eg `'["username1", "username2"]'`; optional; defaults to `''`)
   - `INIT_GREETING`: the way Chanbot greets you when a standup is initialized. (optional; defaults to `'Good morning'`)
   - `START_MESSAGE`: the instructions Chanbot issues when a standup starts. (optional; defaults to `'What did you work on yesterday? What are you working on today? What, if any, are your blockers?'`)
   - `GIPHY`: a string representing a boolean of whether you want to use Giphy on queries Chanbot doesn't understand. (optional; defaults to `FALSE`)
5. Add the URL where the web app is deployed as an [outgoing webhook](https://my.slack.com/services/new/outgoing-webhook) in Slack. Don't forget the trailing `/`! Use `yo` as your trigger. 
6. Type `!standup` in your chosen channel to start a new standup. (Need help? Type `!help`.)


## Original Project
Forked from [morgenbot](https://github.com/eelzon/morgenbot)