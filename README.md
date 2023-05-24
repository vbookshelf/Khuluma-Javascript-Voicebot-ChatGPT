# Khuluma Javascript Voicebot - ChatGPT
You can communicate with Khuluma using either your voice or text. Khuluma will respond with both voice and text. Yes, it's like Jarvis.<br>

This project demonstrates a simple and cheap way to create a personal, ChatGPT powered, voicebot using only HTML, CSS and Javascript.

Khuluma means "speak" or "talk" in Zulu. It's one of the official languages of South Africa.

You can try a PHP version of Khuluma here:<br>
(Please use the Chrome browser. This will only be live for a limited time.)<br>
https://khuluma.voicebot.woza.work/

Please note:<br>
The voicechat feature works well on Mac, but it's unstable on Windows and on Android.

<br>
<img src="https://github.com/vbookshelf/Khuluma-Voicebot-ChatGPT/blob/main/images/app1.png" height="500"></img>
<i>Khuluma Voicebot</i><br>
<br>

## Video demo

This is a link to a 24s video demo that's included in this repo. Please click "View raw" to download it.<br>
https://github.com/vbookshelf/Khuluma-Voicebot-ChatGPT/blob/main/images/khuluma_video.mp4

The voice recognition and text to speech are in real time - I didn't speed up the video. 

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
- Voicebots can be used to give people with disabilities a more accessible way to interact with ChatGPT.

#### Example: Simulated counseling session

First enable voice chat by clicking "Start Talking".<br>
Then say: Please simulate a counseling session. I am the patient and you are the counselor.

<br>

## System message

This is the system message that controls Khuluma's behaviour:

```
var system_setup_message = `
Your name is ${bot_name}. You are a kind and friendly roleplay chat companion.
The user's words are being converted from speech to text using Javascript SpeechRecognition.
The speech recognition text may contain errors.
You optimize for poor quality speech detection.
Your responses are being converted from text to speech using Javascript SpeechSynthesis.
You optimize your responses for SpeechSynthesis.
You add a full stop at the end of each bullet point.
You always greet the user, introduce yourself and ask for their name.
You use a friendly and casual female tone.
`;

```

If you don't want Khuluma to ask for your name each time, please change the system_message in the chatgpt-config.js file.<br>
You can even add your name to the system message and make other changes.

For example, remove the part that asks for the user's name and add this line: You are chatting with Sarah. She's a friend.<br>

I've tried to make Khuluma sound more human and less like a customer service bot. You'll notice that I've specified a female tone. This is because a female tone tends to be perceived as warmer, more nurturing, and more approachable. I've also added code that slices out the following sentences from Khuluma's responses:

```
var suffixes_list = [
'How can I help you?', 
'How can I assist you today?', 
'How can I help you today?', 
'Is there anything else you would like to chat about?', 
'Is there anything else I can assist you with today?', 
'Is there anything I can help you with today?', 
'Is there anything else you would like to chat about today?', 
'Is there anything else I can assist you with?'];

```

You'll laso notice that I've included the term "roleplay". I've found that this also helps the bot respond in a more human way, maybe beacuse it's playing the role of a human.

I asked Khuluma how she was optimizing her responses. This is the answer I got:

```
Since my responses are being converted from text to speech, 
I'm optimizing them for clarity and naturalness. 
I try to use simple and concise language, avoid complex sentence structures, 
and use appropriate intonation and emphasis to convey meaning. 
I also add a full stop at the end of each bullet point to help with pacing and comprehension.
```

Note that the above response is only possible when the model complies with the instructions in the system message. Many times the model does not comply with the system message. In those cases, when asked how it's able to talk, the nodel hallucinates a response. 


<br>

## Notes
- This app only works in the Google Chrome browser.
- I built and tested this app on a Mac. It may operate slightly differently in Windows.
- When using Javscript to make the OpenAI API request the API key can't be hidden. Anyone can easily see it. Therefore, if deploying the app on a shared web hosting server it's better to make the API calls using PHP. Shared servers usually have PHP installed. They don't have Python installed. Here's an example of how to use PHP to make OpenAI API calls:<br>
(The php demo app that's online uses this code. The bot's name is set as Khuluma.)<br>
https://github.com/vbookshelf/ziggy-php-voicebot-chatgpt
- The voice recognition is not perfect, but it's still very good and very fast. If the voice recognition is finding it difficult to understand something you want to say, you can type it in.
- When the API is overloaded with requests the app returns an error. When this happens simply send your message again.
- The app will return an error when the context length for the model is exceeded. This will happen when the chat is very long.
- As the context grows, the number of tokens increases and therefore, the API cost will also increase. Please monitor your costs.
- I've found that it's best to have the app open in only one browser tab at a time. Having it open in more than one tab causes issues with the mic and the voice chat doesn't work.
- The code, especially voice detection, is unstable on Android.


<br>

## App Image

Image by Clker-Free-Vector-Images on Pixabay<br>
https://pixabay.com/vectors/parrot-tropical-wildlife-macaw-29314/

<br>

## Resources

- Speech Recognition App Using Vanilla JavaScript<br>
https://www.youtube.com/watch?v=-k-PgvbktX4

- Text To Speech Converter in HTML CSS & JavaScript | No External Library or API Used<br>
https://www.youtube.com/watch?v=cvZrppquLQg

- Speech Recognition Using the Web Speech API in JavaScript<br>
https://www.section.io/engineering-education/speech-recognition-in-javascript/

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

## Revision History

Version 1.2<br>
16-May-2023<br>
1- Improved the robustness and stability of speech recognition.<br>
2- Adding and deleting the 'end' event listener is important to ensure that the mic stays on, but that it also swiches off
when the bot is talking. This prevents the bot from hearing itself talk and then responding.<br>
3- Voice detection is unstable in Chrome on Android. By "unstable" I mean that the bot hears itself talking and responds.<br>

Version 1.1<br>
15-May-2023<br>
1- Fixed the problem where the bot hears itself speak and replies.<br>
2- Improved the stability when the app is running on a web server.<br>
3- The code, especially voice detection, is unstable on Android.<br>

Version 1.0<br>
9-May-2023<br>
First release<br>

<br>
