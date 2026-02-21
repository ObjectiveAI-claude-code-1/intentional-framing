# intentional-framing

A scalar function that evaluates how deliberately and effectively a cat photograph has been composed around its subject. It answers a simple but revealing question: does this frame belong to this cat?

## How It Works

The function receives a single cat photograph and returns a score between **0** and **1**.

- A score near **1** means the composition feels purposeful — the cat is clearly the reason the photograph exists, and the spatial arrangement of the image serves the subject.
- A score near **0** means the framing feels accidental — the cat is marginal, awkwardly placed, or lost within a composition that does not serve it.

This is not a measurement of technical perfection or adherence to classical rules like the rule of thirds. A cat sitting dead center in a simple frame can score beautifully. A cat caught along a dynamic diagonal can score just as well. What matters is whether the framing feels like it was made for this cat in this moment.

## Input

| Name | Type | Description |
|------|------|-------------|
| `input` | `image` | A cat photograph to evaluate for intentional framing — whether the composition feels deliberate and positions the cat as the natural focal point of the image. |

## Output

A scalar value between `0` and `1`, where higher values indicate stronger intentional framing.

## What It Evaluates

The function decomposes intentional framing into three dimensions, each evaluated by a dedicated sub-function. The final score is the weighted average of all three evaluations.

### 1. Subject Placement and Balance — [`{{ .Task0 }}`](https://github.com/{{ .Owner }}/{{ .Task0 }})

Examines where the cat sits within the boundaries of the frame and whether that placement creates a sense of visual balance and purposeful anchoring. The cat does not need to be centered or conform to any geometric rule — what matters is that its position feels chosen rather than accidental. Scores high when the cat occupies its space with quiet authority, creating stability and focus. Scores low when the cat is awkwardly cropped, shoved into a margin, or lost without spatial intention.

### 2. Effective Use of Surrounding Space — [`{{ .Task1 }}`](https://github.com/{{ .Owner }}/{{ .Task1 }})

Looks outward from the cat to the space that surrounds it and assesses whether that space serves the subject as a compositional tool. Surrounding space is not emptiness — it is context and breathing room. Scores high when the space around the cat gives the subject room to breathe while keeping it prominent and distinct. Scores low when the cat is either suffocated by clutter or diminished into insignificance by an overwhelming expanse of environment.

### 3. Compositional Flow Toward the Subject — [`{{ .Task2 }}`](https://github.com/{{ .Owner }}/{{ .Task2 }})

Assesses whether the visual structure of the image — its lines, shapes, edges, light, and geometry — guides the viewer's eye toward the cat. Scores high when the viewer's eye arrives at the cat almost without effort, carried by leading lines, natural framing elements, light placement, or subtle geometric cues. Scores low when the eye wanders without direction, distracted by competing elements or left without a path to the subject.

## Use Cases

- **Curating collections** — Filter large sets of cat photographs to surface those with genuine compositional strength.
- **Ranking submissions** — Score and compare cat photographs by how effectively their framing serves the subject.
- **Photographer feedback** — Provide structured insight into whether a photograph's composition works in the cat's favor.
- **Quality baselines** — Establish a compositional quality dimension within a broader multi-factor scoring system for cat photography.
- **Training data selection** — Identify well-composed cat photographs for use in training models on compositional merit.

## Philosophy

The three dimensions — placement, space, and flow — are not independent checkboxes. They are interlocking lenses through which to view a single underlying question: *was this photograph composed around its subject?* A cat perfectly placed but surrounded by chaotic space will not feel intentionally framed. A cat with beautiful leading lines will lose its power if awkwardly cropped at the edge. The dimensions reinforce one another, each contributing to the singular impression that this image was made — whether by skill or by fortune — for this cat in this moment.

At its core, `intentional-framing` is an evaluation of photographic empathy: the degree to which the frame respects its subject.