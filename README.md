<div align="center">
  <h1>🏠 Mane-Kelsa (ಮನೆ-ಕೆಲಸ)</h1>
  <p><strong>Connecting local hands to local homes.</strong></p>
  
  <p>
    <img src="https://img.shields.io/badge/Version-2.0.0-emerald" alt="Version" />
    <img src="https://img.shields.io/badge/Platform-Web%20%7C%20Android-blue" alt="Platform" />
    <img src="https://img.shields.io/badge/Built%20With-React%20%7C%20Kotlin-orange" alt="Built With" />
  </p>
</div>

---

## 📖 Overview

**Mane-Kelsa** is a hyper-local directory application designed to bridge the gap between domestic workers (cleaners, gardeners, cooks) and households in small towns. It provides a digital platform for workers to showcase their availability and skills, while allowing residents to find reliable help with ease.

### Key Features
- 🌍 **Multilingual Support**: Fully localized in **Kannada**, **Hindi**, and **English**.
- ⚡ **Real-time Status**: Workers can toggle their availability status (Available/Busy) instantly.
- 📞 **Direct Contact**: One-tap calling to connect users with workers immediately.
- 🌓 **Dark Mode**: Optimized for low-light use and energy saving on mobile devices.
- 📱 **Hybrid Design**: Responsive React web app coupled with a native Android experience.

---

## 🚀 Getting Started (Web)

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher)
- npm or yarn

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/srinivas.git
   cd srinivas
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables:
   Create a `.env.local` file and add your Gemini API key:
   ```env
   GEMINI_API_KEY=your_api_key_here
   ```
4. Run the development server:
   ```bash
   npm run dev
   ```

---

## 🤖 Android Integration

The project includes a native Android component located in the `src/` directory.

### Setup Instructions
1. Follow the [MANE_KELSA_GUIDE.md](./MANE_KELSA_GUIDE.md) for detailed Android Studio setup.
2. Ensure you have a Firebase project set up with the **Realtime Database**.
3. Download and place `google-services.json` in your Android project's `app/` folder.

---

## 🛠 Tech Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS v4, Framer Motion
- **Icons**: Lucide React
- **Android**: Kotlin, Jetpack Compose, Firebase SDK
- **Database**: Firebase Realtime Database
- **AI Integration**: Google Gemini AI (via `@google/genai`)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">
  <p>Built for the local community of Karnataka. ❤️</p>
</div>
