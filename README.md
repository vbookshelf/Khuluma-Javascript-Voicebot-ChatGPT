# Khuluma Voicebot - ChatGPT
Khuluma is ChatGPT with a voice. You can talk to Khuluma using both your voice and text.<br>
Khuluma means "speak" or "talk" in Zulu. It's one of the official languages of South Africa.

<br>
<img src="https://github.com/vbookshelf/Khuluma-Voicebot-ChatGPT/blob/main/images/app.png" height="500"></img>
<i>Khuluma Voicebot</i><br>
<br>

## Video demo

This is a link to a 24s video demo that's included in this repo. Please click "View raw" to download it.<br>
https://github.com/vbookshelf/Khuluma-Voicebot-ChatGPT/blob/main/images/khuluma_video.mp4

The voice recognition and text to speech are in real time - I haven't sped up the video. 

<br>

## How it works
- Javascript SpeechRecognition is used to convert the user's speech into text.
- This text is then sent to ChatGPT via the OpenAI API.
- Javascript SpeechSynthesis converts the response text into voice.
- The voice you'll hear is the default voice of your pc. It can be changed in your system settings.

<br>

## How to run the app
- Download the project folder and place it on your desktop.
- Add your OpenAI API key to the chatgpt-config.js file
- Open the index.html file in the Chrome browser. If Chrome is your default browser then you can simply doulble click the index.html file and it will open the app in your browser.
- Start chatting.

Please note that when running locally you'll need to allow access to your mic each time you want to speak, however when the app is running on a web server (like Dreamhost) you only need to allow access to the mic once. After that you can talk naturally - as demonstrated in the video.

If you want to deploy the app on a web server then you can simply upload it to your web host. There's nothing else you'll need to do because this app doesn't use any backend code like Python or PHP. But, please remember that if you upload this app to a web server your API key will be visible. You'll need to create some backend code to secure it.

<br>

## Features
- Voice and text interface.
- Runs in the Chrome browser.
- A simple design that uses only Javascript, HTML and CSS.
- Can be run locally or deployed to a low cost shared web hosting server.
- Khuluma has context memory.
- The chat can be saved.
- A saved chat can be loaded to resume the conversation.
- Takes advantage of the speed of Javascript.

<br>

## Possible applications
- English practice
- Chat companion for the elderly
- Mental health support
- Learning through conversation
- Practice social skills through roleplay e.g. networking event, job interview, first date etc.
- A voicebot can be used give people with disabilities a more accessible to way to interact with ChatGPT.

<br>

## System message

This is the system message that determines Khuluma's behaviour:

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

If you don't want Khuluma to ask for your name each time, please change the system_message in the chatgpt-config.js file.<br>
You can even add your name to the system message and make other changes.
For example you could add: You are chatting with Sarah. She is learning spanish.
<br>

## Notes
- This app only works in the Google Chrome browser.
- I built and tested this app on a Mac. It may operate slightly differently in Windows.
- When using Javscript to make the OpenAI API request the API key can't be hidden. Anyone can easily see it. Therefore, if deploying the app on a shared web hosting server it's better to make the API calls using PHP. Shared servers usually have PHP installed. They don't have Python installed. Here's an example of how to use PHP:<br>
https://github.com/vbookshelf/Maiya-ChatGPT-Experiments/blob/main/Exp_11--create-and-deploy-a-roleplay-english-practice-chatbot/chatgpt-api-code.php
- The voice recognition is not perfect, but it's still very good and very fast. If the voice recognition is finding it difficult to understand something you want to say, you can type it in.
- When the API is overloaded with requests the app returns an error. When this happens simply send your message again.
- The app will return an error when the context length for the model is exceeded. This will happen when the chat is very long.
- As the context grows, the number of tokens increases and therefore, the API cost will also increase. Please monitor your costs.
- I've found that it's best to have the app open in only one browser tab at a time. Having it open in more than one tab causes issues with the mic and the voice chat doesn't work.
- The code is not stable yet. There are times when the bot hears itself speaking and responds to it's own voice.
- This app needs a stable internet connection. If the bot is not working well, check that your internet connection is okay.

<br>

## App Image

Image by Milu Černochová on Pixabay<br>
https://pixabay.com/vectors/teacher-woman-gentlemen-ball-mum-1443455/

<br>

## Resources

- Speech Recognition App Using Vanilla JavaScript<br>
https://www.youtube.com/watch?v=-k-PgvbktX4

- Text To Speech Converter in HTML CSS & JavaScript | No External Library or API Used<br>
https://www.youtube.com/watch?v=cvZrppquLQg

- SpeechRecognition docs<br>
https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition

- SpeechSynthesis docs<br>
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

