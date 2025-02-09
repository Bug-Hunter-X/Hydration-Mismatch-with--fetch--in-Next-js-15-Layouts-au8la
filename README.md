# Next.js 15 Hydration Mismatch with `fetch` in Layouts

This repository demonstrates a common issue in Next.js 15 applications involving hydration mismatches when using `fetch` within layouts or dynamically loaded components of the `app` directory.  The problem arises from race conditions between the layout's initial render and asynchronous data fetching.

## Problem

When a layout uses `fetch` to retrieve data, and that data is not available before the initial render, it can lead to a hydration mismatch. This results in a blank screen, unexpected behavior, or error messages in the browser's console.

## Solution

The solution involves using techniques like loading states, fallback content, or suspending rendering until the data has arrived.  The example provided utilizes a loading state to display a message while waiting for data. This improves the user experience and prevents hydration errors.

## Reproduction

1. Clone the repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the initial render and subsequent updates.