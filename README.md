# Khuluma Voicebot - ChatGPT
Khuluma is ChatGPT with a voice. You can talk to Khuluma using both your voice and text.<br>
Khuluma means "speak" or "talk" in Zulu. It's one of the official languages of South Africa.

<br>

## How to run the app
- Download the project folder and place it on your desktop.
- Add your OpenAI API key to the chatgpt-config.js file
- Open the index.html file in the Chrome browser. If Chrome is your default browser then you can simmply doulble click the index.html file and it will open the app in your browser.
- Start chatting.

Please note that when running locally you'll need to allow access to your mic each time you want to speak, however when the app is running on a web server (like Dreamhost) you only need to allow access to the mic once. After that you can talk naturally.

<br>

## Features
- Voice and text interface.
- Runs in the Chrome browser.
- A simple design that uses only Javascript, HTML and CSS.
- Can be run locally or deployed to a low cost shared web hosting server.
- The voicebot has context memory.
- The chat can be saved.
- A saved chat can be loaded to resume the conversation.
- Takes advantage of the speed of Javascript.

<br>

## How it works
- Javascript SpeechRecognition is used to convert the user's speech into text.
- This text is then sent to ChatGPT via the OpenAI API.
- Javascript SpeechSynthesis converts the response text into voice.
- The voice the the default voice of your pc. It can be changed.

<br>

## Possible applications
- English practice
- Chat companion for the elderly
- Mental health support
- Learning through engaging conversation
- Practice social skills and learn assertiveness through roleplay e.g. networking event, job interview, first date, dealing with rude people etc.
