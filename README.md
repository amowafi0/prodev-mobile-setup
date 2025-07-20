# ProDev Mobile Setup - Expo Router Application

This project demonstrates setting up a React Native mobile application using Expo Router template. It includes a complete scaffolding process and reset functionality for development practice.

## 🚀 Project Overview

This is a React Native application built with Expo Framework and Expo Router for navigation. The project demonstrates:

- Expo Router file-based routing
- Tab navigation structure
- Theme support (light/dark mode)
- Component architecture
- Reset functionality for development practice

## 📁 File Structure

```
prodev-mobile-setup/
├── app/                          # Expo Router directory
│   ├── _layout.tsx              # Root layout with navigation setup
│   ├── (tabs)/                  # Tab navigation group
│   │   ├── _layout.tsx          # Tab layout configuration
│   │   ├── index.tsx            # Home screen (Tab One)
│   │   └── two.tsx              # Second tab screen
│   └── modal.tsx                # Modal screen
├── components/                   # Reusable components
│   ├── EditScreenInfo.tsx       # File path display component
│   ├── Themed.tsx               # Themed Text and View components
│   └── useColorScheme.ts        # Color scheme hook
├── constants/                    # App constants
│   └── Colors.tsx               # Color definitions for themes
├── assets/                       # Static assets
├── App.js                        # Original app entry point (restored on reset)
├── package.json                  # Project dependencies and scripts
├── reset-project.js              # Reset functionality script
└── README.md                     # This documentation
```

## 🛠️ Scaffolding Process

### Step 1: Project Initialization
The project was initialized with Expo Router template structure. Since the project already had Expo dependencies, we manually created the file-based routing structure.

### Step 2: Directory Structure Creation
Created the following directory structure for Expo Router:
- `app/` - Main routing directory
- `app/(tabs)/` - Tab navigation group
- `components/` - Reusable components
- `constants/` - App constants

### Step 3: Core Files Created

#### Root Layout (`app/_layout.tsx`)
- Configures the root navigation stack
- Sets up theme provider
- Handles font loading and splash screen
- Defines initial route as `(tabs)`

#### Tab Layout (`app/(tabs)/_layout.tsx`)
- Configures tab navigation
- Sets up tab icons using FontAwesome
- Defines two tabs: "Tab One" and "Tab Two"
- Includes header right button for modal navigation

#### Home Screen (`app/(tabs)/index.tsx`)
- **Modified text**: Changed from "Welcome!" to "** First App Created**"
- Displays file path information
- Uses themed components for consistent styling

#### Second Tab (`app/(tabs)/two.tsx`)
- Simple second tab screen
- Demonstrates tab navigation functionality

#### Modal Screen (`app/modal.tsx`)
- Modal presentation screen
- Accessible via header right button in tab navigation

### Step 4: Component Architecture

#### Themed Components (`components/Themed.tsx`)
- Provides themed `Text` and `View` components
- Supports light/dark mode
- Uses color scheme from constants

#### EditScreenInfo (`components/EditScreenInfo.tsx`)
- Displays current file path
- Shows development instructions
- Demonstrates component reusability

#### useColorScheme Hook (`components/useColorScheme.ts`)
- Provides color scheme detection
- Returns 'light' or 'dark' theme
- Used throughout the app for theme consistency

### Step 5: Constants and Configuration

#### Colors (`constants/Colors.tsx`)
- Defines color palette for light and dark themes
- Includes text, background, tint, and icon colors
- Used by themed components

## 🎯 Key Features Implemented

1. **File-based Routing**: Expo Router automatically creates routes based on file structure
2. **Tab Navigation**: Bottom tab navigation with two tabs
3. **Theme Support**: Light/dark mode with themed components
4. **Modal Navigation**: Modal screen accessible from tab header
5. **Component Architecture**: Reusable, themed components
6. **Reset Functionality**: Complete project reset capability

## 📱 Running the Application

### Prerequisites
- Node.js (version 18 or higher)
- npm or yarn
- Expo CLI (`npm install -g @expo/cli`)
- Expo Go app on your mobile device

### Development Commands
```bash
# Start the development server
npm start
# or
npx expo start

# Platform-specific commands
npm run android    # Android
npm run ios        # iOS
npm run web        # Web
```

### Testing on Device
1. Start the development server: `npm start`
2. Scan the QR code:
   - **iOS**: Use Camera app
   - **Android**: Use Expo Go app
3. The app will load on your device with hot reloading

## 🔄 Reset Functionality

### Reset Command
```bash
npm run reset-project
```

### What Reset Does
The reset functionality performs the following actions:

1. **Removes Expo Router Structure**:
   - Deletes the entire `app/` directory
   - Removes Expo Router-specific components from `components/`
   - Removes `constants/` directory

2. **Restores Original App.js**:
   - Replaces the current App.js with the original welcome screen
   - Removes all Expo Router dependencies
   - Returns to the basic Expo setup

3. **Clean State**:
   - Removes all tab navigation
   - Removes themed components
   - Removes modal functionality
   - Returns to single-screen application

### Reset Observations
When running `npm run reset-project`:

1. **Console Output**: Shows progress of file and directory removal
2. **File System Changes**: 
   - `app/` directory is completely removed
   - `components/` directory is cleaned of Expo Router files
   - `constants/` directory is removed
   - `App.js` is restored to original state
3. **Application State**: Returns to basic Expo welcome screen
4. **Development Ready**: Project is ready for a fresh start

### Use Cases for Reset
- **Learning**: Practice the setup process multiple times
- **Clean Slate**: Start over with a fresh implementation
- **Testing**: Verify the setup process works correctly
- **Development**: Reset before implementing new features

## 🛠️ Development Notes

### Dependencies
The project includes all necessary Expo Router dependencies:
- `expo-router`: File-based routing
- `@react-navigation/native`: Navigation primitives
- `expo-font`: Font loading
- `expo-splash-screen`: Splash screen management
- `@expo/vector-icons`: Icon library

### TypeScript Support
The project is configured with TypeScript for better development experience:
- Type definitions for React Native
- Type-safe component props
- Better IDE support and error detection

### Hot Reloading
The development server supports hot reloading:
- Changes are reflected immediately on device
- No need to restart the development server
- Fast development iteration

## 📚 Learning Resources

- [Expo Router Documentation](https://docs.expo.dev/router/introduction/)
- [React Navigation](https://reactnavigation.org/)
- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/)

## 🎉 Next Steps

After completing this setup:

1. **Explore the Code**: Review the file structure and component architecture
2. **Modify Components**: Try changing text, styles, and functionality
3. **Add Features**: Implement new screens, components, or functionality
4. **Practice Reset**: Use the reset functionality to practice the setup process
5. **Build Your App**: Use this as a foundation for your own mobile application

---

**Note**: This project demonstrates the complete Expo Router setup process and includes a reset functionality for educational purposes. The reset feature allows you to practice the scaffolding process multiple times and understand the file structure of a React Native application using Expo. 
