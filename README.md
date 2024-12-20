# Expo Linking.getInitialURL() Inconsistent null return

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` function.  The function inconsistently returns `null` even when the app is launched via a deep link. This makes handling initial URL navigation unreliable.  The `LinkingBug.js` file shows the problematic behavior, and `LinkingBugSolution.js` offers a workaround.

## Problem

The `Linking.getInitialURL()` method is crucial for handling deep links when an app launches.  However, in certain scenarios, it unpredictably returns `null`, leading to unexpected behavior in the application.

## Solution

The provided solution implements a retry mechanism with a timeout.  This approach increases the chances of successfully retrieving the initial URL.