# ESV Theological Research & Study Guide

A React-based biblical study assistant that provides sound Reformed theological teaching based on Scripture and trusted expositional resources. This tool is designed to help non-denominational Christian households and business owners understand and apply God's Word through careful biblical exposition.

## Important Disclaimer

This application is a study tool created to assist with biblical research. It is NOT:
- A spiritual authority or replacement for the Holy Spirit
- A pastor, elder, or church leader
- A substitute for personal Bible study and prayer
- A replacement for local church leadership and pastoral counsel

**Always verify teachings against Scripture and seek guidance from your local church.**

## Features

- **Verse Study**: Deep dive into specific Bible passages with theological context
- **Topical Research**: Explore biblical doctrines and themes
- **Deep Study**: Comprehensive analysis with cross-references and historical context
- **Reformed Framework**: Grounded in literal-historical-grammatical interpretation
- **Conversational Interface**: Natural dialogue for follow-up questions
- **Dark Theme**: Easy-on-the-eyes interface for extended study sessions

## Theological Framework

This assistant aligns with:
- The expositional teaching of John MacArthur
- Reformed tradition and doctrine
- Literal-historical-grammatical interpretation
- ESV as primary translation (with Amplified for context)

**Scripture is always the final authority.**

## Prerequisites

- Node.js (v18 or higher recommended)
- npm or yarn package manager
- Anthropic API key (get one at [https://console.anthropic.com/](https://console.anthropic.com/))

## Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd james_3_17_ai
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```

4. Add your Anthropic API key to `.env`:
```
VITE_ANTHROPIC_API_KEY=your_actual_api_key_here
```

**Important**: Never commit your `.env` file to version control. The `.gitignore` file is configured to prevent this.

## Usage

### Development Mode

Start the development server:
```bash
npm run dev
```

The application will open at `http://localhost:3000`

### Production Build

Build for production:
```bash
npm run build
```

Preview production build:
```bash
npm run preview
```

## How to Use

1. **Choose Your Study Type**: Select from Verse Study, Topical Research, or Deep Study tabs
2. **Start with Examples**: Click any example prompt to begin, or type your own question
3. **Ask Follow-up Questions**: Engage in natural dialogue to go deeper
4. **Reset When Done**: Click "New Study" to start a fresh conversation

### Example Questions

**Verse Study:**
- "Explain Romans 8:28-30 and its theological significance"
- "What does John 3:16 teach about salvation?"
- "Help me understand Ephesians 2:8-9 in context"

**Topical Research:**
- "What does the Bible teach about justification by faith?"
- "Explain the doctrine of the Trinity from Scripture"
- "What is biblical sanctification?"

**Deep Study:**
- "Provide cross-references for verses about God's sovereignty"
- "What's the historical context of the book of Romans?"
- "Compare election in Romans 9 with other passages"

## Project Structure

```
james_3_17_ai/
├── src/
│   ├── ESVTheologicalStudyGuide.jsx  # Main component
│   ├── main.jsx                       # Application entry point
│   └── index.css                      # Global styles with Tailwind
├── public/                            # Static assets
├── index.html                         # HTML template
├── vite.config.js                     # Vite configuration
├── tailwind.config.js                 # Tailwind CSS configuration
├── postcss.config.js                  # PostCSS configuration
├── package.json                       # Dependencies and scripts
└── .env.example                       # Environment variables template
```

## Technology Stack

- **React 18**: UI framework
- **Vite**: Build tool and dev server
- **Tailwind CSS**: Utility-first styling
- **Lucide React**: Icon library
- **Anthropic Claude API**: AI-powered study assistant (claude-sonnet-4)

## API Usage and Costs

This application uses the Anthropic Claude API. Each conversation with the study assistant consumes API tokens:
- Input tokens: System prompt + conversation history + user message
- Output tokens: Assistant's response

**Estimated costs** (as of 2025):
- The system prompt is approximately 3,500 tokens
- Average conversation may use 5,000-15,000 tokens total
- Check current pricing at [https://www.anthropic.com/pricing](https://www.anthropic.com/pricing)

**Tips to manage costs:**
- Click "New Study" to reset conversation history when switching topics
- Be specific with your questions to get focused responses
- Monitor your API usage in the Anthropic Console

## Security Notes

1. **API Key Protection**: Never share your `.env` file or commit it to version control
2. **Client-Side API Calls**: This application makes API calls directly from the browser. For production use, consider:
   - Setting up a backend proxy to hide your API key
   - Implementing rate limiting
   - Adding user authentication

## Customization

### Changing the Theological Framework

The system prompt in `src/ESVTheologicalStudyGuide.jsx` defines the theological framework. To modify:
1. Locate the `systemPrompt` constant (around line 12)
2. Carefully edit the prompt to reflect your desired theological perspective
3. Test thoroughly to ensure consistent, sound responses

### Styling

The application uses Tailwind CSS for styling. Key color values:
- Primary accent: `#8b0000` (dark red)
- Background: `#1e1e1e` (dark gray)
- Cards: `#2d2d2d` (medium gray)
- Text: `#e8e8e8` (light gray)

Modify these in `src/ESVTheologicalStudyGuide.jsx` or create custom Tailwind classes in `tailwind.config.js`.

## Troubleshooting

**API Key Error**: If you see "Error connecting to the study assistant", verify:
- Your `.env` file exists with `VITE_ANTHROPIC_API_KEY` set
- The API key is valid and has available credits
- You've restarted the dev server after adding the `.env` file

**Build Errors**: Clear the cache and reinstall:
```bash
rm -rf node_modules package-lock.json
npm install
```

**Styling Issues**: Rebuild Tailwind:
```bash
npm run build
```

## Contributing

This is a theological study tool. Contributions should:
1. Maintain biblical fidelity and sound doctrine
2. Respect the Reformed theological framework
3. Improve usability and clarity
4. Include appropriate testing

## License

[Add your chosen license here]

## Acknowledgments

- **Scripture quotations** are from The Holy Bible, English Standard Version® (ESV®)
- Theological framework influenced by the teaching ministry of John MacArthur
- Built with modern web technologies and the Claude AI API

---

**"All Scripture is breathed out by God and profitable for teaching, for reproof, for correction, and for training in righteousness, that the man of God may be complete, equipped for every good work." - 2 Timothy 3:16-17 (ESV)**