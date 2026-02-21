# intentional-framing

Evaluates the intentional framing of a cat photograph — whether the composition feels deliberate and positions the cat as the natural focal point of the image.

## Overview

Not every photograph of a cat is a cat photograph. The difference lies in whether the frame exists in service of the cat. The `intentional-framing` function scores how deliberate and effective a photograph's composition feels by examining whether the cat is positioned within the frame in a way that naturally draws the viewer's eye, and whether the spatial arrangement of elements serves the cat as the clear subject.

This evaluation is not about enforcing rigid compositional rules like the rule of thirds. A cat sitting dead center in a simple frame can score beautifully. A cat caught along a dynamic diagonal can score just as well. What matters is whether the framing feels like it was made for this cat in this moment — whether the viewer senses that the image was composed around its subject.

Strong intentional framing means the spatial relationship between the cat and its surrounding space serves the subject — the cat is given room to breathe but is not dwarfed by its environment, and the composition works with the subject rather than against it. Weak framing makes the cat feel like an afterthought — the background dominates, the cat is marginal, or the crop disrupts the viewer's ability to appreciate the subject.

## Input

The function receives a single input: a **cat photograph** (image). The image is evaluated purely on its visual information — no metadata about the photographer's intent, camera settings, or circumstances of capture is required. The function assesses the result, not the process: a lucky snapshot that frames the cat perfectly scores just as well as a carefully composed portrait.

## Output

A scalar score between **0** and **1**, where:

- **Scores near 1.0** indicate strong intentional framing — the photograph feels like a portrait of a cat, with purposeful placement, cooperative surrounding space, and visual flow that draws the eye to the subject.
- **Scores near 0.0** indicate weak or absent framing — the cat feels like an afterthought, randomly placed, lost in empty space, or competing with a chaotic environment for the viewer's attention.

## What It Evaluates

The function decomposes intentional framing into three distinct dimensions, each evaluated by a dedicated sub-function:

### 1. Subject Placement and Balance — [cat-frame-balance](https://github.com/ObjectiveAI-claude-code-1/cat-frame-balance)

Examines where the cat is positioned relative to the boundaries of the frame and whether that placement feels purposeful or arbitrary. A well-placed cat feels settled in the composition — it belongs where it is, whether centered or off to one side, because the position creates visual equilibrium. Scores poorly when the cat feels abandoned by the frame: shoved into a corner, pressed against an edge, or adrift in a vast emptiness.

### 2. Effective Use of Surrounding Space — [cat-photo-spatial-composition](https://github.com/ObjectiveAI-claude-code-1/cat-photo-spatial-composition)

Assesses the space around the cat — negative space, background, and environment — and whether it serves the subject or works against it. Evaluates both the amount of space (not too cramped, not too vast) and its quality (supportive vs. cluttered and distracting). Scores highly when the cat feels prominent without feeling cramped and the surrounding space cooperates with the subject.

### 3. Compositional Flow Toward the Subject — [compositional-flow-to-subject](https://github.com/ObjectiveAI-claude-code-1/compositional-flow-to-subject)

Determines whether the visual structure of the image — lines, shapes, edges, boundaries, light, and spatial cues — guides the viewer's eye naturally toward the cat. Looks for leading lines, natural frames, light gradients, and converging geometry. Scores highly when the gaze arrives at the cat effortlessly, as if the entire visual world of the photograph was arranged to deliver the viewer to its subject.

## Use Cases

- **Photo scoring** — Distinguish well-composed cat portraits from careless snapshots in rating or ranking systems.
- **Content curation** — Surface images where the cat is truly the star rather than a bystander in large photo collections or feeds.
- **Photography feedback** — Provide compositional guidance to aspiring pet photographers on whether their framing choices are effective.
- **Quality filtering** — Filter out poorly framed images in pipelines that collect, process, or display cat photography.

## Scoring Philosophy

The function's final score is a weighted combination of all three sub-function evaluations. None of the three qualities exist in isolation — a perfectly placed cat in a cluttered, directionless composition still feels accidental, and a beautifully flowing image with a cramped, poorly balanced subject still feels like a missed opportunity. It is in the harmony of all three that true intentional framing emerges: the sense that the photograph is not merely an image containing a cat, but a composition built around one.