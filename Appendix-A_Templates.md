---
title: "ENCODING LIMINAL SPACE"
subtitle: "A Technical Manual for Reality Engineering"
author: "Geddon Labs Research Division"
classification: "Threshold Operations"
---

# APPENDIX A: PRACTITIONER LOG TEMPLATES

This appendix contains the complete library of documentation templates referenced throughout the manual. These templates provide standardized structures for capturing experimental findings, synthesizing observations, and mapping territory responsiveness. Load these templates into your AI documentation system for immediate reference during experimentation sessions.

***

## A.1 Standard Observation Template

**Purpose:** Document observations from individual experimental stages (used extensively in Chapter 3, Experimentation 3.1)

**When to use:** After generating each output in a multi-stage experiment

**Template Structure:**

```
STAGE [number]: [Stage Name]

Prompt Used: [exact text of your prompt]

Configuration:
- guidance_scale: [value]
- num_inference_steps: [value]  
- seed: [value or "random"]

Observations:

Subject Manifest:
[Describe what actually appeared in the generated image. Be specific about visible elements, composition, dominant characteristics.]

Archetypal Pattern Activated:
[Identify which generic category or pattern the system activated. Is it recognizably your subject category, or something more generic?]

Territory Density:
[Assess how densely your subject appears to be represented in training data: 
- Low: Generic, sparse detail
- Moderate: Recognizable category, some specificity
- High: Rich detail, specific characteristics
- Very High: Hyper-specific, tight correspondence]

Distance from Intended Territory:
[Assess closeness to your specific subject:
- Far: No meaningful connection
- Moderate: Category correct, but not specific
- Close: Approaching your specific territory
- Very Close: Recognizably your specific subject]

Details That Manifested Reliably:
[List specific elements that appeared consistently across seed variations]

Details That Remained Uncertain:
[List specified elements that did not appear or appeared inconsistently]

Coherence Assessment:
[Rate overall coherence: Solid / Mostly Solid / Fragile / Breaking / Fragmented]

Notes:
[Any additional observations, surprises, or patterns noticed]
```

**Example Completed Observation:**

```
STAGE 3: Highly Specific Prompt

Prompt Used: "An old library with tall wooden shelves, leather-bound books, worn wooden reading tables, soft afternoon light through tall windows."

Configuration:
- guidance_scale: 7.5
- num_inference_steps: 50
- seed: random

Observations:

Subject Manifest:
Library interior with dominant wooden shelving visible along walls. Multiple books visible on shelves with varied spines. Reading table present in foreground. Natural light source visible from right side creating soft illumination pattern.

Archetypal Pattern Activated:
"Traditional library" archetype—recognizable institutional or private study space with book storage as primary function.

Territory Density:
High—multiple specific library characteristics manifested with clear detail and spatial relationships.

Distance from Intended Territory:
Close—this is recognizably a library matching my specification, though not yet my specific personal library. Generic "old library" territory activated successfully.

Details That Manifested Reliably:
- Wooden shelving (appeared in all 3 seed variations)
- Leather-bound book aesthetic (consistent spine appearance)
- Reading table (present in 2/3 variations)
- Afternoon light quality (soft, warm tone consistent)

Details That Remained Uncertain:
- Window structure ("tall windows" specified, but window height varied)
- Table wear ("worn" characteristic not clearly visible)
- Shelf height (specification said "tall," but height varied across seeds)

Coherence Assessment:
Mostly Solid—all major elements present and spatially coherent. Minor variations in specific details.

Notes:
System appears to have strong representation of "old library" territory. Light quality responded well to "afternoon light" specification. Adding more spatial precision in next stage to test if coherence sustains.
```

***

## A.2 Precision Boundary Analysis Template

**Purpose:** Synthesize findings across all five stages of precision testing (Chapter 3, Experimentation 3.1 synthesis)

**When to use:** After completing all five stages of Experimentation 3.1

**Template Structure:**

