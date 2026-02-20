# InnerHue Frontend Redesign — Apertre 3.0

## Project Overview

InnerHue is a mental health journaling platform designed to help users track emotional states, reflect on patterns, and engage with therapeutic tools such as soundscapes and guided prompts. The Apertre 3.0 initiative involved a comprehensive frontend redesign to improve emotional safety, visual consistency, and user engagement across the application.

## Problem Statement

The existing interface exhibited strong indicators of AI-generated UI patterns, including:

* Inconsistent theming across pages
* Low text visibility in emotional selection components
* Generic gradient-heavy layouts
* Disconnected visual hierarchy between Landing, Music, and Analytics pages
* Repetitive grid-based feature sections ("How it Works")

This resulted in a dashboard-like interaction model that conflicted with the reflective nature of a mental health journaling platform.

## My Role

Frontend Developer — UI Systems Refactor

* Led visual system unification across all primary pages
* Redesigned the Music module interaction model
* Standardized shared UI components
* Fixed accessibility and visibility issues in emotion logging
* Implemented consistent elevation and surface styling

## Design Approach

### 1. Global Theme Unification

* Migrated all pages to a unified dark base: `#0f0720`
* Standardized text hierarchy using `text-white`, `text-white/70`, and `text-white/60`
* Introduced a consistent glassmorphism layer:

  * Surfaces: `bg-white/5` to `bg-white/20`
  * Borders: `border-white/10`
  * Backdrop blur: `backdrop-blur-lg`

### 2. Component-Level Refactors

* **MoodCapsule**: Resolved invisible text caused by dark-on-dark contrast

  * calm → `bg-green-500/20 text-green-200`
  * stress → `bg-orange-500/20 text-orange-200`
  * hopeful → `bg-purple-500/20 text-purple-200`
  * neutral → `bg-white/10 text-white/80`
  * Added selected states with ring borders and higher opacity

* **SoftCard**: Migrated from light journal styling to dark glass surfaces

  * `bg-white/10 backdrop-blur-lg border-white/10`

* **BentoDashboard**: Applied vibrant accent tokens on dark surfaces for status cards

* **SuggestionPanel**: Converted from opaque light cards to translucent dark surfaces

* **OrbVisualizer**: Updated container and text styles to align with dark system

### 3. Music Page Redesign (Major)

Rebuilt the Sonic Sanctuary module to improve immersion:

* Featured player with large album-art surface (320px/256px)
* Ambient background glow matching active track
* Animated visualizer bars on album art (16 bars)
* Color-coded themes per track (Rain, Forest, Ocean, Meditation)
* Progress bar animation and large circular play control (64px)
* Vertical track list with active glow states
* Mini visualizers for playing indicators

## Implementation

* **Framework**: React / Next.js
* **Styling**: Tailwind CSS
* **Animation**: Framer Motion
* **Design System**: Custom dark glassmorphism tokens

## Key Improvements

* Visual consistency across 9 page components
* Standardized shared UI across 5 core components
* Fixed mood capsule accessibility issues
* Introduced immersive music player experience
* Unified elevation, spacing, and typography

## Outcome

* Improved readability and emotional logging usability
* Consistent tactile depth across Landing, Music, and Analytics
* Reduced visual fragmentation between modules
* Enhanced interaction feedback via hover and motion states

## Scope of Changes

* Files modified: 15
* Page components updated: 9
* Shared components updated: 5
* Global style additions: 1
* Major redesigns: 1 (Music Module)
* Critical fixes: 1 (MoodCapsule visibility)

## Links

* Repository: <add repo link>
* Pull Request: <add PR link>
* Screenshots (Before / After): <add images>

---

*This case study summarizes the frontend system refactor undertaken as part of Apertre 3.0 for InnerHue.*
