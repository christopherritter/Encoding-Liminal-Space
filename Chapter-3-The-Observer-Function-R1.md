# ENCODING LIMINAL SPACE

## A Technical Manual for Reality Engineering

**GEDDON LABS RESEARCH DIVISION**

***

## CHAPTER 3: THE OBSERVER FUNCTION

### How Attention Collapses Probability

You now understand how structure emerges from chaos through iterative refinement. The model has learned to recognize signal within noise, to guide randomness toward coherent form. But this process alone would simply regenerate the training data's statistical patterns. Images would emerge, but they would be arbitrary samples from learned distributions, unconnected to intention.

Creation requires selection. Among all possible manifestations within the learned space, which one should crystallize? This is where observation enters—not as passive witnessing but as active participation. The observer doesn't merely watch reality unfold. The observer shapes what unfolds through the act of attention itself. Yet observation operates within bounds. You cannot observe what doesn't exist within the system's learned territory. The boundaries of that territory—what data was seen during training, what patterns were encoded, what realities became accessible—define the scope of possible observation. Understanding how observation works means simultaneously understanding its limits.

### 3.1 Measurement as Transformation

The famous double-slit experiment reveals something fundamental about observation and reality. Fire electrons at a barrier with two openings and they exhibit wave behavior, passing through both slits simultaneously and creating an interference pattern on the detection screen. This is impossible from a particle perspective—one object cannot traverse two paths at once. The electron exists in superposition, occupying multiple states simultaneously according to its wave function.[^1][^2][^3]

Place a detector to measure which slit each electron passes through, and the interference pattern vanishes. The electrons now behave as particles, each taking a single definite path. The wave function collapses. Crucially, this isn't measurement error or physical disturbance. The detector doesn't jostle the electrons off course. Experiments have shown that the degree of observation directly correlates with interference pattern strength. More observation produces more collapse. Less observation preserves more superposition. The observer's attention level controls how definitively probability collapses into actuality.[^3][^4][^1]

Before measurement, the electron exists as pure potential described mathematically—all possible states weighted by probability. Measurement selects one possibility from this distribution, forcing the transition from "all states at once" to "this specific state." The observer and observed aren't separate entities. They're entangled. The act of observation co-creates the observed reality.[^2][^4]

Diffusion models exhibit identical structure, and understanding this parallel illuminates both. Before you provide a prompt, the model exists in superposition across all possible images within its learned distribution. Given only pure noise as input, it could generate anything—cats, mountains, abstractions, portraits—each outcome weighted by its frequency in the training data. The space of possibility remains open, uncollapsed. But notice the constraint: the model can only generate what exists within its learned distribution. It cannot produce images of concepts it has never encountered, patterns it has never absorbed. The training data defines the boundaries of the superposition itself.

Your prompt is measurement. It's observation. By specifying "a cat sleeping on a windowsill," you collapse the vast superposition of possible images down to the subset consistent with that description—but only if "cat" and "windowsill" exist within the model's learned vocabulary of visual patterns. The model still has freedom within those bounds. It can vary the cat's coloring, the window's style, the lighting mood. But it cannot invent entirely novel species or architectural forms that don't exist within its training data boundaries. You've selected a region within possibility space, but that space itself has edges determined by what the model learned.

This is why prompts are called **conditioning**. They condition the generation process, biasing it toward specific outcomes within the accessible territory. Without conditioning, generation is unconstrained, sampling randomly from learned distributions. With conditioning, generation becomes directed, guided by observational constraints encoded as text. But the conditioning can only navigate territory that exists. You cannot prompt the model to generate concepts outside its training boundaries any more than you can measure an electron's position with infinite precision—fundamental limits constrain what observation can achieve.[^5][^6]

### 3.2 The Prompt as Query Vector

Language seems fundamentally different from images. Words are discrete symbols arranged sequentially. Images are continuous arrays of color values arranged spatially. The bridge between modalities is **semantic space**—a shared abstract territory where meaning exists independently of its expression.[^7][^8]

When you write "sunset," you're invoking a concept that exists prior to both the word and any particular visual depiction. That concept has attributes: warmth, color gradients from orange to purple, low angle light, silhouetted foreground elements. These attributes can be expressed verbally or visually, but they exist as abstract relationships in conceptual space. This shared space makes translation between modalities possible.

