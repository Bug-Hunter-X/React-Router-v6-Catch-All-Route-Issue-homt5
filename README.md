# React Router v6 Catch-All Route Unexpected Behavior

This repository demonstrates an uncommon issue encountered with the catch-all route ("*") in React Router v6.  The problem occurs when navigating between defined routes; the catch-all route is unexpectedly activated even though a specific route should be handling the navigation.

## Issue Description

The issue occurs when you have other defined routes in your application, and one of these other routes successfully matches the requested URL path. Even in this case, the catch-all route will be rendered.  This prevents the expected route from being displayed, leading to unexpected application behavior.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Navigate between the Home and About pages.  Notice the unexpected behavior of the 404 page.

## Solution

The solution involves carefully considering the order of routes within your React Router configuration. By ensuring that the catch-all route is the last route in your `Routes` component, you can ensure that other routes take precedence.  This prevents the unnecessary triggering of the catch-all route and restores expected behavior.