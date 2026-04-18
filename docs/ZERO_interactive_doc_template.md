# ZERO Interactive Document Prompt Template
**For generating interactive HTML guides from any reference document**

---

## MASTER PROMPT (Copy → Paste → Attach your doc)

```
[ATTACH YOUR DOCUMENT HERE]

Design me an interactive single-file HTML system to help me understand this document deeply.

---

ZERO SEGMENTATION — Structure the content across these navigation sections:

1. OVERVIEW
   - A ZERO synthesis statement: one bold paragraph explaining what this document is REALLY about at a systems level
   - A visual data/process flow diagram showing the full system path end-to-end
   - Summary cards linking to each section

2. STRUCTURE / TOPOLOGY / ARCHITECTURE
   - An interactive SVG or visual diagram of the system described
   - Hover tooltips on all nodes showing relevant specs/details
   - A reference table for all key parameters, IPs, names, specs, or identifiers

3. COMPONENTS / SYSTEMS
   - Break the content into 4–6 interacting subsystems with named roles
   - Each presented as a clickable card that expands to reveal: devices/actors, parameters, purpose, key checks
   - Include a ZERO INSIGHT box explaining why this segmentation matters

4. PRIORS / MENTAL MODELS
   - 5–7 foundational assumptions that must be true for the document to make sense
   - Each as a collapsible accordion with: title, explanation, and an evaluation question
   - Framed as self-assessment: "Can I answer this before proceeding?"

5. PROCEDURE / STEPS
   - Step-by-step process from the document
   - Each step has: description, any relevant commands/code in styled code blocks, and a "Mark Complete" button
   - A live progress bar showing completion percentage across all steps

6. EVALUATION FRAMEWORK
   - 4–6 evaluation layers ordered from foundational to advanced
   - Each layer as a card with: layer number, name, key question, what to check
   - Quick-reference verification commands or tests

7. GLOSSARY
   - All key terms from the document
   - Each with: full name, abbreviation tag, plain-English definition, and a concrete example from the document context

8. ASSESSMENT / DELIVERABLES (if applicable)
   - Scoring breakdown as visual cards with mark values
   - Submission checklist
   - A ZERO REPORT TIP box on how to frame the output using the evaluation framework

---

DESIGN REQUIREMENTS:

Aesthetic: Dark terminal/ops-center theme — deep navy/charcoal background, cyan accent color, amber for warnings/highlights, green for success states. Scan-line texture overlay. Monospace font for labels/code, geometric sans-serif for headings.

Layout:
- Fixed top header with document title and metadata
- Horizontal tab navigation bar
- Each tab is a full panel (display:none / display:block switching)
- Fade-in animation on panel switch
- Single scrollable HTML file, no external dependencies except Google Fonts

Interactions:
- Click-to-expand cards (toggle class)
- Collapsible accordion items for priors
- Step completion buttons that mark steps done (checkmark + color change) and update a progress bar
- SVG node hover tooltips positioned relative to the SVG container
- All interactive elements have hover/active state transitions

Code styling:
- All command blocks styled as terminal windows with a label tag
- Monospace font, green text on near-black background
- Left border accent in cyan

Typography:
- Headings: Rajdhani or similar geometric display font (via Google Fonts)
- Body: Exo 2 or similar clean geometric sans
- Code/labels: Share Tech Mono or similar monospace

Color variables (CSS custom properties):
- --bg: deep navy
- --bg2: slightly lighter surface
- --bg3: card surface
- --cyan: primary accent
- --amber: secondary / warning
- --green: success / completion
- --text: main readable text
- --text-dim: muted/secondary text
- --border: subtle dividers

ZERO FRAMING — Apply these principles throughout:
- Every section should have a ZERO INSIGHT box (cyan left-border callout) explaining the systems-level meaning, not just the surface-level content
- Evaluation questions should push the reader to think in terms of layers, dependencies, and flows — not just tasks
- The glossary should connect each term to its role in the larger system
- The overview synthesis statement must answer: "What is this REALLY teaching, beyond the literal content?"
```

