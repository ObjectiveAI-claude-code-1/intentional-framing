# intentional-framing

Scores how deliberate and effective the compositional framing of a cat photograph feels. Evaluates subject placement and balance, spatial harmony between the cat and its environment, and compositional flow toward the subject. Higher scores indicate photographs that feel composed around the cat rather than merely containing one.

## Purpose

A cat photograph can be a portrait — a deliberate arrangement of space that honors the cat as its subject — or it can be something far less: an image that merely contains a cat, where the subject is incidental to the frame rather than the reason for it. **intentional-framing** distinguishes between these two outcomes.

Given a cat photograph, this function evaluates whether the spatial relationship between the cat and everything else in the frame serves the cat as the focal point. It asks a deceptively simple question: does this photograph feel like it was made for this cat in this moment?

This is not an evaluation of rigid compositional rules. The rule of thirds is irrelevant here. A cat sitting dead center in a quiet frame can score beautifully. A cat caught along a sweeping diagonal can score just as well. What matters is whether the framing feels purposeful — whether the composition, however it was achieved, works in the cat's favor.

## Input

The function receives a single **cat photograph** as input — the complete image as captured or cropped. Every element within the frame becomes part of the evaluation: the cat itself, the space around it, the objects and textures that populate the background and foreground, and the boundaries of the image where the photographer's world ends.

The photograph is treated as a finished composition. The function does not speculate about what lies beyond the frame. It evaluates the spatial reality of the image as it exists and asks whether that reality serves the subject.

## Output

A **scalar score between 0 and 1**.

- Scores approaching **1.0** indicate compositions where the framing feels highly intentional — the cat is placed with purpose, given space that serves it, and surrounded by visual structure that draws the viewer in.
- Scores approaching **0.0** indicate compositions where the cat feels like an afterthought — lost in the frame, overwhelmed by its environment, or trapped in a composition that was never designed around it.
- Scores in the **middle range** indicate partial intentionality — photographs where some dimensions of framing work in the cat's favor while others fall short.

## What It Evaluates

The function assesses three interconnected dimensions of compositional framing. Each captures a different aspect of how the frame relates to its subject.

### 1. Subject Placement and Balance

> [cat-subject-placement](https://github.com/ObjectiveAI-claude-code-1/cat-subject-placement)

Evaluates where the cat is positioned within the architecture of the frame and whether that placement feels purposeful. Strong placement means the cat anchors the composition with a clear center of gravity — the viewer immediately understands where to look. There is a sense of visual equilibrium between the weight of the subject and the weight of the surrounding space.

**Strong signals:** The cat occupies its position with a sense of belonging, as though the frame was drawn around it. The placement feels chosen, even if captured in a fleeting moment. The composition has balance — not rigid symmetry, but the kind of equilibrium where subject and space feel in conversation.

**Weak signals:** The cat is crammed against an edge, awkwardly bisected by the frame boundary, or marooned in emptiness without compositional reason. The viewer's eye wanders, unsure of what the photograph is about. The cat is technically present but compositionally absent.

### 2. Spatial Harmony

> [cat-spatial-harmony](https://github.com/ObjectiveAI-claude-code-1/cat-spatial-harmony)

Evaluates the relationship between the cat and the space around it — negative space, background elements, and foreground objects — and whether that relationship serves the subject. The negotiation between subject and environment should be resolved in the cat's favor.

**Strong signals:** The cat is given room to breathe without being dwarfed. Negative space feels purposeful — it frames, cushions, and stages the cat. Background elements belong to the same visual story as the subject rather than competing with it. The environment acts as a stage for the cat.

**Weak signals:** The background overwhelms the subject with busy textures or dominant shapes. Framing is so tight the cat feels claustrophobic, or emptiness is so vast the cat feels abandoned. The space works against the subject rather than for it — the environment is a distraction, not a stage.

### 3. Compositional Flow

> [cat-compositional-flow](https://github.com/ObjectiveAI-claude-code-1/cat-compositional-flow)

Evaluates whether the visual structure of the image — lines, shapes, boundaries, and tonal contrasts — creates pathways that guide the viewer's eye toward the cat. What matters is the cumulative effect: whether the image has a visual current that carries the viewer to the subject.

**Strong signals:** Leading lines converge toward the cat. Natural frames such as doorways or arches isolate the subject. Pools of light, gradients of focus, or tonal shifts make the cat pop against its background. The viewer's eye arrives at the subject effortlessly and inevitably.

**Weak signals:** The eye bounces around the frame without direction. No visual cues guide attention toward the cat. The subject must compete for the attention it should naturally command. The image lacks a sense of visual order that works in the cat's favor.

## Use-Cases

- **Photo curation and ranking**: Surface cat photographs where the cat feels like the protagonist rather than a bystander in its own picture.
- **Photographer feedback**: Assess whether compositional instincts are translating into images that honor the subject.
- **Automated filtering**: In pipelines processing large volumes of cat imagery, filter out photographs where the cat is lost, marginal, or awkwardly trapped within a frame that was never designed around it.
- **Quality benchmarking**: Use as a foundational compositional signal alongside other quality dimensions such as lighting, focus, and expression.

## Sub-Functions

| # | Sub-Function | What It Evaluates |
|---|---|---|
| 0 | [cat-subject-placement](https://github.com/ObjectiveAI-claude-code-1/cat-subject-placement) | Subject placement and balance within the frame |
| 1 | [cat-spatial-harmony](https://github.com/ObjectiveAI-claude-code-1/cat-spatial-harmony) | Spatial harmony between the cat and its environment |
| 2 | [cat-compositional-flow](https://github.com/ObjectiveAI-claude-code-1/cat-compositional-flow) | Compositional flow toward the subject |