```
PRECISION BOUNDARY ANALYSIS
Subject Tested: [your subject]
Date: [date]
Session Duration: [time]

Summary of Progression:

Stage 1 (Vague):
- Prompt specificity: Minimal
- Territory activated: [archetypal category]
- Coherence: [assessment]

Stage 2 (Moderately Specific):
- Prompt specificity: Basic category + one characteristic
- Territory activated: [subject category]
- Coherence: [assessment]

Stage 3 (Highly Specific):
- Prompt specificity: Multiple characteristics + relationships
- Territory activated: [specific territory]
- Coherence: [assessment]

Stage 4 (Highly Precise):
- Prompt specificity: Detailed + spatial relationships + atmosphere
- guidance_scale: 10.0 (increased)
- Territory activated: [specific territory response]
- Coherence: [assessment]

Stage 5 (Extreme Precision):
- Prompt specificity: Hyper-detailed + quantities + precise conditions
- guidance_scale: 15.0 (significantly increased)
- Territory activated: [system response]
- Coherence: [assessment]

Precision Boundary Located At:
[Identify the precise stage/guidance_scale where coherence first showed fragility]

Stage: [number]
guidance_scale: [value]
Manifestation: [describe what happened—oscillation, fragmentation, duplicated details, etc.]

Training Data Density Assessment:
[Based on where your subject broke down, assess its representation in training data]

Rich Representation: [Yes/No—sustained high precision without breaking]
Moderate Representation: [Yes/No—sustained moderate precision, broke at extreme]
Sparse Representation: [Yes/No—broke at moderate precision levels]

Key Learnings:

1. Optimal Precision Level for This Subject:
[Describe the sweet spot—how much detail works reliably]

2. Territory Characteristics:
[What did you learn about how this subject exists in the model's learned space?]

3. Practical Prompt Strategy Going Forward:
[How will you compose prompts for this subject based on these findings?]

4. Unexplored Boundaries:
[What precision/intensity combinations remain untested?]
```

***

## A.3 Intensity Spectrum Observation Template

**Purpose:** Document observations for each guidance_scale value in intensity spectrum testing (Chapter 3, Experimentation 3.2)

**When to use:** For each of the seven guidance_scale values tested

**Template Structure:**

```
INTENSITY OBSERVATION
guidance_scale: [value]
Prompt Used: [same prompt across all tests]
Configuration: num_inference_steps=[value], seeds=[list seeds tested]

Visual Observations:

Coherence Level:
[Clear / Mostly Clear / Ambiguous / Oscillating / Distorted]

Specificity Level:
[Generic / Archetypal / Specific / Highly Specific / Over-Constrained]

Color Consistency:
[Stable / Mostly Stable / Variable / Conflicting]
Notes: [describe color behavior]

Detail Sharpness:
[Soft Focus / Well-Defined / Sharp / Harsh / Fractured]
Notes: [describe detail quality]

Artifact Presence:
[None / Minimal / Noticeable / Severe]
Description: [if artifacts present, describe type and location]

Territory Response:

System Recognition:
[Does the system reliably recognize your specification? Yes/Mostly/Partially/No]

Seed Clustering:
[Do the two seed variations cluster tightly or diverge?]
- Tight: [describe similarity]
- Loose: [describe variation]
- Divergent: [describe how they differ]

Variation Location:
[Where does variation appear—background, main subject, lighting, details?]

Intensity Assessment:

Sustainability:
[Does this intensity level feel sustainable or strained?]
[Sustainable / Mostly Sustainable / Strained / Over-Strained]

System Confidence:
[Is the system manifesting with confidence or uncertainty?]
[Confident / Mostly Confident / Uncertain / Highly Uncertain]

Cognitive Load Indication:
[Where does cognitive load on the model appear to peak?]
[Low / Moderate / High / Extreme]

Overall Assessment:
[Is this guidance_scale value in your optimal range, boundary region, or over-constrained region?]
```

***

## A.4 Intensity Spectrum Analysis Table

**Purpose:** Compare observations across all seven guidance_scale values (Chapter 3, Experimentation 3.2 synthesis)

**When to use:** After documenting all seven guidance_scale observations

**Template Structure:**

