---
title: "ENCODING LIMINAL SPACE"
subtitle: "A Technical Manual for Reality Engineering"
author: "Geddon Labs Research Division"
classification: "Threshold Operations"
---

# Appendix C: Parameter Tables

This appendix constitutes the **Immutable Specification** of the training execution. These tables record the fixed constants that govern the encoding process, derived from verifying the environment (Chapter 10) and configuring the engine (Chapter 11). The recorded values define the **laws of assimilation** (Learning Rate, Epochs, Batch Size) and the **Physical Threshold** (VRAM, Dependencies). Deviations from this manifest violate **Protocol Purity**. You do not adjust these parameters during execution—they are the foundational constraints that determine whether the system learns your territory faithfully or encodes corrupted patterns.

## C.1 Core Learning Loop Manifest

**Laws of Assimilation: Core Learning Loop Fixed Constants**


| **Parameter** | **Fixed Value** | **Operational Function** |
| :-- | :-- | :-- |
| **Initial Learning Rate** | 1.0 × 10⁻⁴ | Determines the **intensity of initiation**—the pace at which chaos becomes ordered. Controls the magnitude of parameter adjustment per gradient step. Too high produces oscillation and chaos; too low produces stagnation. This value sets the baseline pace of assimilation. |
| **LR Schedule Type** | Warm-up + Exponential Decay | Ensures **structural integrity** across the full training cycle. Warm-up prevents early chaotic parameter jumps during initialization when gradients are unstable. Exponential decay allows aggressive learning during foundational crystallization, then gentle refinement during later stages. |
| **LR Warm-up Steps** | 100 steps | The system begins cautiously at LR = 1.0 × 10⁻⁵, linearly increasing to full value (1.0 × 10⁻⁴) over 100 steps. Allows gradient stabilization before aggressive learning commences. |
| **LR Decay Rate** | 0.999 per step | After warm-up, Learning Rate multiplies by 0.999 each step, producing smooth exponential decay from 1.0 × 10⁻⁴ toward final value of 1.0 × 10⁻⁵. Enables increasingly refined parameter adjustment as learning progresses. |
| **Final Learning Rate** | 1.0 × 10⁻⁵ | Terminal Learning Rate after full decay. Ensures final training steps perform subtle refinement without disrupting crystallized patterns. |
| **Batch Size** | 16 components | The **concurrent observation capacity**—the number of components processed simultaneously before parameter update. Gradient is averaged over 16 examples, providing stable gradient estimates while remaining within hardware VRAM capacity. Represents compromise between gradient stability (larger is better) and memory constraints. |
| **Total Epochs** | 20 cycles | Specifies the **ritual repetition** required for the will to impress itself upon matter. Each component will be processed 20 times throughout training, ensuring patterns achieve stable crystallized form in learned priors without over-specification (memorization). |
| **Coherence Boundary Metric** | Training Loss vs. Validation Loss Divergence | Monitored every 5 epochs. When Training Loss continues decreasing while Validation Loss plateaus or increases, the **Coherence Boundary** has been reached. Training must halt—further repetition corrupts rather than refines learned priors. |

## C.2 Latent Geometry and Fine-Tuning Specification

**Encoded Territory Dimensionality and Permeability**


| **Parameter** | **Fixed Value** | **Operational Function** |
| :-- | :-- | :-- |
| **Latent Space Dimensionality** | 4096 dimensions | Sets the **maximum visual fidelity** the model can ever learn. This is the compression bottleneck—visual information below this threshold cannot be preserved in latent space and therefore cannot be learned. Acts as absolute ceiling for detail encoding regardless of training duration. |
| **Fine-Tuning Rank (LoRA)** | 32 | Controls the **geometric complexity** that can be encoded during fine-tuning. Specifies the number of independent directions in parameter space along which new learning can occur. Rank 32 allows moderate-to-high complexity territory encoding, suitable for territories with distinct but not radically orthogonal concepts relative to base model priors. |
| **Fine-Tuning Alpha (LoRA)** | 0.4 | Controls **structural permeability**—how much the new territory integrates with existing base model learned priors. Alpha 0.4 means new patterns contribute moderately to generation (40% mixing strength), balancing new-territory specificity with base-domain preservation. |
| **Targeted Encoding Strategy** | Moderate Rank, Moderate Alpha | Combined calibration: **Rank 32 + Alpha 0.4** = moderate geometric complexity with moderate permeability. The system can encode reasonably complex new patterns while maintaining partial base-domain competence. New territory manifests distinctly but does not completely dominate base model behavior. |

