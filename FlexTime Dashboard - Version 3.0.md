Readme: FlexTime Dashboard - Version 3.0
This document outlines the major updates, new features, and bug fixes in the latest version of the FlexTime Dashboard, comparing it to the original "FlexTime - Dashboard Centered" version.

Introduction
The FlexTime Dashboard has been completely overhauled and optimized to provide a more robust, user-friendly, and performant experience. The new version moves away from a simple, one-page calculator to a full-featured personal dashboard, complete with data tracking, visualization, and a modern user interface.

New Features
1. A Comprehensive Dashboard Experience
Persistent User Profile: The application now remembers your name and settings, greeting you by name on every visit. The name is only requested on the very first launch or after a data reset.

Visual Insights: Two new charts, powered by Chart.js, have been integrated to give you a clear overview of your time-tracking data.

Recent Hours Distribution (Pie Chart): Visualizes the hours worked over the last 7 days.

Overtime Balance Trend (Line Chart): Tracks your cumulative overtime balance over time, providing a clear trend line.

Data Logging & History: The calculator now logs your daily hours to the browser's local storage.

A new "View Log History" button allows you to see all your past entries.

You can now edit or delete individual log entries directly from the history view.

Key Performance Indicators (KPIs): The dashboard features a new stats panel with three key metrics:

Today's Hours

This Week's Average Hours

Total Overtime Balance

Dark Mode: A dedicated theme toggle button has been added, allowing you to switch between a light and dark theme. The application remembers your preference for future visits.

2. Enhanced User Experience (UX)
Intuitive Interface: The layout has been redesigned from a centered, card-based model to a clean, modern sidebar-and-main-content structure, providing better navigation and visual hierarchy.

One-Time Setup: The user is only prompted for their name once. Subsequent visits show the dashboard immediately, leading to faster access.

Improved Calculator: The "FlexTime Calculator" modal is more explicit and includes a date picker, allowing you to log hours for any day, not just the current one.

Instant Feedback: The overtime balance now changes color (green for positive, red for negative) to provide immediate visual feedback on your status.

Responsive Design: The new layout is fully responsive and adjusts gracefully on different screen sizes, from desktop to mobile.

Bug Fixes and Improvements
Compared to the previous version, the new code addresses several key bugs and introduces significant optimizations.

Fixed Data Handling: The original code had a bug where the calculateHours function didn't have a clear way to save or track historical data. The new version implements a robust logging system that stores data in localStorage, preventing data loss on page refresh.

Weather Widget Stability: The weather API call has been reverted to the more reliable wttr.in service for a fixed location (Bruchsal). This avoids the CORS proxy issues and geolocation permissions that were a potential point of failure. The implementation is also more resilient, handling network errors gracefully.

Improved Calculation Logic: The Flex Mode calculation in the original code had an issue with its hard-coded values (8.75h for a full day off). The new version's calculation is more modular and correctly determines the leave time based on a standard 8-hour day and 45-minute pause.

DOM Manipulation Optimization: The new code uses a single DOMContentLoaded event listener and caches DOM elements. This avoids repeated, expensive lookups, resulting in better runtime performance and a smoother user interface.

Clean Codebase: The JavaScript code is now structured into logical sections with clear functions and comments, making it more maintainable and easier to read. It also leverages modern features like async/await and requestAnimationFrame for better performance.

Consistent Styling: CSS variables are now used for all colors, ensuring a consistent theme that's easy to change and supports a seamless transition between light and dark modes.
