# rank-cat-composition

## Overview

**rank-cat-composition** is a sophisticated compositional analysis function that evaluates and ranks cat photographs by artistic excellence. Rather than assessing cuteness or technical perfection, this function recognizes and elevates photographs that demonstrate intentional, thoughtful composition—images where the photographer has made deliberate artistic choices about framing, balance, subject placement, and context.

In an age of endless casual snapshots, this function distinguishes images that showcase genuine photographic vision from those that rely on accident or luck. It serves photographers developing their craft, curators selecting meaningful images, educators teaching visual literacy, and enthusiasts who wish to deepen their appreciation for photographic artistry.

## Input

The function accepts an array of cat photograph objects:

```json
[
  {
    "url": "string (required)",
    "title": "string (optional)",
    "photographer": "string (optional)"
  },
  ...
]
```

- **url**: The URL or file path to the cat photograph image (required)
- **title**: Optional title or label for the photo
- **photographer**: Optional photographer credit

The array must contain between 2 and 100 photographs.

## Output

The function returns a ranking vector—an array of decimal numbers between 0 and 1, where each number represents the relative rank of the corresponding photo in the input array. Numbers sum to approximately 1.0. Photos with higher values are ranked as having superior compositional excellence.

Example output for 3 photos:
```json
[0.45, 0.35, 0.20]
```

In this case, the first photo ranks highest, followed by the second and third.

## What It Evaluates

The rank-cat-composition function evaluates four interconnected dimensions of compositional excellence:

### 1. Compositional Deliberation
Assesses whether the photographer has made intentional, thoughtful choices about framing, angle, and subject positioning. Does the composition demonstrate understanding of photographic principles like the rule of thirds, leading lines, and perspective? Is the frame boundary carefully selected to emphasize what matters? Photos with deliberate artistic choices rank higher than those appearing accidental.

### 2. Visual Balance and Coherence
Examines the overall harmony and unity of visual elements. Do colors, textures, tones, and spatial elements work together in a balanced, cohesive way? Is there a visual rhythm and logic that guides the viewer's eye, or do elements feel scattered and competing? Images with harmonious composition feel unified and restful to the eye.

### 3. Subject Prominence and Narrative Clarity
Evaluates how effectively the cat functions as the primary focal point and narrative anchor. Does the cat's position and framing naturally draw the eye first? Does the composition convey something meaningful about the cat's character, mood, or relationship to its environment? Photos where the cat's placement suggests intentional creative vision rank higher.

### 4. Contextual Supportiveness
Assesses how well the background, environment, and surrounding elements enhance the cat as the primary subject. Does the context provide meaningful visual support through color contrast, tonal balance, or compositional logic? Or do background elements distract and compete for attention? True compositional excellence involves understanding that the space around the subject is as important as the subject itself.

## Use-Cases

- **Photographer Development**: Help photographers identify their compositional strengths and weaknesses to guide artistic growth
- **Gallery and Publication Curation**: Select photographs that will resonate and inspire rather than merely entertain
- **Visual Education**: Teach students to recognize and understand principles of composition through concrete examples
- **Portfolio Review**: Assess which images from a collection demonstrate the photographer's best compositional thinking
- **Photo Contest Evaluation**: Identify submissions that showcase intentional artistic vision alongside technical quality
- **Personal Growth**: Develop aesthetic appreciation for thoughtful photography and understand what makes images transcendent

## Sub-Functions

This function is composed of four specialized evaluation sub-functions:

- **{{ .Task0 }}**: Scores each photo on compositional deliberation—the intentionality and thoughtfulness of framing choices
  
  https://github.com/{{ .Owner }}/{{ .Task0 }}

- **{{ .Task1 }}**: Ranks photos on visual balance and coherence—the harmony of all visual elements working together
  
  https://github.com/{{ .Owner }}/{{ .Task1 }}

- **{{ .Task2 }}**: Ranks photos on subject prominence and narrative clarity—how effectively the cat serves as focal point
  
  https://github.com/{{ .Owner }}/{{ .Task2 }}

- **{{ .Task3 }}**: Ranks photos on contextual supportiveness—how well background and environment enhance the subject
  
  https://github.com/{{ .Owner }}/{{ .Task3 }}

Each sub-function specializes in evaluating one dimension of compositional excellence, and their combined insights produce the final ranking.

## Philosophy

rank-cat-composition is built on the belief that photography is not merely a matter of luck, equipment, or subject appeal, but fundamentally an art of seeing and thinking. It honors photographers who pause, observe, and compose with purpose. By recognizing these deliberate artistic choices, the function celebrates visual thinking and deepens appreciation for the craft of photography.