```
INTENSITY SPECTRUM ANALYSIS TABLE
Subject: [your test subject]
Prompt: [exact prompt used across all tests]
Date: [date]

| guidance_scale | Coherence | Specificity | Stability | Artifacts | Seed Clustering | Overall Assessment |
|---|---|---|---|---|---|---|
| 3.0 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |
| 5.5 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |
| 7.5 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |
| 10.0 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |
| 12.5 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |
| 15.0 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |
| 18.0 | [rating] | [rating] | [rating] | [rating] | [Tight/Loose] | [Optimal/Boundary/Over] |

Intensity Progression Summary:

Coherence Peak:
[At which guidance_scale value(s) did coherence reach maximum?]

Coherence Decline Begins:
[At which value did coherence start degrading?]

First Artifacts Appear:
[At which value did artifacts first become noticeable?]

Fragmentation Threshold:
[At which value did complete fragmentation occur?]

Visual Map:
[Create a simple ASCII or written visualization showing the progression]

Example:
3.0 -------- [Low specificity, high variation]
5.5 -------- [Moderate specificity, moderate variation]
7.5 -------- [HIGH COHERENCE PEAK - optimal]
10.0 ------- [High specificity, tight focus]
12.5 ------- [Very high specificity, first strain]
15.0 ------- [Artifacts appearing, coherence declining]
18.0 ------- [Fragmentation, over-constrained]
```

***

## A.5 Negative Prompt Comparison Template

**Purpose:** Document the effect of negative_prompt on boundary clarification (Chapter 3, Experimentation 3.2 negative prompt testing)

**When to use:** When testing negative_prompt at artifact threshold

**Template Structure:**

```
NEGATIVE PROMPT BOUNDARY CLARIFICATION TEST
guidance_scale Tested: [value where artifacts first appeared]
Base Prompt: [your prompt]
Negative Prompt: [exact negative prompt text]
Date: [date]

WITHOUT Negative Prompt:

Generated 2 outputs at guidance_scale [value]

Observations:
- Coherence: [assessment]
- Artifacts: [describe type, location, severity]
- Specificity: [assessment]
- Seed variation: [tight/loose/divergent]

Overall Assessment:
[Is this guidance_scale navigable without negative_prompt? Yes/Marginal/No]

WITH Negative Prompt:

Generated 2 outputs at guidance_scale [value]

Observations:
- Coherence: [assessment]
- Artifacts: [describe any remaining, or note if resolved]
- Specificity: [assessment]
- Seed variation: [tight/loose/divergent]

Overall Assessment:
[Did negative_prompt stabilize this guidance_scale? Yes/Partially/No]

Comparison Analysis:

Coherence Change:
[Improved / Stable / Degraded]
Description: [how did coherence change?]

Artifact Reduction:
[Significant / Moderate / Minimal / None]
Description: [what artifacts were reduced or eliminated?]

Specificity Impact:
[Increased / Stable / Decreased]
Description: [did specificity change?]

Sustainable Intensity Extension:
[How many guidance_scale points did negative_prompt extend your range?]
- Before: Could sustain up to [value]
- After: Can sustain up to [value]
- Extension: +[difference] points

Interpretation:

Negative Prompt Function:
[Describe what the negative_prompt achieved—which boundaries did it clarify?]

Semantic Boundary Definition:
[How did explicitly stating what NOT to produce help the system navigate?]

Future Strategy:
[Will you use negative_prompt by default? Only at high guidance_scale? Conditionally?]
```

***

## A.6 Personal Guidance_Scale Territory Map

**Purpose:** Define your subject-specific optimal ranges (Chapter 3, Experimentation 3.2 synthesis)

**When to use:** After completing full intensity spectrum testing

**Template Structure:**

