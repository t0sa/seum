# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

"Le Décompte du Seum" is a French countdown timer single-page application counting down to April 3, 2026 at 18:00. The project is a standalone HTML file with embedded CSS and JavaScript - no build tools, dependencies, or frameworks.

## Architecture

**Single-File Application**: `index.html` contains the entire application:
- **Inline CSS** (lines 7-215): All styles including animations (float, pulse, shake, tears), gradient backgrounds, and responsive design
- **Inline JavaScript** (lines 255-287): Countdown logic that calculates time remaining and updates DOM every second
- **Static Asset**: `seum.png` - main image displayed with dramatic effects

**Key Technical Details**:
- Target date: April 3, 2026 at 18:00 (hardcoded in line 261)
- Countdown calculation uses `Date.getTime()` with millisecond precision
- Updates via `setInterval(updateCountdown, 1000)`
- Completion condition shows celebration message when `distance < 0`

## Development

**Preview**: Open `index.html` directly in a browser (no server required)

**Testing Changes**:
- Edit `index.html` in any text editor
- Refresh browser to see changes
- No compilation or build step needed

**Structure Conventions**:
- CSS animations use `@keyframes` for float, pulse, shake, tears effects
- Time units formatted with `padStart()` for consistent display (days: 3 digits, others: 2 digits)
- Responsive breakpoint at 768px (media query starting line 189)

## Content Elements

**Text Content** (French language):
- Main heading: "Le Décompte du Seum" (line 224)
- Subtitle: "Temps restant avant la fin..." (line 225)
- Caption: "Moi après le 3 avril 2026... 😭" (line 252)
- Completion message: "C'EST FINI ! LIBERTÉ !" (line 269)

**Visual Elements**:
- Floating emoji backgrounds: 😭 (3 instances with staggered animations)
- Main image: `seum.png` with shake animation and purple border
- Gradient theme: Purple gradient (#667eea to #764ba2)