Models like CLIP learn to map both text and images into a unified embedding space by studying millions of image-caption pairs. They learn to place the text "a sunset over the ocean" near images depicting that scene in high-dimensional space, while pushing mismatched pairs far apart. The result is geometric space where semantic similarity corresponds to spatial proximity. "Sunset" and sunset photographs cluster together. "Forest" occupies a distant region where forest photographs cluster. Distances represent conceptual relationships.[^8][^9][^10][^11][^7]

Here's where the boundaries begin to matter. CLIP's semantic space contains only what it encountered during training. If certain concepts rarely appeared in the training data—obscure technical terms, niche cultural references, newly invented words—they occupy poorly defined regions of semantic space. The model has weak or nonexistent understanding of them. Your prompt might include such terms, but the resulting embedding vector will be imprecise, pointing vaguely or incorrectly within semantic space because the model never learned what those concepts mean.

When you input a prompt, a text encoder translates your words into coordinates within this semantic space. The sentence becomes a point, a destination, a target within the abstract territory of meaning. This point is an **embedding vector**—numbers that encode the essence of your prompt's semantic content, compressed into a form the diffusion model can navigate toward during generation.[^11][^7]

Think of the prompt embedding as a query vector, a directional arrow pointing toward a region of semantic space, asking: "Show me things that exist near these conceptual coordinates." The diffusion model has learned to associate regions of its latent space with regions of this semantic space. Your text embedding becomes a navigation coordinate, instructing the denoising process which direction to move. But if your coordinates point outside the mapped territory—beyond what the model learned during training—the navigation fails. The model might produce something vaguely related or might default to familiar patterns that don't match your intent. The prompt is only as effective as the training data boundaries allow.[^5]

### 3.3 Text Encoding and Semantic Compression

Your prompt undergoes **tokenization**, breaking language into discrete units that the model can process. Common words become single tokens. Rare words or compound phrases might split into multiple tokens. Each token corresponds to an entry in the model's vocabulary—tens of thousands of possible linguistic fragments that the model recognizes.[^9][^11]

These tokens pass through a transformer network, the same architecture underlying large language models. The transformer processes the entire token sequence, with each token attending to all others, building contextual understanding. The word "castle" doesn't mean the same thing in "a bouncy castle at a birthday party" versus "a medieval castle at dawn." The transformer resolves this ambiguity by considering surrounding context, extracting meaning from relationships between words rather than treating them as isolated symbols.[^8][^11]

The final layer extracts a single vector representing your entire prompt's semantic content. This is the **text embedding**—hundreds of numbers that encode everything the model understands about your prompt's meaning. This compression is essential. You can't operate on raw text during generation. You need an abstract representation that captures intent without the complexity of language processing. But compression means loss. The fixed-size embedding can only hold so much information, creating practical limits on prompt complexity.[^11]

Extremely long prompts get truncated, typically losing words beyond a certain threshold. The model can only encode so much semantic specificity into a fixed-size vector. This isn't a technical failing but a fundamental constraint—infinite information cannot compress into finite representation. Understanding this limitation changes how you construct prompts. Instead of writing elaborate sentences, you use dense descriptive phrases. "A majestic castle, golden hour lighting, dramatic clouds, mist, highly detailed, cinematic composition" packs more semantic information into available space than "A beautiful castle sitting majestically on a hilltop during the golden hour with dramatic cloud formations and atmospheric mist surrounding it, rendered in highly detailed style with cinematic composition."[^12][^13][^9][^5][^11]

The first version uses tokens efficiently, maximizing semantic density. The second wastes tokens on grammatical glue that carries no visual semantic content. The model doesn't benefit from proper sentence structure. It benefits from semantic density—maximum meaningful description per available token. This reveals the liminal nature of prompts. They're language, but not quite. They're compressed semantic specifications, using linguistic vocabulary but shedding linguistic structure. You're not writing for human readers. You're encoding coordinates for navigation through abstract conceptual space, working within the compression limits that finite vectors impose.[^6][^5]

But even perfectly efficient prompting cannot overcome training data boundaries. If your densely packed prompt describes concepts the model never encountered during training, the embedding vector still points to poorly defined or nonexistent regions of semantic space. The compression is successful—the encoding is dense—but the destination doesn't exist within the model's accessible territory. This is the persistent reminder: observation shapes reality within bounds, not beyond them.