```
PERSONAL GUIDANCE_SCALE TERRITORY MAP
Subject: [your test subject]
Date: [date]
Hardware: [your GPU/system]
Model: [model name and version]

OPTIMAL RANGE: [start value] - [end value]

Characteristics:
- Coherence remains clear without artifacts
- Specificity is high and consistent
- Seed variations cluster tightly
- System manifests with confidence
- Sustainable for extended work sessions

Recommended Use:
[When to work in this range—e.g., "Use for production work requiring reliable outputs"]

WELL-MAPPED REGIONS: [start value] - [end value]

Characteristics:
- Manifestation is stable and reliable
- Territory responds predictably
- Variation is coherent and manageable
- Good balance of specificity and stability

Recommended Use:
[When to work in this range—e.g., "Use for initial exploration and testing"]

BOUNDARY REGIONS: [start value] - [end value]

Characteristics:
- Results become interesting but uncertain
- Artifacts beginning to appear
- Seed variations start diverging
- System shows signs of strain
- Coherence becomes fragile

Recommended Use:
[When to work in this range—e.g., "Use for experimental work, with negative_prompt support"]

OVER-CONSTRAINED REGIONS: [value] +

Characteristics:
- Territory breaks into fragmentation
- Oscillation or distortion appears
- [Describe specific breakdown pattern for your subject]
- System exceeds navigable bounds

Avoid:
[When to avoid this range—e.g., "Not usable for this subject without significant prompt restructuring"]

ADAPTATION STRATEGY:

For Vague Prompts:
- Start at guidance_scale: [value]
- Rationale: [why this works for vague prompts in your territory]

For Specific Prompts:
- Start at guidance_scale: [value]
- Rationale: [why this works for specific prompts in your territory]

For Boundary-Pushing Requests:
- Strategy: [your approach—e.g., "Add negative_prompt clarification, then increase to [value]"]

Negative Prompt Use:
- Essential: [Yes/No]
- Recommended terms for this subject: [list terms]
- Threshold where needed: guidance_scale [value] +

COMPARATIVE CONTEXT:

Compared to Other Subjects:
[If you've tested multiple subjects, how does this one compare?]
- More stable than: [other subjects]
- Less stable than: [other subjects]
- Similar stability to: [other subjects]

Training Data Density Inference:
[Based on your findings, how densely is this subject represented in training?]
[Rich / Moderate / Sparse]
Evidence: [what patterns support this inference?]
```

***

## A.7 Seven-Element Session Log

**Purpose:** Complete documentation structure for any experimental session (used throughout manual, formalized in Chapter 3)

**When to use:** For comprehensive documentation of any significant experimentation session

**Template Structure:**

