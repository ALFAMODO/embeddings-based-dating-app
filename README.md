# About

AI-powered dating app built with Expo, React Native, Clerk, Convex, and OpenAI. It includes authentication, profile onboarding, swipe-based discovery, AI-assisted daily picks, real-time matches, and chat.

## Features

- Email sign in and sign up with Clerk
- Protected app routes with Expo Router
- Multi-step onboarding for name, birthday, gender, photos, location, bio, interests, age range, and dating preferences
- Swipe-style profile discovery with like and reject actions
- Mutual matches stored in Convex
- AI daily picks with compatibility explanations
- Real-time chat for matched users
- Profile editing and photo management
- Location and distance-based matching support
- Haptics, animated cards, glass UI components, and light/dark theme support

## Tech Stack

- Expo SDK 55
- React Native 0.83
- React 19
- Expo Router
- TypeScript
- Clerk for authentication
- Convex for database, backend functions, real-time subscriptions, and vector search
- OpenAI for profile embeddings and AI match explanations
- React Native Reanimated for animations
- pnpm for package management

## Project Structure

```text
app/                  Expo Router screens and route groups
components/           Reusable UI, auth, profile, chat, match, and onboarding components
convex/               Convex schema, queries, mutations, actions, and generated types
hooks/                Shared React hooks
lib/                  Theme, auth, location, haptics, constants, and utility code
providers/            Clerk, Convex, and theme providers
assets/               App icons, splash image, and static images
```

## Requirements

- Node.js
- pnpm
- Expo CLI
- Clerk account
- Convex account
- OpenAI API key
- iOS Simulator, Android Emulator, or a physical device with a development build

## Setup

Install dependencies:

```bash
pnpm install
```

Create a `.env.local` file in the project root:

```bash
EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_xxxxx
EXPO_PUBLIC_CONVEX_URL=https://your-deployment.convex.cloud
```

Start Convex:

```bash
npx convex dev
```

Add the OpenAI key in the Convex dashboard:

```text
OPENAI_API_KEY=sk-xxxxx
```

Start the Expo app:

```bash
pnpm start
```

## Scripts

```bash
pnpm start      # Start Expo
pnpm ios        # Run iOS development build
pnpm android    # Run Android development build
pnpm web        # Start web build
pnpm lint       # Run Expo lint
```

## Demo Data

Demo profile data is included under `convex/sampleData`. To seed demo profiles, run the seed function from the Convex dashboard or Convex CLI after your deployment is configured.

## Environment Notes

- `EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY` is used by the mobile app for Clerk.
- `EXPO_PUBLIC_CONVEX_URL` connects the app to your Convex deployment.
- `OPENAI_API_KEY` should be stored in Convex environment variables, not in `.env.local`.
- Do not commit local environment files or private API keys.

## License

See `LICENSE.md`.