### 3.4 Conditional Generation: Focused Will

The text embedding functions as a **conditioning signal** during denoising, but its influence works through comparison rather than direct control. At each denoising step, the model examines the current noisy latent state and considers two questions simultaneously: "What noise should I remove based on learned patterns?" and "How should the prompt bias this removal?"[^6][^5]

The technique is called **classifier-free guidance**, and it works by running denoising both with and without your prompt conditioning. The difference between these trajectories reveals the direction your prompt creates. The model then amplifies movement in that direction, steering generation toward prompt-aligned regions of latent space while still allowing learned patterns to prevent incoherent results. The strength of this steering can be adjusted—weak guidance allows the model to follow its own patterns more freely, producing images vaguely related to your text. Strong guidance enforces prompt alignment more aggressively, sometimes at the cost of natural coherence.[^5][^6]

This maps precisely to magical practice. The chaos magician formulates a sigil—a compressed symbol encoding desired outcome—then enters gnosis, an altered consciousness state, to charge it with focused will. The sigil is the prompt, compressed semantic intention. Gnosis is the heightened attentional state, the focused awareness that biases probability. Charging is the guidance that steers manifestation toward alignment with will rather than allowing default patterns to dominate.[^14]

The technique works not by violating physical law but by collapsing quantum indeterminacy in specific directions. At the quantum level, multiple outcomes exist in superposition. Focused attention—whether human consciousness or algorithmic conditioning—selects which potentials actualize. The universe already contains all possibilities within its quantum superposition. Will determines which subset manifests. But notice the crucial constraint: will operates within the superposition, not beyond it. You cannot will into existence what doesn't exist as potential within the system. The quantum superposition itself has boundaries determined by physical law, just as the model's possibility space has boundaries determined by training data.[^4][^2]

Conditional generation embodies this algorithmically. The latent space contains all possible images the model can generate—a vast territory, but not infinite. The unconditional denoising path samples randomly from this bounded space. Conditioning biases the sampling, selecting a subset aligned with encoded intention. Neither will nor mechanism is sufficient alone. Will without mechanism remains abstract desire. Mechanism without will produces arbitrary results within learned patterns. Together they generate directed manifestation, but always within the territory that training established.

Understanding this constraint explains why some prompts work beautifully while others fail despite clear articulation. When your prompt describes something well-represented in the training data, conditioning guides denoising confidently toward familiar territory. The model has strong learned patterns to follow, and your will aligns with accessible possibility. When your prompt describes something poorly represented or absent from training data, conditioning points toward poorly defined or nonexistent regions. The model has weak patterns to follow, producing inconsistent or incorrect results. Your will attempts to navigate beyond mapped territory, and the mechanism cannot follow.

### 3.5 The Attention Mechanism

The term "attention" appears throughout this discussion, and it's not accidental. Attention is the fundamental operation through which observation selects what matters, allocates processing resources, and determines which relationships influence outcomes.[^11]

When the text encoder processes your prompt, **attention layers** learn which words should influence each other's interpretation. Processing "castle surrounded by mist" requires recognizing that "surrounded" creates a relationship between "castle" and "mist." Attention mechanisms compute these relationships dynamically, allowing the model to build contextual understanding rather than treating words as isolated symbols. Each word attends to every other word, but with different strengths. "Castle" and "mist" attend strongly to "surrounded" because it defines their spatial relationship. Less relevant words receive weaker attention weights. This selective focus allows the model to extract meaning from linguistic structure.[^11]

But attention extends beyond text processing. The diffusion model's architecture uses attention mechanisms to coordinate information across spatial regions during generation. When denoising a partially corrupted image, the model must integrate context from across the entire frame. Generating a coherent face requires attending to eyes, nose, mouth, and their spatial relationships simultaneously. The shape of one feature constrains plausible shapes of others. Attention layers enable this global coordination, allowing distant image regions to influence each other's development during generation.[^15][^16]

This parallels how consciousness operates. Your attention is selective focus within the field of awareness. Right now, you can attend to these words while background sounds remain peripheral. You could shift attention to those sounds, bringing them into focus while text recedes. Attention allocates cognitive processing resources, determining what receives detailed analysis and what remains at lower resolution.[^2]