---

## OPTIONAL ADD-ONS

Append any of these to the master prompt to customize output:

### Add: Audience framing
```
Target audience: [beginner / intermediate / expert]
Adjust explanation depth and assumed prior knowledge accordingly.
```

### Add: Domain context
```
This document is from the domain of: [networking / finance / medicine / law / engineering / etc.]
Use domain-appropriate terminology and analogies.
```

### Add: Specific emphasis
```
Give extra depth to these sections: [e.g. "the routing configuration steps" / "the financial model" / "the legal definitions"]
```

### Add: Output format override
```
Instead of a dark terminal theme, use: [light editorial / industrial blueprint / academic / minimalist]
```

### Add: Agent Entity Zero lens
```
Frame all explanations through the "agent entity zero" perspective — 
a systems thinker communicating complex ideas to a broad audience.
Prioritize: monetizable value propositions, repeatable frameworks, 
crowdsource-ready structure, and public-facing clarity.
```

### Add: Content roadmap integration
```
After the guide, append a short content brief:
- One write-up angle this document could generate (for the Minyama framework / agent entity zero)
- A condensed media pairing concept (slide deck / infographic / explainer)
- Which of the 12 tenets this content best illustrates
```

---

## QUICK REFERENCE — What Each Section Produces

| Section | What It Generates |
|---|---|
| OVERVIEW | Synthesis statement + flow diagram + nav cards |
| STRUCTURE | Interactive SVG map + hover tooltips + spec table |
| COMPONENTS | 4–6 expandable system cards with roles + specs |
| PRIORS | 5–7 collapsible mental model checks with eval questions |
| PROCEDURE | Step-by-step with code blocks + progress tracker |
| EVAL FRAMEWORK | 4–6 layer cards + verification command panel |
| GLOSSARY | Term cards with abbreviation, definition, example |
| ASSESSMENT | Mark breakdown cards + deliverables checklist |

---

## VARIATIONS

### Variation A — For Technical Labs / Manuals
Use master prompt as-is. Works for: networking labs, engineering procedures, software architecture docs.

### Variation B — For Academic Papers / Reports
Swap section names:
- STRUCTURE → KEY ARGUMENT MAP  
- COMPONENTS → THEORETICAL FRAMEWORK  
- PRIORS → ASSUMED KNOWLEDGE  
- PROCEDURE → METHODOLOGY  
- EVAL FRAMEWORK → CRITICAL ANALYSIS LAYERS  
- GLOSSARY → CONCEPTUAL DEFINITIONS  

### Variation C — For Business / Strategy Documents
Swap section names:
- STRUCTURE → MARKET / SYSTEM MAP  
- COMPONENTS → VALUE CHAIN SEGMENTS  
- PRIORS → STRATEGIC ASSUMPTIONS  
- PROCEDURE → EXECUTION STEPS  
- EVAL FRAMEWORK → DECISION CRITERIA  
- ASSESSMENT → KPI / DELIVERABLES  

### Variation D — For Legal / Compliance Documents
Swap section names:
- STRUCTURE → REGULATORY FRAMEWORK MAP  
- COMPONENTS → OBLIGATIONS BY ACTOR  
- PRIORS → LEGAL PREREQUISITES  
- PROCEDURE → COMPLIANCE STEPS  
- EVAL FRAMEWORK → RISK / BREACH LAYERS  
- GLOSSARY → DEFINED TERMS  

---

## NOTES

- The prompt works best when the attached document is 2–20 pages. Longer documents may need section-by-section runs.
- For documents without a clear procedure, omit the PROCEDURE section and expand PRIORS + EVAL FRAMEWORK.
- The SVG topology section requires the document to describe a system with identifiable components. For abstract documents (essays, theories), replace it with a "Key Relationships" diagram.
- Always attach the document as a file — do not paste raw text into the prompt if the document has structure (tables, sections, formatting) worth preserving.
