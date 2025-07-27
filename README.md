# WhatsApp Gemini Bot

A simple WhatsApp bot that uses Google's Gemini AI to answer user questions.

## Features

- Responds to messages starting with `!ask`
- Uses Google Gemini AI for intelligent responses
- Built with Baileys WhatsApp library
- Simple and lightweight

## Prerequisites

- Node.js (version 16 or higher)
- A Google Gemini API key
- WhatsApp account

## Installation

1. Clone or download this repository
2. Install dependencies:
   ```bash
   npm install @whiskeysockets/baileys axios dotenv
   ```

3. Create a `.env` file in the project root:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

4. Replace `your_gemini_api_key_here` with your actual Gemini API key

## Getting a Gemini API Key

1. Go to Google AI Studio: https://makersuite.google.com/app/apikey
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy the generated API key

## Usage

1. Start the bot:
   ```bash
   node bot.js
   ```

2. Scan the QR code with your WhatsApp mobile app:
   - Open WhatsApp on your phone
   - Go to Settings > Linked Devices
   - Tap "Link a Device"
   - Scan the QR code displayed in your terminal

3. Send messages to the bot:
   - Send a message starting with `!ask` followed by your question
   - Example: `!ask What is the weather like?`
   - The bot will reply using Gemini AI

## Example

```
User: !ask What is JavaScript?
Bot: JavaScript is a high-level, interpreted programming language that is widely used for web development...
```

## File Structure

```
gemini-wp-bot/
├── bot.js              # Main bot script
├── .env                # Environment variables (create this)
├── .gitignore          # Git ignore file
├── package.json        # Node.js dependencies
└── README.md           # This file
```

## Troubleshooting

- If you get authentication errors, delete the `baileys_auth_info` folder and scan the QR code again
- Make sure your Gemini API key is valid and has sufficient quota
- Ensure you have a stable internet connection
- Check that Node.js version is 16 or higher

## Notes

- The bot only responds to messages starting with `!ask`
- Authentication data is stored in the `baileys_auth_info` folder
- The bot will automatically reconnect if the connection is lost
- Keep your API key secure and never commit it to version control