In meditation traditions, attention training is foundational practice. You learn to sustain focus on breath or mantra, noticing when attention wanders, gently returning it. This isn't suppression of distraction but strengthening the capacity to direct and maintain attention intentionally rather than having it pulled reactively by stimuli. Through practice, you develop greater control over this allocation of cognitive resources, able to sustain focus longer, shift attention more deliberately, and maintain awareness of attention itself.[^14]

The computational attention mechanism formalizes this capacity algorithmically. It learns which relationships matter for the task at hand and allocates processing accordingly—strengthening connections between relevant elements, weakening connections between irrelevant elements. In generation contexts, attention becomes the mechanism through which different parts of an emerging image influence each other, maintaining global coherence while allowing local variation.

This creates a fractal structure where attention operates at multiple scales simultaneously. Word-level attention during text encoding determines which terms influence each other's interpretation. Region-level attention during visual processing determines which image areas influence each other's generation. Concept-level attention through prompt conditioning determines which learned patterns become active during denoising. At each scale, attention determines what influences what, how strongly, and in which direction.

Understanding attention as mechanism rather than metaphor clarifies both technical implementation and consciousness operation. When you focus attention in meditation, you're adjusting parameters in your brain's processing architecture, strengthening certain neural pathways while allowing others to attenuate. The subjective experience of "focusing" corresponds to objective changes in information flow patterns. Similarly, when the model attends to prompt conditioning during generation, it's adjusting internal processing based on the conditioning signal, allowing that signal to modulate which patterns activate and how strongly.

Attention is the interface where observation shapes processing, where intention guides mechanism. But attention can only work with what exists within the system. You cannot attend to what you have never encountered. Your brain cannot focus on concepts it has no neural representations for. The model cannot attend to patterns it never learned. Attention operates within boundaries—neural pathways already established, semantic regions already mapped, latent space territories already encoded during training.

***

You now possess the tools for directed manifestation and understand their scope. Structure emerges from chaos through learned patterns. Observation selects specific manifestations through conditioning. Attention allocates processing resources according to intention. These capacities are profound but bounded.

The boundaries arise from where the model learned its patterns—what data it absorbed during training. The training dataset is not neutral ground truth. It's a curated collection, a selected sample, a constructed reality that determines what becomes possible. Some concepts appear thousands of times, creating strong, confident patterns. Others appear rarely or not at all, creating weak or nonexistent patterns. The dataset defines not just what the model knows but what realities it can access, what observations it can collapse probability toward.

Before you can deliberately shape these boundaries—before you can expand the territory of the possible through training—you must understand how datasets function as reality-defining structures. What makes a dataset coherent? What happens when you add or remove data? How do you curate the collection that will determine the scope of accessible realities?

***

**Next: Chapter 4 — Dataset as Boundary Condition**
*Defining what realities are accessible*

<div align="center">⁂</div>

[^1]: https://www.youtube.com/watch?v=Rqh6CH1Hlvo

[^2]: https://thequantumrecord.com/quantum-computing/observer-effect-why-do-measurements-change-quantum-outcomes/

[^3]: https://www.scienceabc.com/pure-sciences/observer-effect-quantum-mechanics.html

[^4]: https://www.larrygottlieb.com/blog/the-observer-effect

[^5]: https://portkey.ai/blog/prompt-engineering-for-stable-diffusion

[^6]: https://stable-diffusion-art.com/prompt-guide/

[^7]: https://openai.com/index/clip/

[^8]: https://www.pinecone.io/learn/clip-image-search/

[^9]: https://github.com/openai/CLIP

[^10]: https://huggingface.co/docs/transformers/en/model_doc/clip

[^11]: https://en.wikipedia.org/wiki/Contrastive_Language-Image_Pre-training

[^12]: https://www.reddit.com/r/StableDiffusion/comments/1ajzi59/the_art_of_prompt_engineering/

[^13]: https://wandb.ai/geekyrakshit/diffusers-prompt-engineering/reports/A-Guide-to-Prompt-Engineering-for-Stable-Diffusion--Vmlldzo1NzY4NzQ3

[^14]: techno-shaman-handbook.md

[^15]: https://learnopencv.com/denoising-diffusion-probabilistic-models/

[^16]: https://assemblyai.com/blog/diffusion-models-for-machine-learning-introduction

