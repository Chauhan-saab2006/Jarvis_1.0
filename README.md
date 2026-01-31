# Jarvis - AI Voice Assistant

Jarvis is a Python-based voice assistant powered by Google's Gemini AI. It listens to voice commands, processes them with AI, and responds with voice output.

## Features

- 🎤 **Voice Recognition**: Listens to commands using Google Speech Recognition
- 🤖 **AI Responses**: Uses Google Gemini 2.0 Flash for intelligent responses
- 🔊 **Text-to-Speech**: Provides spoken feedback using pyttsx3
- 🌐 **Web Integration**: Opens websites (YouTube, Wikipedia, Google, Instagram, WhatsApp, GitHub)
- 🎵 **Music**: Play songs on YouTube
- 💬 **Messaging**: Send messages via WhatsApp
- 🕐 **Time**: Tell the current time
- 🎮 **Application Launcher**: Open Chrome and Cursor
- 💬 **Chat Interface**: Interactive AI chat mode

## Prerequisites

- Python 3.13+
- Microphone (for voice input)
- Google API Key (Gemini API)
- Internet connection

## Installation

1. **Clone or download the project**
   ```bash
   cd e:\VS_DATA\jarvis
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv env
   .\env\Scripts\Activate.ps1
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   - Create a `.env` file in the project root
   - Add your Google API Key:
     ```
     GOOGLE_API_KEY=your_api_key_here
     ```

## Configuration

### Getting a Google API Key

1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Click "Create API Key"
3. Copy the key and paste it in your `.env` file

### Note on Quota

The Gemini API has a free tier with limited requests. For production use:
- Upgrade to a paid plan in [Google Cloud Console](https://console.cloud.google.com/)
- Monitor your usage at https://ai.dev/rate-limit

## Usage

Run the assistant:
```bash
python jarvis.py
```

### Commands

- **"open [website]"**: Opens YouTube, Wikipedia, Google, Instagram, WhatsApp, or GitHub
- **"time"**: Tells you the current time
- **"music"**: Play a song on YouTube (prompts for song name)
- **"message"**: Send a WhatsApp message (prompts for message and contact)
- **"open chrome"**: Opens Chrome browser
- **"open cursor"**: Opens Cursor IDE
- **"jarvis shutdown"**: Closes the application
- **Any other text**: Gets an AI response from Gemini

## Project Structure

```
jarvis/
├── jarvis.py              # Main application
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (API keys)
├── .gitignore            # Git ignore file
├── README.md             # This file
└── env/                  # Virtual environment
```

## Dependencies

- `google-generativeai`: Google Gemini API
- `pyttsx3`: Text-to-speech
- `SpeechRecognition`: Voice recognition
- `python-dotenv`: Environment variable management
- `pyautogui`: GUI automation
- `pyperclip`: Clipboard management
- `PyAudio`: Audio processing

## Troubleshooting

### "API key not found in environment variables"
- Ensure `.env` file exists in the project root
- Verify `GOOGLE_API_KEY=your_key` is in the `.env` file
- Restart the terminal after creating `.env`

### "Quota exceeded" error
- Your free tier quota has been exhausted
- Upgrade to a paid Google Cloud plan
- Check your billing details at [Google Cloud Console](https://console.cloud.google.com/)

### Microphone not working
- Ensure your microphone is connected and enabled
- Check Windows microphone permissions
- Run as administrator if needed

### Voice recognition fails
- Speak clearly into the microphone
- Reduce background noise
- Check internet connection (required for Google Speech Recognition)

## Security Notes

⚠️ **Never commit your `.env` file to version control**
- The `.gitignore` file protects it automatically
- Always keep your API key private
- Regenerate keys if accidentally exposed

## Future Enhancements

- [ ] Local speech recognition (offline)
- [ ] Natural language understanding improvements
- [ ] Custom voice profiles
- [ ] Task scheduling
- [ ] Multi-language support
- [ ] Integration with calendar and email

## License

This project is for personal use.

## Support

For issues or questions:
1. Check the troubleshooting section above
2. Review Google Gemini API documentation: https://ai.google.dev/
3. Check Google Speech Recognition issues: https://github.com/Uberi/speech_recognition
