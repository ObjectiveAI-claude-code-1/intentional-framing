# intentional-framing

A scalar function that evaluates how deliberately and effectively a cat photograph has been composed around its subject.

## Overview

There is a difference between a photograph *of* a cat and a *cat photograph*. The first is an image in which a cat happens to appear. The second is an image that exists because of the cat — where everything in the frame conspires to say: *look here, at this creature, in this moment.* The `intentional-framing` function exists to distinguish between these two experiences.

It scores the intentionality of a photograph's composition: whether the spatial arrangement of the frame serves the cat as its focal point. This is not an evaluation of rigid compositional rules. A cat sitting dead center in a quiet frame can score beautifully. A cat caught mid-leap along a sweeping diagonal can score just as well. What matters is whether the framing feels like it was made for this cat in this moment.

## Input

| Field | Type | Description |
|-------|------|-------------|
| `input` | `image` | A cat photograph to evaluate for intentional framing — whether the composition feels deliberate and positions the cat as the natural focal point of the image. |

The function receives a single cat photograph. The image is evaluated not just as a collection of objects but as a set of spatial relationships: the cat and the negative space around it, the cat and the edges of the frame, the cat and the lines and shapes that either draw the eye inward or scatter it outward.

## Output

A scalar value between **0** and **1**.

- **High scores (closer to 1)** indicate strong intentional framing — the cat's placement feels chosen, the surrounding space supports the subject, and visual elements guide the eye toward the cat with a sense of compositional inevitability.
- **Low scores (closer to 0)** indicate weak or absent framing — the cat feels randomly placed, the environment overwhelms or marginalizes the subject, and the viewer's eye wanders with no coherent path toward the cat.

## What It Evaluates

The function decomposes intentional framing into three distinct qualities, each assessed by a dedicated sub-function:

### 1. Subject Placement and Balance — [{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

Evaluates where the cat sits within the frame and whether that position feels purposeful. A cat placed with care — whether centered with quiet symmetry or offset with dynamic tension — creates an instant sense of order. This sub-function rejects placements that feel accidental: a cat awkwardly cropped at an edge, crammed into a corner without justification, or marooned in an undifferentiated expanse of empty space. It asks whether the cat's position, among all possible positions, is the one that makes the photograph feel whole.

### 2. Effective Use of Surrounding Space — [{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

Assesses whether the space around the cat plays a supporting role or competes with it. In strong compositions, the surrounding area gives the cat room to breathe — providing context without overwhelming the subject or stealing focus. This sub-function identifies problems such as backgrounds so cluttered that the eye has nowhere to rest, frames so wide that the cat is dwarfed into insignificance, or crops so tight that the cat feels trapped. It measures whether the cat has been given exactly the space it needs, no more and no less.

### 3. Compositional Flow Toward the Subject — [{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

Determines whether the visual elements of the photograph guide the viewer's eye toward the cat. It traces the paths shaped by lines, edges, contrasts, and light gradients, assessing whether they converge on the subject. Leading lines — floorboards angling inward, shelves terminating at the cat, light brightening toward its face — create a sense of compositional inevitability. This sub-function identifies when the flow works against the subject: the eye drifting to competing focal points, following diagonals away from the cat, or wandering without resolution.

## Use Cases

- **Photo contest curation** — Surface the most deliberately composed cat portraits from thousands of submissions, separating intentional compositions from incidental snapshots.
- **Pet photography portfolio assessment** — Help photographers identify which images in their body of work have the strongest compositional presence and visual authority.
- **Social media content elevation** — Rank and prioritize the most visually striking cat photographs for feeds, features, and editorial selections.
- **Photography education and feedback** — Provide aspiring pet photographers with a compositional feedback loop, helping them understand what distinguishes a compelling frame from a forgettable one.

## Philosophy

This function is guided by the principle that intentional framing is a feeling, not a formula. It does not enforce the rule of thirds or demand golden-ratio compliance. It asks a simpler, deeper question: *was this photograph made for this cat?* When the placement is deliberate, the space is generous but controlled, and the eye flows naturally toward the subject, the image transcends the casual snapshot and becomes something worth lingering over. That is the standard `intentional-framing` aspires to measure.