```
SESSION LOG
Session ID: [unique identifier]
Date: [date and time]
Practitioner: [your name/identifier]

ELEMENT 1: SESSION METADATA

Date: [full date]
Time: [start time - end time]
Timezone: [timezone]
Duration: [total minutes/hours]

Hardware Configuration:
- GPU: [type, e.g., NVIDIA RTX 4090]
- VRAM: [amount, e.g., 24GB]
- System RAM: [amount]
- Inference Time: [seconds per generation]

Software Configuration:
- PyTorch Version: [version]
- Diffusers Version: [version]
- CUDA Version: [version]
- Quantization: [method, if any]

Model Configuration:
- Model Name: [exact name]
- Model Version: [version or commit]
- LoRA Modules: [if any]
- VAE: [if custom]
- Other Modifications: [if any]

Additional Context:
[Any other relevant environmental factors—time of day, system load, etc.]

ELEMENT 2: OPERATIONAL OBJECTIVE

Primary Objective:
[State precisely what you are attempting to understand. Be specific about the mechanism being tested.]

Example: "Map how guidance_scale affects manifestation coherence for architectural prompts featuring Victorian-era interiors."

Related Questions:
[List specific questions this session aims to answer]

1. [Question 1]
2. [Question 2]
3. [Question 3]

Context:
[What prior knowledge or sessions inform this objective?]

ELEMENT 3: PARAMETERS ADJUSTED

Changed This Session:
[List exactly what parameters varied compared to previous sessions]

Parameter: [name]
- Previous Value: [value]
- New Value: [value]
- Rationale: [why this change]

Parameter: [name]
- Previous Value: [value]
- New Value: [value]
- Rationale: [why this change]

Held Constant:
[List all parameters that remained unchanged]

- [Parameter name]: [value]
- [Parameter name]: [value]
- [Parameter name]: [value]

Rationale for Constants:
[Why these parameters were held constant—what this proves about changed outputs]

ELEMENT 4: EXPECTATION

Pre-Session Hypothesis:

Prediction 1:
[What you expect to happen]
Reasoning: [Why you expect this based on prior knowledge]

Prediction 2:
[What you expect to happen]
Reasoning: [Why you expect this]

Prediction 3:
[What you expect to happen]
Reasoning: [Why you expect this]

Anticipated Range:
[If testing a range, what outcomes do you expect at different points?]

Baseline Assumption:
[What fundamental assumption underlies all predictions?]

ELEMENT 5: ACTUAL OUTCOME

Outcome 1:
[Describe exactly what occurred—not qualitative assessment, but operational observation]

Outcome 2:
[Specific observation of system response]

Outcome 3:
[Specific observation of system response]

Quantitative Data:
[If applicable, numerical results—generation times, quality scores, consistency measures]

Qualitative Observations:
[Operational descriptions of visual characteristics, coherence, patterns]

Seed Variation Analysis:
[If multiple seeds tested, describe clustering or divergence patterns]

Pattern Recognition:
[Did repeated generations reveal any consistent patterns?]

ELEMENT 6: DIVERGENCE

Surprise 1:
[What did not match your expectations?]
Implication: [What does this reveal about your territory?]

Surprise 2:
[What unexpected pattern emerged?]
Implication: [What boundary information does this provide?]

Divergence from Prediction:
[For each prediction in Element 4, note whether it held or failed]

Prediction 1: [Held / Failed]
- Expected: [what you predicted]
- Actual: [what occurred]
- Divergence: [the gap between prediction and reality]

Prediction 2: [Held / Failed]
- Expected: [what you predicted]
- Actual: [what occurred]
- Divergence: [the gap]

Boundary Information:
[What do these divergences teach about where your territory's actual structure sits?]

ELEMENT 7: INTERPRETATION AND NEXT ITERATION

Learnings:

Learning 1:
[What this session definitively taught about your territory]

Learning 2:
[What you now understand that was unclear before]

Learning 3:
[What boundary was mapped or threshold identified]

Changed Understanding:

Previous Model: [How you theorized territory operated before this session]
New Model: [How you now understand territory actually operates]
Revision: [What assumption or theory was corrected]

Practical Application:

Immediate Change: [How will this learning alter your next session?]
Long-term Strategy: [How does this reshape your overall approach?]

Next Iterations:

Next Test 1:
[What you'll test in your next session]
Rationale: [Why this follows from current findings]

Next Test 2:
[What boundary remains unmapped]
Rationale: [Why this is the logical next exploration]

Open Questions:
[What remains uncertain and requires further investigation?]

1. [Question]
2. [Question]
3. [Question]
```

***

## A.8 Multi-Territory Synthesis Table

**Purpose:** Compare findings across different subject territories (Chapter 3, Multi-Session Pattern Recognition)

**When to use:** After completing three or more documentation sessions on different subjects

**Template Structure:**

