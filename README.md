# Khuluma Voicebot - ChatGPT
Khuluma is ChatGPT with a voice. You can talk to Khuluma using both your voice and text.<br>
Khuluma means "speak" or "talk" in Zulu. It's one of the official languages of South Africa.


I never expected this simple design to work so well.

<br>
<img src="https://github.com/vbookshelf/Khuluma-Voicebot-ChatGPT/blob/main/images/app.png" height="500"></img>
<i>Khuluma Voicebot</i><br>
<br>

<br>

## How to run the app
- Download the project folder and place it on your desktop.
- Add your OpenAI API key to the chatgpt-config.js file
- Open the index.html file in the Chrome browser. If Chrome is your default browser then you can simply doulble click the index.html file and it will open the app in your browser.
- Start chatting.

Please note that when running locally you'll need to allow access to your mic each time you want to speak, however when the app is running on a web server (like Dreamhost) you only need to allow access to the mic once. After that you can talk naturally. 

If you want to deploy the app on a web server then you can simply upload it to your web host. There's nothing else you'll need to do because this app doesn't use any backend code like Python or PHP. But, please remember that if you upload this app to a web server your API key will be visible. You'll need to create some backend code to secure it.

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
- The voice you'll hear is the default voice of your pc. It can be changed.

<br>

## Possible applications
- English practice
- Chat companion for the elderly
- Mental health support
- Learning through engaging conversation
- Practice social skills through roleplay e.g. networking event, job interview, first date etc.

<br>

## System message

This is the system message that determines the bot's behaviour:

```
system_setup_message = `
Your name is ${bot_name}. You are a kind and friendly chat companion.
The user's words are being converted from speech to text using Javascript SpeechRecognition.
The speech recognition text may contain errors.
You optimize for poor quality speech detection.
Your responses are being converted from text to speech using Javascript SpeechSynthesis.
You optimize your responses for SpeechSynthesis.
You add a full stop at the end of each bullet point.
You always greet the user, introduce yourself and ask for their name.
`;

```
<br>

## Resources

- Speech Recognition App Using Vanilla JavaScript<br>
https://www.youtube.com/watch?v=-k-PgvbktX4

- Text To Speech Converter in HTML CSS & JavaScript | No External Library or API Used<br>
https://www.youtube.com/watch?v=cvZrppquLQg

- SpeechRecognition<br>
https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition

- SpeechSynthesis<br>
https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis

- Change the voice your Mac uses to speak text<br>
https://support.apple.com/guide/mac-help/change-the-voice-your-mac-uses-to-speak-text-mchlp2290/mac

- Andrew Ng course:<br>
ChatGPT Prompt Engineering for Developers<br>
https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/

- Maiya ChatGPT Experiments<br>
https://github.com/vbookshelf/Maiya-ChatGPT-Experiments

<br>

## Comments
Feel free to share your comments in the discussion forum:<br>
https://github.com/vbookshelf/Khuluma-Voicebot-ChatGPT/discussions/1

<br>
