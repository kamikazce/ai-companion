# AI companion

## Currently, the project is being rewritten, version 0.9.8, is still based on the previous code

![logo](https://raw.githubusercontent.com/Hukasx0/ai-companion/main/public/ai_companion_logo.jpg)

![License](https://img.shields.io/github/license/Hukasx0/ai-companion)
![Downloads](https://img.shields.io/github/downloads/Hukasx0/ai-companion/total)


AI Companion is a project that aims to provide users with their own personal AI chatbot on their computer. It allows users to engage in friendly and natural conversations with their AI, creating a unique and personalized experience.
This software can also be used as a backend or API for other projects that require a personalised AI chatbot.

## Features
- works locally - does not require API keys for other services, which makes it completely free to use (well, apart from electricity costs - your computer must work somehow), also does not require the Internet to work
- privacy - all conversations are kept locally in the SQLite database, which means that your conversations or the characteristics of your AI stay only on your computer
- API - you can use it as a backend for your other projects that requires LLMs, custom ai chatbots or custom ai characters
- speed - wrote in Rust shows good efficiency when it comes to CPU (nothing slows your generation) and RAM (you don't need to use weaker ai models)
- ease of use - everything can be changed in web user interface, and everything is compiled into a single binary file that can be launched on your machine (no need for playing with hundreds of confusing
files, and no need to fight with wrong library/interpreter/framework versions)
- customization - you can change the AI's name, personality, appearance and the first message sent. Also short term and long term memory of ai can be modified
- short-term memory - artificial intelligence remembers recently received/sent messages
- long-term memory - AI can remember conversations even thousands of prompts later using long-term memory - associating things with different words, phrases or sentences
- real-time learning - when chatting with the AI, it is able to create "memories" as well as learn about the people it chats with (what their profession is, what they like to eat, drink and so on)
- feeding ai with custom data - using the API, it is possible to save to the AI's long-term memory, e.g. fragments of documents, articles, song lyrics, poems
- roleplay - ai chatbot can (if enabled) perform actions between asterisks (*) e.g. *moves closer*, *waves hello*
- you can load character files in .json or .png (character cards) format. For example, you can create your own [here](https://zoltanai.github.io/character-editor/)
- import and export messages via json
- you can use {{char}} and {{user}} in companion's persona, example dialogue, first message and user persona (if you change username or companion name, you don't need to change these, it will automatically change)

## API documentation
API documentation can be found here

## Projects based on ai-companion Backend/API/Library
- [local assistant](https://github.com/Hukasx0/local-assistant) - llm powered ai virtual assistant
- [matrix companion bot](https://github.com/Hukasx0/matrix-companion-bot) - AI-based chat bot running on the Matrix protocol 

## ~~Use as python library~~ (Deprecated)
~~If you are looking for a Python library that allows you to use the ai-companion backend in your projects, it is available here [ai-companion-py](https://github.com/Hukasx0/ai-companion-py)~~

## installation

### Recommended
go to https://github.com/Hukasx0/ai-companion/releases/tag/0.9.8
and depending on your system select [download_linux.sh](https://github.com/Hukasx0/ai-companion/releases/download/0.9.8/download_linux.sh) or [download_windows.bat](https://github.com/Hukasx0/ai-companion/releases/download/0.9.8/download_windows.bat), after running the script, all files will be downloaded and placed in the correct folders

### Manual installation
create a folder AI_companion, navigate to it, then install [AI_companion](https://github.com/Hukasx0/ai-companion/releases/download/0.9.8/ai_companion) or [AI_companion.exe](https://github.com/Hukasx0/ai-companion/releases/download/0.9.8/ai_companion.exe) (depending on your system), then create a folder 'models/' and put [AI model](#supported-ai-models) there,
on linux that's it, on windows you still need:
download sqlite from [here](https://www.sqlite.org/2023/sqlite-dll-win64-x64-3420000.zip)
and extract in the same folder where AI_companion.exe is located

## Supported AI models
small list of tested and working AI models:
- Only GGUF models are supported

## Compilation from source code:
To build an executable file you need: [Node.js and npm](https://nodejs.org/), [Rust and cargo](https://www.rust-lang.org/)

make a git clone of the repository:
```
git clone https://github.com/Hukasx0/ai-companion
```
go to the folder
```
cd ai-companion/
```
install node modules
```
npm i
```
compile everything into one binary
```
npm run build-full
```
(after compilation the binary should be in ai-companion/backend/target/release)

and then proceed the same as for manual installation