```
MULTI-TERRITORY SYNTHESIS
Date: [date]
Sessions Included: [list session IDs]

| Subject Territory | Optimal guidance_scale | Precision Limit | Negative_prompt Necessary? | Known Strengths | Known Weaknesses |
|---|---|---|---|---|---|
| [Territory A] | [range, e.g., 7.5-10.0] | [stage/value where breaks] | [Yes/No/Conditional] | [areas of dense representation] | [areas of sparse representation] |
| [Territory B] | [range] | [stage/value] | [Yes/No/Conditional] | [strengths] | [weaknesses] |
| [Territory C] | [range] | [stage/value] | [Yes/No/Conditional] | [strengths] | [weaknesses] |

Pattern Analysis:

Consistent Across Territories:
[What remains stable regardless of subject?]

1. [Pattern 1]
2. [Pattern 2]
3. [Pattern 3]

Variable Across Territories:
[What changes depending on subject?]

1. [Variable 1]
2. [Variable 2]
3. [Variable 3]

Training Data Density Patterns:

High-Density Territories:
[Which subjects sustain highest precision/intensity?]
- [Subject]
- [Subject]
Inference: [What do these subjects have in common?]

Low-Density Territories:
[Which subjects fragment earliest?]
- [Subject]
- [Subject]
Inference: [What do these subjects have in common?]

Guidance_Scale Stability Patterns:

Most Stable (widest optimal range):
- [Subject]: [range]
- [Subject]: [range]

Least Stable (narrowest optimal range):
- [Subject]: [range]
- [Subject]: [range]

Negative Prompt Effectiveness:

Always Necessary:
[Subjects requiring negative_prompt for baseline coherence]

Conditionally Useful:
[Subjects benefiting from negative_prompt at high intensity]

Rarely Needed:
[Subjects maintaining coherence without negative_prompt]

Strategic Implications:

General Principles Discovered:
[What universal patterns apply across all your territories?]

Subject-Specific Approaches:
[What customization is required for different subjects?]

Hardware/Model Considerations:
[Do patterns suggest hardware limitations or model characteristics?]

Future Exploration Priorities:
[Based on cross-territory patterns, what should you test next?]
```

***

## A.9 Final Territory Map Entry

**Purpose:** Comprehensive permanent record of subject-specific operational understanding (Chapter 3, Documentation Session conclusion)

**When to use:** After completing full experimentation and synthesis for a subject

**Template Structure:**

