# Enumberator — Number Learning App for Young Children

## Overview

A single-page web app that helps 4-year-olds learn numbers 1-20 through interactive mini-games. Designed around developmental research for preschool-age children.

## Design Principles

### Pedagogy (Research-Backed)
- **Subitizing first:** Recognizing small quantities (1-4) without counting is a foundational skill
- **Concrete before abstract:** Always pair numerals with visual quantities (objects, dots)
- **Multi-sensory:** Visual + auditory reinforcement (see the number, hear it spoken, count objects)
- **Scaffolded difficulty:** Progress from recognition → counting → ordering → simple arithmetic
- **Errorful learning:** Mistakes are expected and gently corrected with hints, never punished

### Reward Without Addiction
- Intrinsic motivation over extrinsic: animations are part of the experience, not gated rewards
- No streaks, scores, leaderboards, or daily login incentives
- Gentle encouragement on mistakes ("Not quite! Try again!")
- Natural session ending: 8-10 rounds, then a "You did great!" closing screen
- No "play again" pressure loop — closing screen has a calm, finished feeling
- Celebration of effort (completing the session), not perfection

### UX for 4-Year-Olds
- Large, colorful touch targets (minimum 64px, ideally 80px+)
- Works on tablets (primary device for this age group)
- Simple interactions: tap/click only (no drag-and-drop for youngest levels)
- Friendly animal/character theme
- Fun sound effects and animations on every interaction
- Clear visual feedback for correct/incorrect answers
- No text instructions — use audio prompts and visual cues

## Game Modes

### Mode 1: "Count the Animals"
- Animals appear on screen (frogs, cats, dogs, butterflies, etc.)
- Child taps each animal to count it (animal wiggles and makes a sound, counter increments)
- After counting, child picks the correct number from 2-3 choices
- Builds: counting, one-to-one correspondence, number recognition

### Mode 2: "Bubble Pop"
- Bubbles float up with numbers written inside them
- A voice/text prompt says "Find the [N]!"
- Child taps the correct bubble — it pops with a satisfying animation
- Wrong bubbles wobble but don't pop
- Builds: numeral recognition, listening comprehension

### Combined Flow
A session alternates between the two modes for variety:
1. Round 1-2: Count the Animals
2. Round 3-4: Bubble Pop
3. Round 5-6: Count the Animals
4. Round 7-8: Bubble Pop
5. Closing celebration screen

## Difficulty Levels

| Level | Name             | Number Range | Choices | Skills                              |
|-------|------------------|-------------|---------|--------------------------------------|
| 1     | Little Counter   | 1-5         | 2       | Subitizing, counting, recognition    |
| 2     | Number Explorer  | 1-10        | 3       | Recognition, counting larger sets    |
| 3     | Number Champion  | 1-20        | 4       | Full range recognition and counting  |
| 4     | Math Starter     | 1-10        | 3       | Simple addition/subtraction visuals  |

### Level 4 (Math Starter) Details
- "Count the Animals" becomes: "3 frogs are here. 2 more hop in! How many now?"
- "Bubble Pop" becomes: "Pop the bubble that shows 2 + 1!"
- Always uses concrete visuals — never abstract equations alone

## Technical Approach

- **Single HTML file** with embedded CSS and JavaScript
- **No dependencies** — vanilla JS, CSS animations, Web Audio API
- **Responsive design** — works on phones, tablets, and desktops
- **Web Audio API** for sound effects (pops, dings, animal sounds)
- **CSS animations** for wiggle, bounce, float, confetti effects
- **Emoji-based** animal characters (no image assets needed)

## Color Palette
- Warm, friendly, high-contrast colors
- Pastel background, bold saturated colors for interactive elements
- Distinct colors for correct (green) vs incorrect (gentle orange, not red) feedback

## File Structure
```
index.html    — the entire app (single file)
DESIGN.md     — this document
```
