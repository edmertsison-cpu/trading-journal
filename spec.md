# Trading Journal Pro - Specification

## Overview
A locally-stored, PWA-enabled Trading Journal application built with HTML, Tailwind CSS, and Vanilla JavaScript.

## Architecture
- **Frontend:** Single-page HTML application styling via Tailwind CSS CDN.
- **Storage:** HTML5 `localStorage` for all user data (offline first).
- **PWA Capabilities:** `manifest.json` for installation parameters and `sw.js` for caching and offline functionality.

## Features
- **Dashboard:** Tracks initial capital, total current balance, all-time net profit, and net transfers.
- **Calendar View:** Navigable monthly grid displaying daily P&L, trades, deposits, and withdrawals.
- **Monthly Summary:** Aggregates metrics for the currently viewed month.
- **Data Entry Modal:** Input mechanism for daily metrics.
- **Offline Support:** Full PWA offline readiness.
