# 📰 NewsApp

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?logo=flutter&logoColor=white)](https://flutter.dev) [![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?logo=dart&logoColor=white)](https://dart.dev) ![Platforms](https://img.shields.io/badge/Platforms-Android%20|%20iOS%20|%20Web%20|%20Windows%20|%20macOS%20|%20Linux-informational)

A cross‑platform Flutter app to browse breaking and category‑based news, with a smooth carousel, image caching, and in‑app article viewing. Built with clean widgets and lightweight services. ✨

### ✨ Features
- 🚀 **Landing experience**: Simple onboarding with a clean call‑to‑action.
- 🗞️ **Breaking news carousel**: Auto‑playing image slider with pager indicator.
- 📈 **Trending list**: Fast, scrollable list with cached images.
- 🏷️ **Category browsing**: Business, Entertainment, General, Health, Sports.
- 🌐 **In‑app reader**: Opens articles via `webview_flutter`.
- ⚡ **Performance**: `cached_network_image` and shimmer placeholders.

### 🧰 Tech Stack
- **Flutter** (Material 3)
- **HTTP** for REST calls
- **cached_network_image**, **carousel_slider**, **smooth_page_indicator**, **webview_flutter**, **shimmer**

### 📦 Dependencies (from `pubspec.yaml`)
- `http`
- `cached_network_image`
- `carousel_slider`
- `smooth_page_indicator`
- `webview_flutter`
- `shimmer`

---

## 🚀 Getting Started

### Prerequisites
- Flutter SDK 3.x and Dart 3.x installed
- NewsAPI.org API key (free tier works for development)

### Clone and run
```bash
git clone https://github.com/<your-username>/newsapp.git
cd newsapp
flutter pub get
flutter run
```

### ⚙️ Configure your API key
This project uses the NewsAPI.org endpoints. Replace the inline `apiKey` query parameter in these files with your own key:

- `lib/services/news.dart`
- `lib/services/slider_data.dart`
- `lib/services/show_category_news.dart`

Example (replace the value after `apiKey=`):
```text
https://newsapi.org/v2/top-headlines?...&apiKey=YOUR_API_KEY
```

Tip: For a cleaner setup, you can extract the key into a constant (e.g., `lib/secrets.dart`) and interpolate it in the URLs.

### 🧪 Run on specific platforms
- Android: `flutter run -d android`
- iOS: `flutter run -d ios` (requires Xcode/macOS)
- Web: `flutter run -d chrome`
- Windows/macOS/Linux: `flutter run -d windows` (or `macos`/`linux`)

### 🏗️ Build
- Android APK: `flutter build apk --release`
- iOS: `flutter build ios --release`
- Web: `flutter build web`

---

## 🗂️ Project Structure
```text
lib/
  main.dart                 # App entry; sets up MaterialApp and routes
  pages/                    # UI screens (landing, home, category, details)
  services/                 # Network calls to NewsAPI (breaking, sliders, categories)
  models/                   # Data models (articles, sliders, categories)
  images/                   # Local assets (category thumbnails)
```

## 🧭 App Flow
1. Landing page ➜ "Get Started"
2. Home page shows:
   - Horizontal category chips (local images)
   - Breaking news carousel with pager dots
   - Trending articles list
3. Tap any item ➜ opens full article in an in‑app WebView

---

## 🔐 Notes on API usage
- Respect NewsAPI.org rate limits and terms.
- Avoid committing real API keys. Prefer local config or CI secrets for production builds.

## 🤝 Contributing
Pull requests are welcome! If you have ideas for features or UI improvements, open an issue first to discuss what you’d like to change. 💡

## 🙏 Acknowledgements
- Data powered by NewsAPI.org
- Flutter community packages listed above

## 📄 License
No license has been explicitly set. Consider adding one (MIT is a common choice) if you intend to share or distribute this project.

---

Made with ❤️ using Flutter.
