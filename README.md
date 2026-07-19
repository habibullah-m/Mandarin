# Mandarin

## Overview

I built a mobile-first AI language learning app designed to help users improve their spoken Mandarin through structured lessons and AI-powered conversation practice. The app combines a guided curriculum, listening and speaking exercises, and real-time roleplay conversations to create an immersive learning experience.

Users can sign in using passwordless magic links, complete a personalized onboarding flow, progress through a structured curriculum, and track their speaking and listening activity. Premium users can generate custom AI roleplay scenarios tailored to their learning goals.

**Tech stack:**

* Expo (React Native)
* TypeScript
* Expo Router
* Supabase (Auth, Postgres, Edge Functions)
* OpenRouter
* Expo AV & Speech APIs

**Features:**

* Built a cross-platform mobile app for iOS and Android with Expo
* Implemented passwordless authentication using Supabase magic links
* Created a personalized onboarding flow based on language level, motivation, and interests
* Developed a structured Mandarin curriculum with 12 chapters and 86 lessons
* Added listening and speaking practice with progress tracking
* Integrated voice recording, AI transcription, and pronunciation practice
* Built real-time AI roleplay conversations with scenario-based objectives
* Enabled custom AI-generated learning scenarios
* Tracked speaking/listening time and lesson completion
* Implemented a premium subscription flow with an in-app paywall


## Setup

Follow these steps to install and set up the project.

### Clone the Repository

```bash
git clone https://github.com/habibullah-m/Mandarin
cd Mandarin
```

### Prerequisites

- Node.js
- npm or pnpm
- Supabase CLI

Install Supabase CLI:

```bash
npm install supabase --save-dev
```

### Environment Variables

Create a `.env` file in the root:

```bash
EXPO_PUBLIC_SUPABASE_URL=your_supabase_project_url
EXPO_PUBLIC_SUPABASE_KEY=your_supabase_anon_key
```

### Supabase Setup

Login and link your project:

```bash
npx supabase login
npx supabase link --project-ref YOUR_PROJECT_REF
```

Apply database migrations:

```bash
npx supabase db push
```

Deploy Edge Functions:

```bash
npx supabase functions deploy chat-completion
npx supabase functions deploy transcribe-audio
npx supabase functions deploy scenario-generate
npx supabase functions deploy start-trial
```

Set required function secrets:

```bash
npx supabase secrets set OPENROUTER_API_KEY=your_openrouter_key
npx supabase secrets set SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
```

### Auth Redirect Setup

Add your app redirect URL in Supabase Auth URL configuration:

```bash
mandarin://
```

### Frontend

Install dependencies:

```bash
npm install
```

Run the app:

```bash
npm run start
```

Run on iOS simulator:

```bash
npm run ios
```

Run on Android emulator:

```bash
npm run android
```

Run lint:

```bash
npm run lint
```
