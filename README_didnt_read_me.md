# Gemini Fashion Bot

Gemini Fashion Bot is a Flutter-based personal fashion assistant app powered by Google's Gemini API. It provides users with fashion advice, analyzes images of outfits, and suggests shopping links, all in a friendly conversational interface.

## Features
- Chat-based fashion advice
- Image analysis for outfit suggestions
- Premade prompt chips for quick questions
- Color palette recommendations
- Body type-specific tips
- Sustainable and seasonal fashion suggestions
- Shopping links for recommended outfits
- Modern, responsive UI

## Technologies Used
- Flutter (Dart)
- Gemini API (Google Generative Language)
- HTTP requests
- Image Picker
- Linkify for clickable links

## How It Works
- Users can type questions or select premade prompts.
- Users can upload outfit images for analysis.
- The app sends queries and images to Gemini API for natural language responses.
- Responses include actionable tips, color matches, and shopping links.

## API Key Security
**Important:**
- The Gemini API key is currently hardcoded in `main.dart` for development.
- **Do NOT commit your API key to public repositories.**
- For production, use environment variables or secure storage to load the API key at runtime. Example approaches:
  - Use a `.env` file and the `flutter_dotenv` package.
  - Store the key in a secure backend and fetch it at app startup.
  - Use platform-specific secure storage (Android/iOS Keychain).

## Getting Started
1. Clone the repository.
2. Add your Gemini API key securely (see above).
3. Run `flutter pub get` to install dependencies.
4. Run the app with `flutter run`.

## File Structure
- `lib/main.dart`: Main app logic and UI
- `android/`: Android platform files
- `pubspec.yaml`: Dependencies
- `README.md`: Project documentation

## Contributing
Pull requests are welcome! Please ensure API keys are never exposed in commits.

## License
MIT
