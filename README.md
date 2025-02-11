# GaiaBOT - AI Chat Integration

A Node.js application that integrates Groq and Gaianet AI services for interactive chat conversations about Paris tourism.

## Features

- Dual AI interaction (Groq as user, Gaianet as assistant)
- Automatic topic rotation
- Colorful console output
- Smart retry mechanism
- Progress countdown timer
- Error handling and recovery

## Prerequisites

- Node.js 18 or higher
- npm (Node Package Manager)
- Gaianet account
- Groq API key

## Installation

1. Clone the repository:

```bash
git clone https://github.com/anantaabdlh/Gaia-BOT.git
cd Gaia-BOT
```

2. Install dependencies:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
echo 'export NVM_DIR="$HOME/.nvm"' >> $HOME/.bash_profile
echo '[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm' >> $HOME/.bash_profile
echo '[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion' >> $HOME/.bash_profile

source $HOME/.bash_profile
nvm install --lts
node -v
npm -v
npm install
npm intall openai
```

3. edit configuration files:

## Configuration

### 1. Gaianet Setup

1. Go to [Gaia Apikey](https://www.gaianet.ai/gaia-domain-name?referralCode=R5NUx0)
2. Create Api key
3. Paste the token into `data.txt`

### 2. OPENAI Setup

1. Visit [OPENAI Console](https://platform.openai.com/settings/organization/api-keys)
2. Create a new API key
3. Copy the API key and replace it in `main.js`:

```javascript
const API_KEYS = {
  OPENAI: "your_openai_api_key_here",
};
```

## Usage

Run the application:

```bash
node main.js
```

The bot will:

1. Load configurations and display banner
2. Connect to both AI services
3. Start cycling through tourism topics
4. Display colored conversation output
5. Handle errors and retry automatically

## Configuration Options

You can modify various settings in `main.js`:

- `RETRY_CONFIG`: Adjust retry attempts and wait times
- `TOPICS`: Customize conversation topics
- `SYSTEM_PROMPTS`: Modify AI behavior prompts
- `MODEL_CONFIG`: Adjust AI model parameters

## Error Handling

The application includes:

- Exponential backoff for retries
- Token validation
- Stream parsing error recovery
- Network error handling

## Dependencies

- `node-fetch`: HTTP client
- `groq-sdk`: Groq AI integration
- `figlet`: ASCII art banner
- `winston`: Logging system

## Project Structure

```
gaiabot/
├── config/
│   ├── banner.js
│   ├── colors.js
│   ├── countdown.js
│   └── logger.js
├── main.js
├── data.txt
└── README.md
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you encounter any issues or have questions:

1. Check the error logs
2. Verify your API keys and tokens
3. Ensure all prerequisites are met
4. Create an issue in the repository
