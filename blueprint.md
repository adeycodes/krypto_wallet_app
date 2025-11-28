# Blueprint: Crypto Wallet App

## Overview

A Flutter-based crypto wallet application that allows users to track cryptocurrency prices, manage their portfolio, and view market trends in real-time. The app features a modern, intuitive Web3 design, a stunning dark theme with vibrant accents, and is built to be resilient to network issues by fetching live data from the CoinGecko API. It includes an onboarding flow for new users and provides a seamless experience for managing crypto assets.

## Implemented Features

*   **Onboarding Experience:** A two-page onboarding flow introduces users to the app's features, shown only on the first launch using `shared_preferences`.
*   **Modern "Web3" Design:** A complete visual overhaul with a new dark theme, vibrant color palette, and updated component styles for a sleek, modern look and feel.
*   **Redesigned Home Screen:** A completely revamped home screen featuring a portfolio card with an integrated line chart, redesigned action buttons, and a refined asset and activity list.
*   **New Activity Screen:** A new screen dedicated to displaying a list of recent transactions.
*   **State Management:** Uses `flutter_riverpod` for robust and scalable state management.
*   **API Integration:** Fetches coin market data and global market metrics from the CoinGecko public API.
*   **Core Screens:** Includes foundational screens for Home, Markets, Wallet, and Profile.
*   **Basic UI Components:** Implemented basic widgets for displaying coin data, loading states, and errors.
*   **Dependency Management:** `dio` for network requests, `intl` for formatting, `fl_chart` for charts, `lucide_icons` for icons, and `smooth_page_indicator` for the onboarding screen.


## Current Task: UI Revamp & Feature Completion

This sprint focuses on a complete visual overhaul of the application to match the provided high-fidelity designs and to implement all core features required for a complete crypto dashboard experience.

### Plan of Action

1.  **~~Create Onboarding Experience:~~** (Done)
    *   ~~Implement a two-page onboarding flow to introduce users to the app's features.~~
    *   ~~Utilize a `PageView` and `smooth_page_indicator` for a clean, swipeable interface.~~
    *   ~~Add navigation controls: "Next", "Get Started", "Skip", and "Sign In".~~
    *   ~~Use `shared_preferences` to show onboarding only on the first launch.~~

2.  **~~Add Core Dependencies:~~** (Done)
    *   ~~`fl_chart`: For rendering dynamic line charts on the Home and Coin Details screens.~~
    *   ~~`smooth_page_indicator`: For the dot indicator on the onboarding screen.~~
    *   ~~`shared_preferences`: For persisting local user data like the onboarding status.~~
    *   ~~`lucide_icons`: For a fresh icon set.~~

3.  **~~Update Core Theming & Styles:~~** (Done)
    *   ~~Revise `app_colors.dart` to establish the new dark theme palette, including dark gradients and vibrant cyan/purple accents.~~
    *   ~~Update text styles and component themes (`ElevatedButton`, `AppBar`, etc.) to align with the modern Web3 aesthetic.~~

4.  **~~Revamp Home Screen:~~** (Done)
    *   ~~Rebuild the `HomePage` UI to match the new design.~~
    *   ~~Integrate a `LineChart` into the "Total Portfolio Value" card to visualize portfolio trends.~~
    *   ~~Style the primary action buttons: `Send`, `Receive`, `Buy`, `Swap`.~~
    *   ~~Restyle the "My Assets" and "Recent Activity" list items for a cleaner look.~~
    *   ~~Update the main bottom navigation bar to include a new "Activity" tab.~~

5.  **Revamp Markets Screen:**
    *   Reconstruct the `MarketsScreen` UI.
    *   Build the new market statistics card displaying Market Cap, 24h Volume, etc.
    *   Restyle the filter chips (`All`, `Favorites`, `Gainers`, `Losers`).
    *   Redesign the `CoinCard` widget to match the new, more detailed list item style.
    *   Implement the floating refresh button for manual data fetching.

6.  **Create Coin Details Screen:**
    *   Create a new `coin_details_screen.dart`.
    *   Build the screen layout, including a header with the coin's image and favorite/share actions.
    *   Implement a detailed `LineChart` with time-range filters (1H, 24H, 7D, etc.).
    *   Add a "Statistics" section for data points like Market Cap, Volume, and All-Time High.
    *   Include an "About" section with the coin's description.

7.  **Implement Functional Requirements:**
    *   **Favorites:** Allow users to mark/unmark coins as favorites, with persistence.
    *   **Error/Loading States:** Ensure all screens handle loading, error, and empty data states gracefully with appropriate UI feedback.
    *   **Navigation:** Wire up all navigation paths between the screens.
