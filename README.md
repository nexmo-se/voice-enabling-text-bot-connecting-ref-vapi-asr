# Vonage API - Voice enabling a text-only bot reference connection code

You can use this very simple text-only to chatbot to simulate a real chatbot for demo purpose.


## About this very simple chatbot

See https://github.com/nexmo-se/voice-enabling-text-bot-sample-app-vapi-asr for a **sample Voice API application** using this very simple chatbot to connect voice calls and get a voice interaction with this text-only bot.

You may edit the source code file very-simple-bot.js to add additional sample requests/responses in the dictionaries and create new ones for additional languages.

### Local deployment

To run your own instance of this sample application locally, you'll need an up-to-date version of Node.js (we tested with version 14.3.0).

Download this sample application code to a local folder, then go to that folder.

Install dependencies once:
```bash
npm install
```

Launch the applicatiom:
```bash
node very-simple-bot
```

### Command Line Heroku deployment

You must first have deployed your application locally, as explained in previous section, and verified it is working.

Install [git](https://git-scm.com/downloads).

Install [Heroku command line](https://devcenter.heroku.com/categories/command-line) and login to your Heroku account.

If you do not yet have a local git repository, create one:</br>
```bash
git init
git add .
git commit -am "initial"
```

Start by creating this application on Heroku from the command line using the Heroku CLI:

```bash
heroku create myappname
```

Note: In above command, replace "myappname" with a unique name on the whole Heroku platform.

On your Heroku dashboard where your application page is shown, click on `Settings` button,
add the following `Config Vars` and set it with its argument:</br>
GOOGLE_APPLICATION_CREDENTIALS</br>

Deploy the application:

```bash
git push heroku master
```

### Connecting server code to use

To simulate the voice interaction with a text-only bot, you may use this very simple chatbot code
```bash
node very-simple-bot.js
```
with the client application (from https://github.com/nexmo-se/voice-enabling-text-bot-sample-app-vapi-asr)
```bash 
node voice-on-text-bot-app-with-simple-bot.js
```

--------

To just see the ASR results, you may use you may use this very simple chatbot code
```bash
node very-simple-bot.js
```

with the client application (from https://github.com/nexmo-se/voice-enabling-text-bot-sample-app-vapi-asr)
```bash 
node voice-on-text-bot-app-generic.js
```

of course, you would need to add your own code in this client application to interact with your actual text-only chatbot.







