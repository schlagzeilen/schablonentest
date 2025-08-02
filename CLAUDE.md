# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple web application for NFC product scanning and testing. The project consists of a single HTML file (`nfc-scanner.html`) that implements a complete NFC-based product testing workflow.

## Architecture

**Single-Page Application**: The entire application is contained in `nfc-scanner.html` with embedded CSS and JavaScript. No build process or external dependencies are required.

**Core Functionality**:
- NFC scanning using the Web NFC API (`NDEFReader`)
- Product serial number extraction from NFC tags
- Test result recording (Pass/Fail)
- CSV export functionality for test results
- Local storage of scanned products in browser memory

**Key Components**:
- NFC scanning interface with permission handling
- Product list management with duplicate detection
- Test result prompt system
- CSV export with timestamp data

## Development Commands

This project requires no build, test, or lint commands as it's a standalone HTML file. To develop:

1. Open `nfc-scanner.html` directly in a web browser
2. For NFC functionality, serve over HTTPS (required for Web NFC API)
3. Test on NFC-capable devices (primarily Android phones with Chrome)

## Testing

No automated test framework is configured. Testing should be done manually:
- Test NFC scanning with physical NFC tags
- Verify CSV export functionality
- Test duplicate product detection
- Validate UI responsiveness on mobile devices

## Browser Compatibility

- Requires browsers with Web NFC API support (primarily Chrome on Android)
- HTTPS is required for NFC functionality
- Modern JavaScript features used (async/await, template literals)