<div align="center">

<img src="assets/textsentry-icon.svg" alt="TextSentry logo" width="140" />

# TextSentry

**AI-powered protection against unwanted text messages.**

[Android app](https://github.com/TextSentry/text-sentry-android) · [Website](https://github.com/TextSentry/text-sentry-web) · [Infrastructure](https://github.com/TextSentry/text-sentry-iac)

</div>

## Overview

TextSentry is an Android app designed to help you take control of unwanted SMS messages. It uses AI to evaluate incoming texts and decide whether they fit the categories you want to filter, such as political campaigns, voting outreach, and marketing advertisements.

When an incoming message matches your preferences with sufficient confidence, TextSentry can automatically respond. Optionally, it can delete handled messages and keep a history of its actions.

## Features

- **AI-powered message classification** — Evaluate messages based on their content and configurable instructions, rather than relying on fixed keywords.
- **Customizable categories** — Filter voting-related outreach, political campaign messages, and marketing advertisements. Voting and political categories are enabled by default.
- **Confidence threshold** — Set the minimum classification confidence required to take action.
- **Automatic responses** — Reply to matching messages without requiring manual review of each text.
- **Optional deletion** — Choose whether handled messages are deleted.
- **History and transparency** — Review messages that received replies, model confidence scores, and whether deletion occurred.
- **Simple settings** — Configure your API key, filtering preferences, custom instructions, and confidence threshold.

## How it works

1. The Android app receives an incoming SMS (subject to Android permissions and platform restrictions).
2. TextSentry sends the message content and configured filtering instructions to its AI service for evaluation.
3. The response is evaluated against your enabled categories and confidence threshold.
4. For matching messages, the app can send a response and optionally delete the message.
5. The result is recorded in the app's history.

TextSentry's behavior depends on its configuration, granted Android permissions, and availability of the AI service. Automated classification can make mistakes.

## Project repositories

| Repository | Purpose |
| --- | --- |
| [text-sentry-android](https://github.com/TextSentry/text-sentry-android) | Android application, filtering, settings, message handling, and history |
| [text-sentry-web](https://github.com/TextSentry/text-sentry-web) | Public website |
| [text-sentry-iac](https://github.com/TextSentry/text-sentry-iac) | AWS infrastructure as code, including hosting, API, identity, and deployment resources |
| **test-sentry** (this repository) | Project overview, documentation, and shared branding |

## Configuration

The Android app uses the TextSentry AI service and its current model by default. Users can configure an API key, categories, additional classification instructions, confidence threshold, and optional message deletion in the app's settings.

For build and deployment details, see the README and workflows in each component repository. **Do not commit API keys, credentials, or other secrets.**

## Privacy and permissions

TextSentry processes SMS content to classify messages. Depending on how the service and app are configured, message content may be transmitted to the AI backend. Only grant the app permissions you understand and need, and review the applicable privacy disclosures before using it.

Android restricts SMS access, sending, and deletion. Certain functions may require the app to be set as the default SMS handler or may be subject to device and distribution policies.

## Status

TextSentry is under active development. Features, behavior, and availability may change.

## Branding

The project icon is available at [assets/textsentry-icon.svg](assets/textsentry-icon.svg). Its shield represents protection, while the speech bubble and blocked-message mark represent unwanted-text filtering.
