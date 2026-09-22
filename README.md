# DaVinci Resolve Master Academy — Student Assessment Prototype

Interactive DaVinci Resolve learning and assessment prototype created by Joe Nasr for students.

Live prototype:
https://joenasriani.github.io/davinciresolve/

## What it does

The application organizes DaVinci Resolve training into four learning tracks:

- Edit
- Color
- Fairlight
- Fusion

Each track combines:

- concise instructional content
- a simplified mental model for the topic
- a 10-question knowledge check
- score tracking
- pass/fail logic
- sequential module unlocking

A score of 8/10 or higher is required to progress to the next section.

## Implementation

The application is built as a single-page browser prototype using:

- React 18 loaded through CDN
- ReactDOM
- Babel Standalone for in-browser JSX
- Tailwind CSS via CDN
- Lucide icons
- Canvas Confetti
- JavaScript application state with React hooks

The entire application is contained in a static `index.html` file and requires no backend or build process.

## Application state

React state tracks:

- active learning track
- active module
- current question
- selected answer
- score
- module completion
- unlocked modules
- overall academy completion
- responsive menu state

Progression logic prevents later tracks from opening until the required previous assessment has been passed.

## Assessment model

Each current module contains 10 multiple-choice questions.

Answers are evaluated client-side and the running score is stored in component state.

The module passes when:

`score >= 8`

Successful completion unlocks the next learning track.

## Purpose

This prototype explores how instructor-led DaVinci Resolve material can be converted into a compact browser-based learning path with assessment, progression, and immediate feedback.

Created by Joe Nasr.

https://joe-nasr-signals.vercel.app/
