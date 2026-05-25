# AI Chatbot 🤖

A modern, ChatGPT-like AI chatbot built with Next.js, TypeScript, and OpenAI API.

![License](https://img.shields.io/badge/license-MIT-blue)
![Node](https://img.shields.io/badge/node-%3E%3D18-brightgreen)
![Next.js](https://img.shields.io/badge/next.js-14-black)

## Features ✨

- 💬 **Real-time Chat Interface** - Smooth, responsive chat UI
- 🎨 **Dark Mode Support** - Built-in light/dark theme toggle
- ⚡ **Fast & Responsive** - Optimized performance with Next.js
- 🔒 **Secure** - Environment variables for API key management
- 📱 **Mobile Friendly** - Fully responsive design
- 💾 **Conversation History** - Keep track of chat messages
- 🎯 **Type-Safe** - Full TypeScript support
- 🚀 **Production Ready** - Proper error handling & logging

## Tech Stack

- **Frontend**: Next.js 14, React 18, TypeScript, Tailwind CSS
- **Backend**: Next.js API Routes
- **AI**: OpenAI API (GPT-3.5 Turbo / GPT-4)
- **Styling**: Tailwind CSS with dark mode
- **Deployment**: Vercel-ready

## Prerequisites

- Node.js 18+
- npm or yarn
- OpenAI API key ([Get one here](https://platform.openai.com/api-keys))

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/varunverse22/ai-chatbot.git
cd ai-chatbot
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Set Up Environment Variables

Create a `.env.local` file in the root directory:

```env
OPENAI_API_KEY=your_openai_api_key_here
NEXT_PUBLIC_MODEL=gpt-3.5-turbo
NEXT_PUBLIC_MAX_TOKENS=2000
```

**Get your OpenAI API key:**
1. Go to [OpenAI Platform](https://platform.openai.com/)
2. Sign up or log in
3. Navigate to [API keys](https://platform.openai.com/api-keys)
4. Click "Create new secret key"
5. Copy and paste it into `.env.local`

### 4. Run Development Server

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Usage

1. Type your message in the input box
2. Press `Enter` to send (or `Shift+Enter` for new line)
3. The AI will respond in real-time
4. Clear chat history with the "Clear" button

## Project Structure

```
ai-chatbot/
├── app/
│   ├── api/
│   │   └── chat/route.ts          # OpenAI API integration
│   ├── components/
│   │   ├── ChatBox.tsx            # Message input
│   │   ├── Message.tsx            # Message display
│   │   └── Header.tsx             # App header
│   ├── globals.css                # Global styles
│   ├── layout.tsx                 # Root layout
│   └── page.tsx                   # Home page
├── public/                        # Static assets
├── .env.local.example             # Environment variables template
├── .gitignore
├── next.config.js
├── package.json
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

## API Endpoint

### POST /api/chat

Sends a message and gets AI response.

**Request:**
```json
{
  "messages": [
    { "role": "user", "content": "Hello" },
    { "role": "assistant", "content": "Hi there!" }
  ],
  "userMessage": "How are you?"
}
```

**Response:**
```json
{
  "message": "I'm doing well, thank you for asking!",
  "model": "gpt-3.5-turbo"
}
```

## Deployment

### Deploy to Vercel (Recommended)

1. Push code to GitHub
2. Go to [Vercel](https://vercel.com)
3. Import project from GitHub
4. Add environment variables in project settings:
   - `OPENAI_API_KEY`: Your OpenAI API key
5. Deploy!

```bash
# Or deploy via CLI
vercel
```

## Scripts

```bash
npm run dev        # Start development server
npm run build      # Build for production
npm start          # Start production server
npm run lint       # Run ESLint
npm run type-check # Run TypeScript type check
```

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `OPENAI_API_KEY` | Your OpenAI API key (required) | - |
| `NEXT_PUBLIC_MODEL` | AI model to use | `gpt-3.5-turbo` |
| `NEXT_PUBLIC_MAX_TOKENS` | Max tokens per response | `2000` |
| `NEXT_PUBLIC_API_URL` | API base URL | `http://localhost:3000` |

## Customization

### Change AI Model

Edit `.env.local`:
```env
NEXT_PUBLIC_MODEL=gpt-4
```

### Adjust Temperature & Max Tokens

Edit `app/api/chat/route.ts`:
```typescript
{
  temperature: 0.7,      // 0-2 (higher = more creative)
  max_tokens: 2000       // Adjust response length
}
```

### Customize Styling

Edit `tailwind.config.js` and `app/globals.css`

## Performance Optimization

- ✅ Code splitting with Next.js
- ✅ Image optimization
- ✅ CSS minification
- ✅ API route caching
- ✅ Dynamic imports

## Security

- ✅ Environment variables for sensitive data
- ✅ API key never exposed to client
- ✅ Server-side API calls only
- ✅ CORS headers properly configured
- ✅ Input validation
- ✅ Error handling without exposing details

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md)

## License

MIT License - see [LICENSE](LICENSE) file

## Support

For issues or questions:
- Open an [issue](https://github.com/varunverse22/ai-chatbot/issues)
- Check [existing issues](https://github.com/varunverse22/ai-chatbot/issues)
- Read [documentation](README.md)

## Roadmap 🗺️

- [ ] Voice input/output
- [ ] Image generation
- [ ] Chat export (PDF, JSON)
- [ ] User authentication
- [ ] Chat history database
- [ ] Conversation sharing
- [ ] Custom system prompts
- [ ] Multi-language support
- [ ] Rate limiting UI
- [ ] Analytics dashboard

## Author

**Varun Verse** - [@varunverse22](https://github.com/varunverse22)

---

⭐ If you found this helpful, please star the repository!
