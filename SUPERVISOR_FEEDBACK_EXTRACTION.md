# General Research Guidelines Extracted from Supervisor Feedback

*This document shows how specific supervisor feedback on the proof-carrying code paper was generalized into universal research guidelines*

## Source Document
`second_paper_proof_carrying/research_plan_with_supervisor_feedback.md`

## Extraction Process: Specific → General

### 1. Ultimate Objective Clarity

**Specific Feedback:**
> "What will be the ultimate objective here? Will it be 3D scene generation or still the image?"

**Generalized Principle:**
- Always specify the final output format clearly (2D/3D, vector/raster, images/scenes/layouts)
- Don't leave ambiguity about output modality
- Distinguish between primary outputs (core contribution) and optional extensions
- Justify why the chosen format is appropriate for the problem

**Why This Matters:**
Ambiguity about output format creates confusion about evaluation metrics, technical requirements, and the scope of contributions.

---

### 2. Output Modality Specificity

**Specific Feedback:**
> "What kind of image are you hoping for? Floor plans? What's on your mind?"

**Generalized Principle:**
- Be specific about output types (e.g., "floorplans" could mean rendered images, CAD files, vector drawings)
- Clarify technical specifications early (file formats, precision requirements, representations)
- Explain the implications of format choices on your approach

**Why This Matters:**
Vague descriptions of outputs make it impossible to design appropriate evaluation protocols and choose the right technical approach.

---

### 3. Application-Driven Research Framework

**Specific Feedback:**
> "Need to work backwards from application to map out research framework"

**Generalized Principle:**
- Start with the real-world use case, not the technical method
- Articulate the problem from user/practitioner perspective first
- Derive research questions from application needs
- Connect practical requirements to technical challenges
- Consider how the solution would be deployed in practice

**Why This Matters:**
Research that starts with "let's use technique X" rather than "let's solve problem Y" often lacks clear motivation and impact assessment.

---

### 4. Mapping to Established Research Areas

**Specific Context:**
The research plan showed mapping to:
- Constrained Generation (NeurIPS/ICML)
- Layout Generation (CVPR/SIGGRAPH)
- Program Synthesis (formal methods)

**Generalized Principle:**
- Map your work to 2-3 established research communities
- Show where your work sits in the research landscape
- Articulate what makes the intersection novel or underexplored
- Frame contributions to appeal to multiple communities
- Reference canonical works from each relevant area

**Why This Matters:**
Helps reviewers understand your contribution context, identifies the right venues, and clarifies how your work advances multiple fields.

---

### 5. Comprehensive Baseline Identification

**Specific Feedback:**
> "There will always be a baseline"

**Specific Context:**
The research plan included 6 baseline categories:
- Floorplan generation baselines (FloorPlan-LLaMa, HouseDiffusion, etc.)
- Constraint-aware generation baselines (ConceptLab, ChatHouseDiffusion)
- Building code compliance baselines (CAD checkers, CODE-ACCORD)
- Post-hoc constraint satisfaction baselines
- Evaluation protocol comparisons
- Benchmark datasets

**Generalized Principle:**
- Identify baselines early in research planning (not after experiments)
- Include multiple categories:
  - Direct competitors (solving the same problem)
  - Adjacent methods (related techniques from neighboring domains)
  - Ablation baselines (your method with components removed)
  - Simple baselines (naive approaches for lower bounds)
- Create structured comparison tables showing what each baseline addresses
- Explicitly identify what gaps your work fills that no baseline covers
- Present baseline strengths honestly, not just limitations

**Why This Matters:**
Comprehensive baseline comparison is essential for establishing novelty, demonstrating improvement, and satisfying reviewers. Missing obvious baselines is a common rejection reason.

---

## Integration into Main Checklist

These principles have been integrated into `1_AI_Research_Paper_Checklist.md` as a new section:

**§ Problem Definition & Research Positioning**

This section appears early in the checklist (before Introduction) because these questions must be answered during research planning, not during paper writing.

### Subsections Created:
1. ✅ **Ultimate Objective Clarity** (4 checklist items)
2. ✅ **Application-Driven Research Framework** (5 checklist items)
3. ✅ **Mapping to Established Research Areas** (5 checklist items)
4. ✅ **Baseline Identification Strategy** (5 checklist items)

### Enhanced Existing Section:
- **§ Experimental Validation** → Added "Comprehensive Baseline Strategy" subsection (5 checklist items)

---

## Key Insight: Research Planning vs. Paper Writing

Notice that most of these principles apply to **research planning**, not just paper writing:

| Principle | When to Apply |
|-----------|---------------|
| Ultimate objective clarity | Research design phase |
| Output modality specificity | Problem formulation phase |
| Application-driven framework | Project inception phase |
| Mapping to established areas | Literature review phase |
| Baseline identification | Experiment design phase |

**Implication:** Use the updated checklist as a **research planning tool**, not just a writing checklist.

---

## Universal Applicability

These principles work across AI research domains:

- **Computer Vision**: What outputs? (segmentation masks, bounding boxes, 3D meshes?)
- **NLP**: What format? (sequences, trees, graphs, embeddings?)
- **Robotics**: What modality? (trajectories, control signals, policies?)
- **ML Theory**: What problem class? (supervised, RL, generative?)

The supervisor's feedback on a specific architectural AI project revealed general principles that apply to any AI research.

---

## Using This for Future Research

**Before starting any new project:**
1. ✅ Write a one-paragraph description of the ultimate output
2. ✅ Specify all technical format details
3. ✅ Describe the real-world application scenario
4. ✅ List 3 research communities your work relates to
5. ✅ Identify 5-10 potential baselines across multiple categories

**If you can't complete these 5 tasks clearly, your research problem isn't well-defined yet.**

---

*Last updated: October 5, 2025*
*Source feedback: Supervisor review of proof-carrying code research plan*