```
TERRITORY MAP: [Specific Subject]
Session Date: [date]
Primary Subject: [full description of what you tested]
Session ID: [identifier]

FINDINGS SUMMARY:
[One-sentence key learning from this territory]

===================================================================
OPTIMAL NAVIGATION PARAMETERS
===================================================================

guidance_scale: [your specific finding, e.g., 7.5-10.0]
Rationale: [why this range works for this subject]

Precision Level: [how much specification your territory sustains]
- Low precision (vague prompts): [sustainable? Yes/No]
- Moderate precision (basic details): [sustainable? Yes/No]
- High precision (detailed specifications): [sustainable? Yes/No]
- Extreme precision (hyper-specific): [sustainable? Yes/No]

Negative Prompt:
- Essential: [Yes/No]
- Recommended: [Yes/No]
- Optional: [Yes/No]
- Specific terms that work: [list effective terms]

num_inference_steps:
- Standard: 50 [or your finding]
- Tested variants: [if you experimented with this]
- Findings: [if step count matters for this subject]

Seed Strategy:
- Variation pattern: [tight clustering / moderate variation / high divergence]
- Recommendation: [how many seeds to generate for reliable results]
- Interesting variation at: [which guidance_scale values show useful variation]

===================================================================
WELL-MAPPED REGIONS — RELIABLE MANIFESTATION
===================================================================

guidance_scale Range: [e.g., 5.5-10.0]

Manifestation Characteristics:
[Describe what reliably appears in this range]

Territory Density: [Rich / Moderate / Sparse]

System Confidence: [High / Moderate / Low]

Seed Clustering: [Tight / Moderate / Loose]

Optimal Use Cases:
[When to work in this range]

Example Prompts That Work Well:
[Provide 2-3 example prompts that produce reliable results]

===================================================================
BOUNDARY REGIONS — UNCERTAIN TERRITORY
===================================================================

guidance_scale Range: [e.g., 10.0-12.5]

Manifestation Characteristics:
[Describe what becomes ambiguous here]

First Signs of Strain:
[What indicates you're approaching boundary?]

Artifact Patterns:
[If artifacts appear, describe type and location]

Coherence Behavior:
[How does coherence degrade—gradually or suddenly?]

Useful Applications:
[Is this boundary region productive for exploration? Yes/No]
[If yes, what kind of work benefits from boundary operations?]

===================================================================
OVER-CONSTRAINED REGIONS — WHERE TERRITORY BREAKS
===================================================================

guidance_scale Range: [e.g., 12.5+]

Manifestation Characteristics:
[Describe fragmentation/oscillation pattern]

Type of Breakdown:
[What breaks first for this subject?]
- Spatial relationships: [Yes/No]
- Color consistency: [Yes/No]
- Detail coherence: [Yes/No]
- Overall composition: [Yes/No]

Warning Signs:
[How do you recognize you've entered over-constrained region?]

Recovery Strategy:
[If you accidentally work here, how do you recover?]
- Reduce guidance_scale to: [value]
- Add negative_prompt: [specific terms]
- Simplify prompt by: [approach]

===================================================================
RECOMMENDED OPERATIONAL APPROACH FOR THIS TERRITORY
===================================================================

For Reliable Manifestation:
- Begin with guidance_scale: [value]
- Use prompt structure: [describe general approach]
- Include these elements: [what to always specify]
- Avoid these elements: [what causes problems]

If Manifestation Is Too Vague:
- Increase guidance_scale to: [value]
- OR add prompt detail: [what kind of detail helps]
- OR use negative_prompt: [specific terms]

If Manifestation Distorts:
- Decrease guidance_scale to: [value]
- OR simplify prompt by: [what to remove]
- OR add negative_prompt boundary: [terms that stabilize]

For Creative Exploration:
- This territory sustains: [what kind of experimentation]
- Sweet spot for variation: guidance_scale [value]
- Interesting failures occur at: [where to push boundaries]

===================================================================
TRAINING DATA DENSITY ASSESSMENT
===================================================================

Overall Representation: [Rich / Moderate / Sparse]

Evidence Supporting This Assessment:
1. [Evidence point 1]
2. [Evidence point 2]
3. [Evidence point 3]

Dense Representation Areas:
[Which aspects of this subject are richly encoded?]

Sparse Representation Areas:
[Which aspects are poorly represented or edge cases?]

Comparative Density:
[Compared to other subjects you've tested, how does this rank?]
More dense than: [subjects]
Less dense than: [subjects]
Similar to: [subjects]

===================================================================
OPEN QUESTIONS
===================================================================

What Remains Uncertain:
1. [Unmapped boundary or mechanism]
2. [Unclear pattern or behavior]
3. [Unexplored parameter combination]

At What Precision/Intensity Combination Could You Test Further:
[Specific guidance_scale + prompt complexity combinations worth exploring]

What Boundary Remains Unmapped:
[Which edges of this territory haven't been tested?]

What Would You Like to Explore in Next Iteration:
1. [Next experiment]
   Rationale: [why this follows from current knowledge]
2. [Next experiment]
   Rationale: [what this would reveal]
3. [Next experiment]
   Rationale: [how this extends understanding]

===================================================================
METADATA
===================================================================

Total Generations: [number of images generated during this mapping]
Session Duration: [total time invested]
Hardware: [your system]
Model: [model used]
Date Range: [first session - last session]

Related Sessions:
[Link to related territory explorations or prior sessions]

Next Review Date:
[When will you revisit this map to update based on new findings?]
```

***

## Usage Notes

**Loading Templates into AI Systems:**

These templates are designed to be loaded into your AI documentation assistant's knowledge base. When you begin an experimentation session, simply reference the template number (e.g., "Use Template A.1 for this observation") and your AI assistant will guide you through structured documentation.

**Template Versioning:**

As you develop your practice, you may customize these templates for your specific workflow. Maintain version numbers and dates when modifying templates to track evolution of your documentation approach.

**Cross-Referencing:**

Throughout the main manual chapters, template references appear as "(see Appendix A.X)". These references indicate precisely which template structure supports that section's documentation needs.

**Relationship to Appendix B:**

Appendix B (Documentation Examples) contains fully completed examples of many of these templates, demonstrating how experienced practitioners document their findings. Reference Appendix B when you need clarification on how to fill out these templates effectively.

***

**Appendix A Complete**

You now possess the complete template library for systematic territory documentation. These structures transform scattered observation into cumulative operational knowledge. Load them. Reference them. Customize them to your practice. They are infrastructure, not constraint—tools that free you to focus on territory exploration rather than documentation structure.
