# intentional-framing

Evaluates the intentional framing of a cat photograph — scoring how deliberate and effective the composition feels, and whether the spatial arrangement of elements serves the cat as the natural focal point of the image.

## Purpose

There is a meaningful difference between a photograph *of* a cat and a photograph that merely *contains* one. The first feels deliberate: the frame was built around the subject. The second feels accidental: the cat is present, but the image does not belong to it. This function measures where a given cat photograph falls on that spectrum.

The evaluation is style-agnostic. It does not enforce compositional rules like the rule of thirds, nor does it reward any particular placement strategy. A centered cat in a simple frame can score beautifully. A cat caught along a dynamic diagonal can score just as well. What matters is whether the framing feels like it was made for this cat in this moment — whether the viewer senses that the image was composed around its subject.

## Input

| Field | Type | Description |
|-------|------|-------------|
| input | `image` | A cat photograph to evaluate for intentional framing — whether the composition feels deliberate and positions the cat as the natural focal point of the image. |

The function receives a single cat photograph with no additional metadata. This mirrors the viewer's experience: when encountering a photograph, the viewer has no knowledge of the photographer's intent, equipment, or process. The image must speak for itself.

## Output

A scalar value between **0** and **1**.

- Scores near **1** indicate strong intentional framing — the photograph feels composed around the cat, with purposeful placement, supportive surrounding space, and visual elements that guide the eye toward the subject.
- Scores near **0** indicate weak or absent framing — the cat feels like an afterthought, lost in its environment, awkwardly placed, or competing with its surroundings for the viewer's attention.

## What It Evaluates

The function decomposes intentional framing into three distinct dimensions, each assessed by a dedicated sub-function:

### 1. Subject Placement and Balance
[{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

Evaluates where the cat sits within the frame and whether that position feels purposeful and anchored. Assesses whether the visual weight of the composition — the cat, its background, the negative space — is distributed in a way that creates equilibrium or purposeful tension. A well-placed cat feels like it could not reasonably be anywhere else without the image suffering for it. A poorly placed cat feels adrift, shoved into a corner, awkwardly cropped, or marooned in irrelevant space.

### 2. Effective Use of Surrounding Space
[{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

Evaluates everything in the photograph that is not the cat — the negative space, background, and environment — and determines whether it supports or undermines the subject. The ideal surrounding space gives the cat room to breathe without dwarfing it, provides context or atmosphere without introducing clutter, and complements the subject the way a setting frames a jewel. Too much space makes the cat insignificant; too little makes it feel cramped; cluttered space fragments the image's coherence.

### 3. Compositional Flow Toward the Subject
[{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

Evaluates whether the visual elements within the photograph — leading lines, natural boundaries, tonal contrasts, environmental geometry — create a current that guides the viewer's eye toward the cat. In a photograph with strong compositional flow, the eye arrives at the cat naturally and settles there with satisfaction. In a photograph with weak flow, the eye wanders without direction or is drawn to competing elements that make the cat feel incidental.

## Use-Cases

- **Photo ranking and curation**: Surface cat photographs with strong compositional craftsmanship from large collections.
- **Photography feedback**: Help photographers understand why one framing of the same cat in the same room feels more compelling than another.
- **Quality filtering**: Use as one signal among many in a multi-dimensional evaluation of cat photograph quality.
- **Gallery selection**: Identify images that demonstrate intentional composition for curated publications or exhibitions.

## Scoring Philosophy

Strong intentional framing means the spatial relationship between the cat and its surrounding space serves the subject. The cat is given room to breathe but is not dwarfed by its environment. The composition works with the subject rather than against it. The viewer senses visual order — a feeling that everything within the frame participates in presenting the cat.

Weak framing makes the cat feel like an afterthought. The background dominates, the cat is marginal, the crop disrupts the viewer's ability to appreciate the subject, or the visual elements scatter attention away from the cat rather than toward it.

The hallmark of a high-scoring photograph is a sense of inevitability — as though the rectangle of the image was drawn around the cat, rather than the cat dropped into a rectangle.