# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

HyperLog is a blockchain-powered digital pilot logbook website for hyperlog.aero. The project currently consists of a single-page marketing website (`hyperlog_frontpage.html`) built with vanilla HTML, CSS, and JavaScript.

**Product:** HyperLog - "Trust in Every Entry"
**Company:** HyperLog Ltd (UK-based)
**Domain:** hyperlog.aero

## Architecture

This is a static single-page website with no build tools or dependencies. All styles and scripts are embedded inline in `hyperlog_frontpage.html`.

### Key Files
- `hyperlog_frontpage.html` - The complete website (HTML + inline CSS + inline JS)
- `HYPERLOG_WEBSITE_BRIEF.md` - Product specification and design requirements

### Development
To preview the website, open `hyperlog_frontpage.html` directly in a browser or use any local server:
```bash
python3 -m http.server 8000
```

## Brand Guidelines

### Colors
**Primary (Denim Blue):**
- Main: `#025EB5`
- Light: `#328DD8`
- Lighter: `#7DBEF4`
- Dark: `#00213D`

**Neutrals:**
- Night Rider: `#333333`
- Night Rider Dark: `#242526`
- White Dark: `#D1D2D2`

**Trust Level Indicators:**
- Certified (green): `#10B981`
- Tracked (amber): `#F59E0B`
- Logged (blue): `#3B82F6`

### Typography
- Primary font: Outfit (Google Fonts)
- Monospace: JetBrains Mono (for data/numbers)
- Brand guidelines specify Alexandria font, but the website uses Outfit

### Trust Level System
HyperLog has a three-tier trust classification that is central to the product:
1. **Logged** - Pilot-signed entries (cryptographic signature only)
2. **Tracked** - Corroborated by external data (ADS-B, FlightRadar)
3. **Certified** - Signed by regulatory authorities (CAA, EASA, FAA)

## Technical Context

The website promotes a Flutter mobile app that uses:
- Hyperledger Fabric blockchain (enterprise-grade, no cryptocurrency)
- On-device cryptographic key storage (iOS Keychain / Android Keystore)
- Backend relay for Fabric communication

Target audiences: Pilots, Airlines, Regulators, Flight Schools
