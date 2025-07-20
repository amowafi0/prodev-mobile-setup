# Mobile Development Setup - Expo Router Project

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app) using the latest Expo Router template.

## Project Scaffolding Process

### 1. Project Initialization
The project was initialized using the Expo Router template:
```bash
npx create-expo-app@latest prodev-mobile-app-0x00
```

### 2. Initial Project Structure
The template created a comprehensive starter app with the following structure:
- **app/**: File-based routing directory using Expo Router
  - **(tabs)/**: Tab-based navigation structure
    - `index.tsx`: Home screen with welcome message
    - `explore.tsx`: Explore screen
  - `_layout.tsx`: Root layout configuration
- **components/**: Reusable UI components
- **constants/**: App constants and theme definitions
- **hooks/**: Custom React hooks
- **assets/**: Images, fonts, and other static assets
- **scripts/**: Utility scripts including reset-project.js

### 3. Home Screen Modification
The default welcome text in `app/(tabs)/index.tsx` was successfully changed from "Welcome!" to "** First App Created**" as requested.

### 4. Development Server
To start the development server:
```bash
npx expo start
```

This provides options to:
- Open in development build
- Run on Android emulator
- Run on iOS simulator
- Use Expo Go app for testing

### 5. Project Reset Process

#### What the `npm run reset-project` command does:

The reset script performs the following operations:

1. **User Prompt**: Asks whether to move existing files to `/app-example` or delete them
2. **Directory Management**: 
   - Moves or deletes the following directories: `app`, `components`, `hooks`, `constants`, `scripts`
   - Creates a new `/app-example` directory (if user chooses to preserve files)
3. **Fresh Start**: Creates a new minimal `/app` directory with:
   - `index.tsx`: Simple screen with basic React Native components
   - `_layout.tsx`: Basic Expo Router stack layout

#### Observations from Running Reset:

**Before Reset:**
- Complex tab-based navigation structure
- Multiple custom components (HelloWave, ParallaxScrollView, ThemedText, etc.)
- Comprehensive styling and theming system
- Multiple screens and navigation tabs

**After Reset:**
- Minimal app structure with just two files
- Simple stack-based navigation
- Basic React Native components (View, Text)
- Clean slate for custom development

#### File Structure Changes:

**Original Structure (moved to app-example):**
```
app/
├── (tabs)/
│   ├── _layout.tsx
│   ├── index.tsx (with "** First App Created**" text)
│   └── explore.tsx
├── _layout.tsx
└── +not-found.tsx
components/
├── Collapsible.tsx
├── ExternalLink.tsx
├── HapticTab.tsx
├── HelloWave.tsx
├── ParallaxScrollView.tsx
├── ThemedText.tsx
├── ThemedView.tsx
└── ui/
constants/
├── Colors.ts
hooks/
├── useColorScheme.ts
├── useColorScheme.web.ts
└── useThemeColor.ts
scripts/
└── reset-project.js
```

**New Structure (after reset):**
```
app/
├── index.tsx (minimal screen)
└── _layout.tsx (basic stack layout)
app-example/
├── app/ (original complex structure)
├── components/ (all original components)
├── constants/ (original constants)
├── hooks/ (original hooks)
└── scripts/ (including reset-project.js)
```

## Development Workflow

1. **Start Development**: Run `npx expo start` to begin development
2. **Edit Files**: Modify files in the `app/` directory to see changes
3. **Test on Devices**: Use Expo Go app or simulators to test your app
4. **Reference Original**: Check `app-example/` directory for reference to the original template structure

## Key Features of Expo Router

- **File-based Routing**: Create routes by adding files to the `app/` directory
- **Type Safety**: Full TypeScript support
- **Universal Apps**: Run on iOS, Android, and Web
- **Hot Reloading**: Instant updates during development
- **Built-in Navigation**: Automatic navigation handling

## Next Steps

1. Start the development server: `npx expo start`
2. Edit `app/index.tsx` to customize your main screen
3. Add new screens by creating files in the `app/` directory
4. Reference the `app-example/` directory for component patterns and styling examples
5. Remove the `app-example/` directory when no longer needed

## Learn More

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals and advanced topics
- [Expo Router documentation](https://docs.expo.dev/router/introduction/): File-based routing guide
- [React Native documentation](https://reactnative.dev/): Core React Native concepts
