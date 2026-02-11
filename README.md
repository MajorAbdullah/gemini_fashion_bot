# Gemini Fashion Bot
### An AI-powered personal fashion assistant built with Flutter and Google Gemini

Gemini Fashion Bot is a cross-platform mobile application that provides personalized fashion advice through a conversational chat interface. Powered by Google's Gemini 2.0 Flash API, it can analyze outfit images, recommend color palettes, suggest styling alternatives, and provide shopping links -- all in a natural, friendly tone.

---

## Features

- **AI Fashion Chat** -- Conversational interface where users ask fashion questions and receive natural language styling advice from Google Gemini
- **Outfit Image Analysis** -- Upload photos from camera or gallery; the Gemini vision model analyzes clothing items, color matches, and styling opportunities
- **Premade Prompt Chips** -- Quick-access horizontal chip bar with common fashion questions like "How to style jeans for a night out?" and "What colors match with my skin tone?"
- **Color Palette Recommendations** -- Dedicated palette button that prompts Gemini to suggest wardrobe color schemes based on uploaded images
- **Shopping Link Suggestions** -- When recommending outfits or accessories, the bot includes actionable website links for purchasing
- **Clickable URLs** -- Bot messages use `flutter_linkify` to render tappable hyperlinks that open in the device browser
- **Animated Typing Indicator** -- Three-dot fade animation shows when the bot is generating a response
- **Image Preview with Cancel** -- Selected images appear as a thumbnail preview with a remove button before sending
- **Body Type and Skin Tone Advice** -- The AI assistant provides guidance tailored to body types, skin undertones, and seasonal trends
- **Sustainable Fashion Tips** -- Includes eco-friendly fashion suggestions and wardrobe organization advice
- **Secure API Key Handling** -- Gemini API key loaded from a local `api_keys.dart` file excluded from version control

---

## Tech Stack

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Material Design](https://img.shields.io/badge/Material_Design-757575?style=for-the-badge&logo=materialdesign&logoColor=white)

---

## Getting Started

### Prerequisites

- Flutter SDK (>=3.6.0)
- Dart SDK (>=3.6.0)
- A Google Gemini API key ([get one here](https://aistudio.google.com/app/apikey))
- Android Studio or VS Code with Flutter extensions

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/MajorAbdullah/gemini_fashion_bot.git
   ```
2. Navigate to the project directory:
   ```bash
   cd gemini_fashion_bot
   ```
3. Create the API key file:
   ```bash
   echo "const geminiApiKey = 'YOUR_GEMINI_API_KEY';" > lib/api_keys.dart
   ```
4. Install dependencies:
   ```bash
   flutter pub get
   ```
5. Run the application:
   ```bash
   flutter run
   ```

> **Security Note:** Never commit your `lib/api_keys.dart` file to a public repository. It is excluded via `.gitignore`.

---

## Usage

1. **Launch the app** -- The chat screen opens with premade prompt chips at the top.
2. **Ask a question** -- Type a fashion question in the text field or tap a premade prompt chip to populate it.
3. **Upload an outfit photo** -- Tap the photo icon in the text field to take a picture or select from gallery. A preview thumbnail appears before sending.
4. **Get AI advice** -- The bot analyzes your text and/or image and responds with styling tips, color recommendations, and shopping links.
5. **Color palette mode** -- Tap the palette icon in the app bar to set the prompt to wardrobe color palette analysis, then upload an image.
6. **Follow links** -- Tap any blue hyperlink in bot messages to open shopping websites in your browser.

---

## Project Structure

```
gemini_fashion_bot/
|-- lib/
|   |-- main.dart              # App entry point, chat UI, image picker, Gemini API service, message rendering
|   |-- api_keys.dart          # Local API key storage (not committed to version control)
|-- android/                   # Android platform configuration
|-- pubspec.yaml               # Flutter dependencies and configuration
|-- analysis_options.yaml      # Dart linting rules
|-- README.md                  # Project documentation
```

---

## Key Dependencies

| Package | Purpose |
|---------|---------|
| `http` | HTTP requests to the Gemini generative language REST API |
| `image_picker` | Camera and gallery image selection |
| `flutter_linkify` | Automatic link detection and rendering in chat messages |
| `url_launcher` | Opens URLs in the device browser |
| `google_generative_ai` | Google Generative AI SDK |
| `flutter_bloc` | State management |
| `cached_network_image` | Efficient image caching |
| `speech_to_text` | Voice input support |
| `palette_generator` | Color palette extraction from images |

---

## How It Works

1. The user sends a text query or image through the chat interface.
2. The `ApiService` class constructs a prompt with fashion-specific system instructions (the "StyleBot" persona) and sends it to the Gemini 2.0 Flash API endpoint.
3. For image queries, the image is Base64-encoded and sent as inline data alongside the text prompt.
4. The API response is cleaned of markdown formatting artifacts and displayed as a styled chat bubble with clickable links.

---

## Contributing

Contributions are welcome. Please fork this repository, create a feature branch, and submit a pull request. Ensure API keys and other sensitive data are never exposed in commits.

---

## License

MIT

---

## Contact

- **GitHub:** [MajorAbdullah](https://github.com/MajorAbdullah)
- **Email:** sa.abdullahshah.2001@gmail.com