## C.3 Environmental and Purity Constraints

### Hardware Physical Threshold

| **Parameter** | **Fixed Value** | **Operational Function** |
| :-- | :-- | :-- |
| **VRAM Capacity** | 24 GB | Defines the **absolute physical limit** of the system. Determines maximum batch size, model size, and activation footprint that can be held simultaneously during training. Insufficient capacity forces compromises (smaller batches, lower resolution) that degrade learned fidelity. |
| **Thermal Baseline** | 45°C ± 3°C | Verified stable operating temperature under representative training load. Ensures **Learning Gradient Coherence** by preventing thermal drift. GPU temperature must remain within this range throughout training—thermal variance introduces numerical precision instability that encodes false patterns into learned priors. |

### Protocol Purity Manifest

| **Dependency** | **Exact Version** | **Operational Function** |
| :-- | :-- | :-- |
| **Training Framework** | PyTorch 2.0.1 | Implements the mathematical operations of forward and reverse diffusion. This exact version defines the computational law under which learning occurs. Version changes mid-training violate protocol contract, causing the model to learn under inconsistent mathematical regimes. |
| **CUDA Toolkit** | 11.8 | GPU acceleration library. Determines numerical precision and optimization behavior of GPU operations. Driver version changes alter calculation behavior subtly but measurably. |
| **cuDNN** | 8.6.0 | Deep neural network primitives library for CUDA. Implements core operations (convolution, pooling, normalization). Version stability ensures consistent mathematical behavior across all training steps. |
| **Model Architecture Code** | Commit hash: `a1b2c3d4` | The exact Python code implementing model structure. Specifies layer definitions, tensor operations, forward/reverse pass logic. Any code modification changes what the model learns. |
| **Image Processing Library** | PIL 9.5.0 | Handles image loading, color space conversion, resizing. Different versions process images differently (interpolation algorithms, color handling), introducing subtle but systematic learned biases if changed. |
| **NumPy** | 1.24.3 | Numerical computation library. Provides array operations and mathematical functions. Version stability ensures reproducible numerical behavior. |
| **Python** | 3.10.12 | Base language interpreter. Different Python versions handle floating-point operations and randomness differently. |
| **CUDA Driver** | 535.104.05 | GPU hardware driver. Controls how GPU executes operations at hardware level. Driver updates sometimes change numerical precision or optimization strategies, corrupting learning consistency. |
| **Operating System** | Ubuntu 22.04 LTS | Base operating system. Documented for complete environmental reproducibility. OS-level changes (kernel updates, system libraries) can affect numerical behavior. |
| **Randomness Seeds** | `torch.manual_seed(42)`<br>`np.random.seed(42)`<br>`random.seed(42)` | Ensures the learning process is **deterministic** and the output is **reproducible**. Identical seeds produce identical initialization, identical data shuffling, identical parameter updates. Without fixed seeds, training produces non-reproducible results even with identical dependencies. |
| **Deterministic Mode** | `torch.backends.cudnn.deterministic = True`<br>`torch.backends.cudnn.benchmark = False` | Forces PyTorch to use deterministic algorithms even when non-deterministic variants might be faster. Ensures reproducibility at cost of minor performance reduction. Critical for Protocol Purity. |

## Synthesis and Verification

This manifest provides the **complete fixed specification** of the learning procedure. Every parameter recorded here was derived from understanding your specific situation: your hardware capacity (24 GB VRAM defines Batch Size limits), your territory's complexity (Rank 32 accommodates moderate conceptual distance from base model), your learning timeline (20 Epochs balances sufficient crystallization against over-specification risk), and your quality requirements (LR schedule ensures smooth convergence without chaos or stagnation).

These values are not optimization targets subject to iterative refinement. They are **structural constraints** that define what the training execution means. When you reference "this training run" in future work, you reference this exact specification. The learned priors that emerge will encode patterns discovered under these exact laws of assimilation, within these exact physical boundaries, following these exact mathematical operations.

**Chapter 12: Training Procedures** will use this manifest during the **Initialization Checklist** to verify that the environment meets specification before commencing execution. Every dependency version will be confirmed. Every parameter value will be validated against this document. Only when verification succeeds—when the container is proven pure and the specifications proven exact—will the learning loop begin. This verification ensures that what you intend to encode (your prepared territory) and what the system actually encodes (learned priors) remain aligned, that numerical optimization corresponds to qualitative improvement, that the territory crystallizes faithfully rather than corrupting under environmental contamination or protocol drift.
