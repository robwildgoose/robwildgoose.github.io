---
title: My Little Voice
status: In Progress
project_type: Personal app
summary: A free, offline-first AAC app for my daughter and other children who need a communication tool.
platforms:
  - iOS
  - Android
tech:
  - .NET MAUI
  - Accessibility
  - AAC
  - SQLite
  - OpenMoji
  - Mulberry Symbols
  - ARASAAC
  - C#
order: 9
privacy_url: /privacy/my-little-voice/
---

## Building Little Voice: Creating a Free, Offline-First AAC App for My Daughter

Communication is a foundational right, yet for many children, including those who are nonspeaking, minimally speaking, autistic, or navigating apraxia or speech delays, getting access to reliable Augmentative and Alternative Communication (AAC) tools can be surprisingly difficult.

For me, this project is deeply personal. My own daughter is autistic and non-verbal, and building **Little Voice** has given me a meaningful way to use my skills as a developer to directly support her communication and development. When looking at existing AAC options, I quickly ran into the reality so many families face: dedicated speech devices and leading communication apps often come with steep price tags, ongoing subscriptions, or lengthy processes just to apply for funding and grants. A child shouldn't have to wait on paperwork or budgets just to have a reliable way to express what they want, feel, or need.

**Little Voice** is my answer to that: a free, offline-first, neurodiversity-affirming AAC app built on Android with **.NET MAUI**, designed to turn an everyday phone or tablet into a calm, dependable communication space for my daughter, and for any other family who needs it.

### Designed Around Real Kids and Sensory Comfort

Visual design in an AAC app is not just about appearance. It affects how comfortable and focused a child feels when trying to communicate. Bright, harsh colors and glaring screens can cause visual fatigue or sensory overload.

Little Voice uses a **sensory-friendly, pastel-toned adaptation of the Fitzgerald Key** so word categories stay visually consistent and intuitive without feeling overwhelming:

- **Soft yellows/warm tones** for people and pronouns
- **Calm mint greens** for actions and verbs
- **Gentle peaches/oranges** for nouns and everyday objects
- **Soothing blues** for feelings and descriptors
- **Soft rose/coral tones** for social words and urgent needs

Tiles feature generous spacing, tactile rounded corners, and clear pairings of symbols and high-contrast labels so motor planning stays consistent and both pre-readers and emerging readers have support.

### Open Symbols, 100% Offline, and No Vendor Lock-In

A communication tool shouldn't stop working when you lose Wi-Fi or cellular signal, and a child's vocabulary should never be held hostage inside a proprietary format. Whether we are at home, at school, in the car, or out at the park, Little Voice is built to work locally without needing an internet connection to speak or display boards.

- **Open-Licensed Symbol Packs:** Little Voice uses open-licensed symbol libraries, specifically **Mulberry Symbols**, **ARASAAC**, and **OpenMoji**, packaged cleanly with simple JSON manifests and stored locally in **SQLite**. Families can download lightweight, modular packs, including high-interest topics like dinosaurs with fun sound effects, without bloating the app or worrying about third-party tracking.
- **Easy Export & Portability:** One of the biggest frustrations with expensive AAC ecosystems is how hard it can be to export your child's custom cards and boards once you've spent months building them. Little Voice is designed around open files and straightforward exporting so parents always own their boards, images, and audio, making it simple to back up, share, or move away from locked-in systems whenever they choose.
- **Local Speech & Familiar Voices:** Powered by **Sherpa-ONNX** for local, offline text-to-speech, Little Voice also supports mixing in real recorded audio, meaning a tile for *Mom*, *Dad*, or a favorite routine can play a familiar voice from home.

### Turning a Regular Tablet Into a Dedicated Voice

One of the biggest practical hurdles for families using a standard Android device for AAC is accidental exits, swiping out of the app, hitting a system button, or getting pulled into notifications.

Little Voice leans into **Android Screen Pinning (App Pinning)** alongside a parent-protected edit mode so caregivers can keep the communication board front and center when needed, while still making it straightforward to customize grids, add personal photos or audio, and step back in as a parent. Alongside the communication board itself, a **Parent Companion** section is planned to share plain-English, research-informed ideas like modeling and giving wait time in everyday routines.

### Why I'm Building It This Way

At its core, My Little Voice started with a simple goal: as a dad, I wanted to remove the barriers between my daughter having a thought and being able to share it, without expensive paywalls, subscriptions, proprietary lock-in, or waiting on grants getting in the way. By combining .NET MAUI, local SQLite storage, offline neural speech, open symbol libraries, and sensory-conscious design, my hope is to build a communication tool that supports her growth every day and helps other families along the way.
