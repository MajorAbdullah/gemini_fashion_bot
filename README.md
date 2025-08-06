# Gemini Fashion Bot

## Overview

Gemini Fashion Bot is a Flutter-based mobile application that acts as a personal fashion assistant. Powered by Google's Gemini API, it provides users with instant, AI-driven fashion advice, outfit analysis, and shopping suggestions through a conversational chat interface. The app is designed to help users make better style choices, discover new trends, and get personalized recommendations based on their questions or uploaded outfit images.

## What Problem Does This Solve?

Fashion advice is often expensive, inaccessible, or generic. Gemini Fashion Bot solves this by:

- Making expert fashion guidance available to everyone, instantly and for free.
- Allowing users to get personalized tips based on their own photos and questions.
- Helping users discover new trends, color palettes, and outfit ideas tailored to their needs.
- Providing actionable shopping links and sustainable fashion suggestions.
- Making fashion advice fun, interactive, and easy to use.

## How Does It Work?

1. **Chat-Based Interface:** Users interact with the bot by typing questions or selecting premade prompts (e.g., "How to style jeans for a night out?").
2. **Image Analysis:** Users can upload photos of their outfits. The app sends these images to the Gemini API for analysis and receives feedback, styling tips, and color recommendations.
3. **AI-Powered Responses:** The Gemini API processes user queries and images, returning natural language advice, shopping links, and relevant emojis.
4. **Premade Prompts:** Quick-access chips let users ask common fashion questions with a single tap.
5. **Shopping Suggestions:** When appropriate, the bot provides links to websites where users can buy recommended items.
6. **Secure API Key Handling:** The Gemini API key is loaded from a local file (`lib/api_keys.dart`) and excluded from version control for security.

## Features

- Modern Flutter UI with responsive design
- Chat interface for fashion Q&A
- Upload and analyze outfit images
- Premade prompt chips for quick questions
- Color palette and body type-specific advice
- Sustainable and seasonal fashion tips
- Shopping links for recommended outfits
- Animated typing indicator for bot responses
- Clickable links in bot messages

## Technologies Used

- Flutter (Dart)
- Gemini API (Google Generative Language)
- HTTP requests
- Image Picker
- Linkify for clickable links

## Getting Started

1. Clone the repository.
2. Add your Gemini API key to `lib/api_keys.dart` (do not commit this file to public repos).
3. Run `flutter pub get` to install dependencies.
4. Start the app with `flutter run`.

## File Structure

- `lib/main.dart`: Main app logic and UI
- `lib/api_keys.dart`: Local API key storage (excluded from GitHub)
- `android/`: Android platform files
- `pubspec.yaml`: Dependencies
- `README.md`: Project documentation

## Security Note

**Never commit your API key to public repositories.**
The app is set up to keep your Gemini API key private by using `.gitignore`.

## Contributing

Pull requests are welcome! Please ensure API keys and other sensitive data are never exposed in commits.

## License

MIT

# gemini_fashion_bot

A new Flutter project.
