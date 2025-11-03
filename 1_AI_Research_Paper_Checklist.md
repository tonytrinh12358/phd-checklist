# AI Research Paper Writing Checklist
*Based on expert supervisor feedback - Use this checklist for all future AI research papers*

## **Quick Reference to Other Tools**
- → **Paper structure & page allocation**: See `REF_paper_structure.md`
- → **Statistical tests & reporting**: See `REF_statistical_rigor.md`

---

## 🎯 **BEFORE STARTING RESEARCH** ⚠️ CRITICAL

*Use this checklist during research planning, not just paper writing. If you can't complete these 5 tasks clearly, your research problem isn't well-defined yet.*

### Pre-Research Definition Checklist
- [ ] **One-paragraph output description** - write a clear paragraph describing the ultimate output of your research (format, modality, specifications)
- [ ] **Technical format details specified** - document all technical specifications (file formats, precision requirements, representations, dimensions)
- [ ] **Real-world application scenario described** - articulate the concrete use case and deployment context for your solution
- [ ] **3+ research communities identified** - list the established research areas your work relates to (with example venues)
- [ ] **5-10 potential baselines listed** - identify baselines across multiple categories before starting experiments:
  - Direct competitors solving the same problem
  - Adjacent methods from neighboring domains  
  - Simple/naive approaches for lower bounds
  - State-of-the-art methods from related areas

### Why This Matters
Completing this checklist prevents:
- ❌ Ambiguity about evaluation metrics and technical requirements
- ❌ Difficulty designing appropriate evaluation protocols
- ❌ Research that lacks clear motivation ("let's use technique X" vs. "let's solve problem Y")
- ❌ Missing obvious baselines (common rejection reason)
- ❌ Unclear positioning within the research landscape

---

## **Core Writing Philosophy**

###  **Self-Contained & Accessible Writing**
- [ ] **"Grandmother test"** - write so someone with no prior knowledge can understand (except theorems)
- [ ] **Define all technical terms** - explain every acronym, method name, or technical concept on first use
- [ ] **Avoid jargon without explanation** - if you use terms like "Align Only", "Quality Only", explain what they mean
- [ ] **Progressive complexity** - introduce simple concepts before building to complex ones

## **Problem Definition & Research Positioning**
*Critical foundation questions to answer during research planning - these inform experimental design*

###  **Ultimate Objective Clarity**
- [ ] **Specify the final output format** - be crystal clear about what you're generating (2D/3D, vector/raster, images/scenes/layouts)
- [ ] **Output modality specificity** - don't leave ambiguity about the type of output (e.g., "floorplans" could mean rendered images, CAD files, or vector drawings - specify which)
- [ ] **Primary vs. secondary outputs** - distinguish between core contributions and optional extensions
- [ ] **Format justification** - explain why the chosen output format is appropriate for your problem (e.g., vectors for precision, 3D for realism)
- [ ] **Technical specification clarity** - document file formats, precision requirements, and representation choices

*Why this matters: Ambiguity about output format creates confusion about evaluation metrics, technical requirements, and scope of contributions.*

###  **Application-Driven Research Framework**
- [ ] **Work backwards from application** - start with the real-world use case and derive research questions from it
- [ ] **Concrete problem statement** - articulate the problem from the user/practitioner perspective first
- [ ] **Research question derivation** - explicitly show how research questions emerge from the application need
- [ ] **Bridge application to research** - connect practical requirements to technical challenges and contributions
- [ ] **Real-world validation context** - consider how your solution would be evaluated or deployed in practice

*Why this matters: Research starting with "let's use technique X" rather than "let's solve problem Y" often lacks clear motivation and impact assessment.*

###  **Mapping to Established Research Areas**
- [ ] **Identify related problem domains** - map your work to 2-3 established research communities (e.g., constrained generation, layout synthesis, program synthesis)
- [ ] **Position within landscape** - show where your work sits relative to existing research areas
- [ ] **Highlight novel intersection** - articulate what makes your combination of areas novel or underexplored
- [ ] **Cross-community appeal** - frame contributions to be valuable to multiple research communities
- [ ] **Reference canonical works** - cite seminal papers from each relevant research area to establish context

*Why this matters: Helps reviewers understand contribution context, identifies right venues, and clarifies how your work advances multiple fields.*

###  **Comprehensive Baseline Strategy** ⚠️ CRITICAL
*"There will always be a baseline" - identify all relevant baselines early in research planning (not after experiments)*

- [ ] **Multi-category baseline coverage** - include baselines from different research angles:
  - Direct competitors (methods solving the same problem)
  - Adjacent methods (related techniques from neighboring domains)
  - Ablation baselines (your method with components removed)
  - Simple baselines (naive approaches to establish lower bounds)
- [ ] **Exhaustive keyword search** - search for papers with ALL keyword variations:
  - Example: For "prompt optimization" also search: "prompt tuning", "prompt learning", "prompt engineering", "instruction optimization", "instruction tuning"
  - Use at least 5 different keyword combinations for your problem
- [ ] **Current SOTA comparison** - compare against papers from the last 12 months
- [ ] **ArXiv recency check** - check arXiv for relevant papers from the last 3 months
- [ ] **Baseline gaps analysis** - explicitly identify what existing baselines DON'T address that your work does
- [ ] **Structured baseline comparison table** - create table showing what each baseline addresses and limitations
- [ ] **Fair comparison protocol** - ensure baselines are evaluated on the same criteria as your method
- [ ] **Equal implementation care** - implement baselines with same rigor as your method:
  - Same hyperparameter tuning effort
  - Same computational budget
  - Same data preprocessing and augmentation
- [ ] **Published numbers vs. reimplementation** - if using published numbers, explain why; if reimplementing, document any differences
- [ ] **Baseline strengths acknowledgment** - honestly present what each baseline does well, not just their limitations

*Why this matters: Comprehensive baseline comparison establishes novelty, demonstrates improvement, and satisfies reviewers. Missing obvious baselines is a common rejection reason (25% of rejections).*

### 📌 **Universal Applicability Across AI Domains**

These principles apply regardless of your specific AI research area:

| Domain | Output Clarity Question | Example Formats |
|--------|------------------------|-----------------|
| **Computer Vision** | What outputs are you generating? | Segmentation masks, bounding boxes, 3D meshes, depth maps |
| **NLP** | What format/structure? | Sequences, parse trees, graphs, embeddings, structured data |
| **Robotics** | What modality/representation? | Trajectories, control signals, policies, motion plans |
| **ML Theory** | What problem class? | Supervised learning, RL, generative models, optimization |
| **Generative AI** | What type of generation? | Images, text, audio, 3D objects, code, structured outputs |

*Remember: These questions should be answered during research design, not while writing the paper.*

## 📝 Introduction Section

###  **Claims & Evidence Strategy** ⚠️ CRITICAL
- [ ] **Cite supporting papers** for all major arguments, especially in opening paragraphs
- [ ] **Back claims with evidence** - if you claim existing approaches have problems, show qualitative examples
- [ ] **Qualitative evidence** for comparative claims (show where existing methods fail vs. your approach succeeds)
- [ ] **Map claims to experiments** - every performance claim in intro should have corresponding experimental validation planned
- [ ] **Comprehensive evaluation metrics** - if claiming improvements in multiple dimensions, plan experiments for all of them
- [ ] **Avoid unsupported claims** - only claim what you can experimentally validate

###  **Method Overview & Technical Details**
- [ ] **Explain "HOW" not just "WHAT"** - don't just say what your method introduces, explain how it achieves it
- [ ] **Include technical components** (e.g., LLM, Diffusion, DPO/SFT) with appropriate references
- [ ] **Include variance analysis** in key figures (run experiments multiple times with different seeds)
- [ ] **Comprehensive figure legends** and detailed captions for all figures

### ✅ **Venue Appropriateness & Positioning**
- [ ] **Avoid "integrated" language** - for focused venues (e.g., CVPR), don't say "vision-integrated" as it implies the vision component is optional; use "vision-based" or "vision-driven" to emphasize the core focus
- [ ] **Position work at venue's core** - frame your work so the main component matches the venue's focus (vision for CVPR, NLP for ACL, etc.), not as an applied system where the venue's focus is just one module
- [ ] **Front-load primary discipline** - put the venue's discipline (e.g., vision) at the forefront of your narrative, not as a preprocessing step

### ✅ **Writing Precision & Clarity**
- [ ] **Justify unusual numbers** - if you mention "901 samples" or other non-round numbers, either explain why (e.g., "all available samples from 3 generators") or downplay specificity and delegate details to captions
- [ ] **Use complete sentences** - avoid fragments like "The challenge: how to add X" → rewrite as proper sentences with more detail
- [ ] **Generalize specific mentions** - instead of "where Stable Diffusion excels", consider "where diffusion models excel" unless you truly mean only Stable Diffusion
- [ ] **Define all acronyms immediately** - e.g., "classical CV" should be "classical computer vision (CV)" on first use

### ✅ **Analogies & Positioning Relative to Prior Work**
- [ ] **Avoid direct "analogous" claims** - saying "We propose an analogous solution to [X]" can sound like you just applied [X] to your problem
- [ ] **Emphasize differences first** - instead of analogy, say "[X] addressed problem Y in domain Z, but this is insufficient for our domain because..." then explain your novel approach
- [ ] **Frame as inspiration, not transplantation** - if a prior work inspired you, acknowledge it but emphasize what's fundamentally different about your problem and solution

### ✅ **Theoretical Details in Introduction**
- [ ] **Provide intuition before formalism** - don't reference "Theorem 4" before explaining what your method does at a high level
- [ ] **Order theorems logically** - if you reference Theorem 4 before Theorem 2, consider reordering or restructuring
- [ ] **Minimize symbols in introduction** - avoid notation like E(G_k) and convergence details before describing the method intuitively
- [ ] **Defer technical details** - convergence rates and Lipschitz continuity should come after method overview, ideally with reference to a schematics figure

### ✅ **Contribution Organization**
- [ ] **Use 3-4 clear bullets** - contributions should be formatted as a bulleted list, not a dense paragraph
- [ ] **Eliminate redundancy** - if you repeat the same information, it suggests unclear organization; say each thing once in the right place
- [ ] **Be concise yet complete** - each bullet should cover one major contribution without excessive detail
- [ ] **Progressive disclosure** - contribution bullets provide high-level claims; details go in method section

### ✅ **Results Preview in Abstract/Intro**
- [ ] **Provide context for numbers** - if stating results like "84% reduction, 99.3% accuracy", explain what these mean for the reader
- [ ] **Connect to main claim** - add a sentence explaining why these results matter (e.g., "demonstrating our method's ability to improve any generator")
- [ ] **Consider teaser figures** - if you mention large numbers like "901 samples" or complex results, create a plot showing the key findings

## 🔗 Related Work Section

### ✅ **Section Structure & Organization**
- [ ] **No formal subsections** - avoid `\subsection{}` in Related Work; use `\noindent{\bf Title:}` for paragraph headings instead
- [ ] **Limit to 4-5 paragraphs** - keep Related Work concise by grouping similar works together
- [ ] **Start with context** - begin with a sentence establishing why this research area is important (e.g., "X is gaining traction due to its practical importance...")
- [ ] **Cluster citations** - group related works together with multiple citations rather than discussing each individually
- [ ] **Establish relevance early** - each paragraph should make clear how these works relate to your paper and why they're insufficient

###  **Citation Best Practices**
*Applies throughout paper: Introduction, Related Work, Methodology, and Experiments*

- [ ] **Use appropriate citation formats**: `\citet` for in-text author mentions, `\cite` for parenthetical citations
- [ ] **Remove redundant author names** by choosing correct citation commands
- [ ] **Follow conference styling** for references and formatting requirements
- [ ] **Cite all datasets** - provide citations for every dataset used in evaluation
- [ ] **Cite all baselines** - provide citations for every baseline method mentioned
- [ ] **Explain new concepts** - ensure any new concept has explanation or proper reference
- [ ] **Past tense for authors, present for methods** - "Smith et al. proposed X" (past) but "Method X uses Y" (present)
- [ ] **Multiple citations for broad claims** - when saying "approaches do X", cite multiple papers, not just one

### ✅ **Content Selection & Focus**
- [ ] **Discuss only related work** - only include works directly related to your primary task; avoid tangentially related areas unless necessary
- [ ] **Justify foundational topics** - if discussing broader areas (e.g., constraint satisfaction for a floorplan paper), explain why it's relevant
- [ ] **Move distant connections to supplementary** - topics like program synthesis that have only philosophical connections should go to supplementary, not main Related Work
- [ ] **Selective literature coverage** - Related Work is not a laundry list; it's about contextualizing your contribution
- [ ] **Avoid overly broad discussions** - don't discuss entire research areas unless they directly inform your approach

### ✅ **Compatibility & Dataset Discussion**
- [ ] **Consider section placement** - if discussing dataset compatibility issues, consider making it a separate small section rather than embedding in Related Work
- [ ] **Delegate details to supplementary** - keep only key points in main paper, move detailed compatibility analysis to supplementary
- [ ] **Keep it very concise** - if dataset compatibility is important but tangential, summarize in 1-2 paragraphs max in main paper

## 🛠️ Methodology Section

### ✅ **Section Structure & Flow**
- [ ] **Follow standard CVPR pattern** - structure should be: Related Work → (optional Data Positioning section) → Proposed Method
- [ ] **Integrate theory with method** - don't have a separate "Theoretical Foundations" section before Method; integrate theory into the method description
- [ ] **Method section structure** - within Method: (1) Problem Formalization, (2) Theoretical Foundations (with theorems), (3) Algorithm Description
- [ ] **Single problem formulation** - have exactly one problem formulation section/paragraph, not multiple scattered throughout
- [ ] **Theory-algorithm connection** - when describing algorithm, explicitly reference how theorems inform design decisions

###  **Problem Formulation**
- [ ] **Concrete problem definition** - create a dedicated "Problem Formulation" section
- [ ] **Mathematical formulation** where possible (use set notation, formal definitions)
- [ ] **Clear objective statement** - what exactly are you optimizing for?

### ✅ **Subsection Naming & Organization**
- [ ] **Align subsection names with figure** - subsections in Method should use the same names as modules/blocks in your schematics figure
- [ ] **Maintain consistent terminology** - if the figure says "Vision Pipeline", the subsection should be "Vision Pipeline", not "Vision Component"
- [ ] **Emphasize venue focus in structure** - for vision venues, present vision as core to the problem, not just a preprocessing step

###  **Modular Organization**
- [ ] **Treat method as collection of modules** (3-4 main modules, each with sub-components)
- [ ] **Color-code or visually organize** modules in methodology figure
- [ ] **Module-based section structure**: subsections for modules, sub-subsections for components within modules
- [ ] **Clear module objectives** - each module should have a well-defined purpose that contributes to overall goal

###  **Mathematical Rigor & Notation**
- [ ] **Use mathematical notation** to explain core functions where appropriate
- [ ] **Consistent notation** throughout the paper, refer back to problem formulation notation
- [ ] **Generic formulation** - use abstract notation (e.g., $\mathcal{D}$) instead of specific dataset names
- [ ] **Instantiation in experiments** - provide specific details about how abstract components are implemented

###  **Technical Completeness**
- [ ] **Don't skip details in first draft** - include more information initially, compress later
- [ ] **Comprehensive coverage** - ensure all important technical details are included
- [ ] **Method-figure alignment** - organize text flow to match the sequence in methodology figure
- [ ] **Concise technical specifications** - keep environment details (GPU/batch size/code file name) brief as they're not the research focus

### ✅ **Algorithm Reproducibility** ⚠️ CRITICAL
- [ ] **Reproducibility test** - give method section to a colleague; can they implement it from the paper alone?
- [ ] **Training procedure fully specified**:
  - Loss functions defined with equations
  - Optimization algorithm stated (e.g., Adam, SGD)
  - Learning rates & schedules given
  - Convergence criteria specified
- [ ] **All hyperparameters documented** - in main paper or appendix with justification or ablation
- [ ] **Pseudocode or algorithm box** - include formal algorithm description for complex methods

### ✅ **Mode/Variant Discussion**
- [ ] **Delegate to supplementary if high-level** - if discussing different modes (lightweight, full, oracle), consider moving detailed discussion to supplementary
- [ ] **Focus on core algorithm** - main method section should describe the primary algorithm and its components
- [ ] **Remove unimplemented future work** - if something is "Future Work" or not implemented, remove it entirely from the paper
- [ ] **Keep one implementation approach** - unless variants are a core contribution, focus on what you actually implemented and tested

### ✅ **Implementation Details**
- [ ] **Consider supplementary placement** - if implementation details are extensive, move them to supplementary material
- [ ] **Keep method section focused** - prioritize algorithm description, theoretical properties, and key design decisions in main text

###  **Theorem & Mathematical Proofs**
- [ ] **Limit theorems to 1-2** - keep only essential theorems in main text that deliver strong basis, move others to appendix
- [ ] **Proofs placement** - keep theorems in main text but move proofs to supplementary/appendix to save space
- [ ] **Reference theorems near their statement** - ideally in the same Method section where stated
- [ ] **Provide proofs** - include proofs for all stated theorems (main text or appendix)
- [ ] **Theorem relevance** - ensure each theorem directly supports your main contribution

### ✅ **Mathematical Correctness** ⚠️ CRITICAL
- [ ] **Independent verification** - have a colleague verify all mathematical derivations, theorems, and equations
- [ ] **Percentage calculations verified** - use correct formula: (new - old) / old × 100, NOT (new - old) / new × 100
- [ ] **Metric ranges validated** - ensure all metrics respect their valid ranges:
  - Probabilities ∈ [0,1]
  - Percentages ∈ [0,100] or [-100,100]
  - Correlations ∈ [-1,1]
  - Accuracy/precision/recall ∈ [0,1] or [0,100]
- [ ] **Terminology correctness** - use precise mathematical language:
  - "Optimal" only with formal proof
  - "Converges" only with convergence proof
  - "First" only after exhaustive literature search
  - "Guaranteed" only with theoretical backing

## 🧪 Experimental Validation

### ✅ **Experimental Setup Documentation**
- [ ] **Cite all datasets** - provide citations for every dataset used in evaluation
- [ ] **Cite all baselines** - provide citations for every baseline method mentioned
- [ ] **Explain metric choice** - if using standard metrics, say "we use standard metrics [cite]" and explain any additional custom metrics
- [ ] **Justify custom metrics** - if introducing new metrics, explain why they're needed beyond standard ones

### ✅ **Experimental Rigor & Statistical Testing** ⚠️ CRITICAL
- [ ] **Multiple datasets/benchmarks** - test on minimum 3 different datasets or benchmarks
- [ ] **Multiple random seeds** - run experiments with minimum 3-5 different random seeds
- [ ] **Error bars or confidence intervals** - report uncertainty on ALL quantitative results
- [ ] **Statistical significance testing** - use appropriate tests (t-test, Wilcoxon, etc.)
  - → See `REF_statistical_rigor.md` for choosing the right test, effect sizes, and reporting templates
- [ ] **Cross-validation or proper train/val/test splits** - avoid data leakage and overfitting
- [ ] **All claimed improvements must be tested** - don't claim improvements you haven't measured
- [ ] **Multiple evaluation dimensions** if multiple benefits are claimed
- [ ] **Ablation for each component** - systematically test the contribution of each proposed component

### ✅ **Writing Efficiency & Redundancy**
- [ ] **Eliminate table caption redundancy** - don't repeat detailed results from tables in the running text; either discuss high-level insights or refer to the table
- [ ] **Strategic sub-text usage** - table/figure sub-captions should add context, not duplicate what's in the main text
- [ ] **Single discussion per result** - each result should be discussed once in the best location (either in text or caption), not both
- [ ] **Cross-reference without repeating** - you can say "Table X shows..." to direct attention without repeating all numbers

### ✅ **Baseline Evaluation in Experiments**
*Note: Baseline identification strategy is in "Pre-Research Definition" section above*

- [ ] **Multi-category baseline coverage** - ensure implementation covers all baseline categories identified during research planning
- [ ] **Baseline comparison table** - create a structured comparison showing what each baseline addresses and doesn't address
- [ ] **Novelty gap articulation** - explicitly show what gap your work fills that no baseline covers
- [ ] **Fair evaluation protocol** - ensure all methods are evaluated on the same metrics and datasets
- [ ] **Baseline limitations analysis** - discuss both strengths and weaknesses of each baseline honestly

### ✅ **Generic Framework Validation**
- [ ] **Dataset generalization** - if using abstract notation, test on multiple datasets
- [ ] **Framework flexibility** - show that your approach works beyond the specific instantiation

### ✅ **Ablation Studies & Pattern Analysis**
- [ ] **Unified ablation section** - if ablation studies appear in both experiments and results, combine into one dedicated section
- [ ] **Qualitative comparison patterns** - ensure qualitative comparisons clearly show identifiable patterns and trends
- [ ] **Component impact visualization** - show clear visual evidence of how different components affect performance

## ✍️ General Writing Principles

### ✅ **Draft Strategy**
- [ ] **Write detailed first draft** - don't worry about length limits initially
- [ ] **Compression in revision** - best refinement comes from thoughtful compression of complete content
- [ ] **8 pages → 7 pages is fine** for initial drafts - completeness over conciseness initially

### ✅ **Reviewer Perspective**
- [ ] **Anticipate reviewer expectations** - if you claim X, Y, Z improvements, reviewers will look for X, Y, Z experiments
- [ ] **Self-audit claims** - every claim should have supporting evidence planned
- [ ] **Clear contribution articulation** - make it easy for reviewers to understand your contributions

### ✅ **Results Writing Style**
- [ ] **Lead with method ownership** - write "our results show that..." instead of "Figure 1 shows that..."
- [ ] **Active voice for findings** - emphasize your method's achievements rather than passive figure descriptions
- [ ] **Connect results to claims** - explicitly link experimental results back to introduction claims

## 📐 **Figures, Tables & Visual Elements**

### ✅ **Figure Quality & Design**
- [ ] **Professional figures** with legends, proper captions, error bars
- [ ] **Multiple experimental runs** for key results
- [ ] **Visual organization** that supports the textual organization (color coding, module grouping)
- [ ] **Eye-friendly color schemes** - use industry-standard, accessible colors for any color-coded elements
- [ ] **Large, readable text** - ensure text in charts and tables is sufficiently large for readability
- [ ] **Vector format preferred** - all figures should be vector format (PDF) with readable fonts
- [ ] **Annotations and visual enhancement** - add annotations, images, and visual elements to make figures more engaging
- [ ] **Computer vision specific visuals** - include sample images, visual comparisons, and annotated examples for CV research

### ✅ **Tables & Data Presentation**
- [ ] **Remove tiny confidence intervals** - if CI values are very small (close to zero), remove to save space
  - → See `REF_statistical_rigor.md` for proper CI calculation and reporting
- [ ] **Table clarity** - ensure all table elements are clearly labeled and explained
- [ ] **Space efficiency** - optimize table formatting for maximum information density
- [ ] **Hyperparameter tables** - create dedicated tables for key parameters (epochs, batch size, learning rates)
- [ ] **Visual engagement** - make tables more visual and engaging, especially for computer vision research

### ✅ **Strategic Visual Elements - Method Section**
- [ ] **Module-flow diagrams** - small diagrams showing information flow between method components
- [ ] **Complexity progression examples** - show how method handles different complexity levels
- [ ] **Bias-mitigation illustration** (if applicable) - before/after comparison

### ✅ **Strategic Visual Elements - Experiments Section**
- [ ] **Hyperparameter summary table**
- [ ] **Dataset distribution visualization** (pie/bar chart)

### ✅ **Strategic Visual Elements - Results Section**
- [ ] **Ablation visualizations** - bar charts or plots showing impact of different components
- [ ] **Qualitative success/failure grids** - side-by-side comparisons showing method improvements
- [ ] **Data efficiency plots** - line plots showing performance vs. training data amount
- [ ] **Computation vs. quality trade-offs** - scatter plots showing efficiency benefits

### ✅ **Visual Elements Integration**
- [ ] **Figure density** - appropriate number of visuals for paper length (3-4 key figures for 7-8 page paper)
- [ ] **Visual narrative** - figures tell a coherent story that supports the text
- [ ] **Space optimization** - visuals use space efficiently (`\columnwidth` vs `figure*`)
- [ ] **Annotated visualizations** - add clear annotations to before/after comparisons and violation/correction figures

## 📐 **Formatting & Presentation**

###  **Text Organization & Flow**
- [ ] **Strategic bullet point usage** - avoid excessive bullets; combine related points into paragraphs
- [ ] **Bullet point purpose** - only use bullets when doing something special with each point
- [ ] **Paragraph flow** - ensure smooth transitions between concepts and sections
- [ ] **Section balance** - avoid having too many subsections with only bullet points
- [ ] **Combine related paragraphs** - if two short paragraphs are adjacent and related, merge into one
- [ ] **Space-saving formatting** - use paragraph spacing reduction when needed to meet length requirements

###  **LaTeX Formatting Optimization**
- [ ] **Use indent bold strategically** - apply `\indent\textbf{}` where appropriate to save space
- [ ] **Spacing adjustments** - reduce spacing between paragraphs when necessary for length constraints
- [ ] **Format efficiency** - optimize LaTeX commands for maximum space utilization

## 🎯 Pre-Submission Final Check

### ✅ **Number Consistency Audit** ⚠️ CRITICAL
- [ ] **Cross-section number verification** - ensure identical numbers appear in Abstract, Introduction, and Results:
  - Same improvement percentages
  - Same baseline scores
  - Same statistical significance values
- [ ] **Table/figure reference accuracy** - verify all in-text references to tables/figures cite the correct numbers
- [ ] **"Best" result consistency** - ensure claimed "best" results remain consistent throughout paper
- [ ] **Manual calculation check** - use a calculator to verify 3-5 random improvement calculations
- [ ] **Ctrl+F audit** - search for each key metric value and verify consistency across all mentions

###  **Claim-Evidence Audit**
- [ ] **Every claim has support** - go through introduction and verify each claim has experimental backing
- [ ] **Method completeness** - ensure no important technical details are missing
- [ ] **Mathematical consistency** - check that notation is used consistently throughout
- [ ] **Reference completeness** - all statements that need citations have them

###  **Structure Review**
- [ ] **Logical flow** from problem formulation → method modules → experiments
- [ ] **Figure-text alignment** - text organization matches visual organization
- [ ] **Modular clarity** - each method component has clear purpose and contribution

###  **Content Quality Verification**
- [ ] **Novelty assessment** - verify that your contributions are clearly novel and distinguish them from prior work
- [ ] **Rigor verification** - ensure all theoretical claims have proofs, experiments use multiple seeds with confidence intervals
- [ ] **Clarity check** - confirm clear problem statement and transparent discussion of limitations
- [ ] **Positioning strength** - verify all contribution claims are backed by concrete evidence

###  **Accessibility & Self-Containment Audit**
- [ ] **Technical term definitions** - every specialized term is explained on first use
- [ ] **Assumption verification** - no unstated assumptions about reader's background knowledge
- [ ] **Progressive complexity** - concepts build logically from simple to complex
- [ ] **Grandmother test compliance** - non-expert could follow the main narrative

###  **Technical Compilation & Formatting**
- [ ] **LaTeX compilation** - compile document and fix all compilation errors
- [ ] **Citation resolution** - verify all citations resolve correctly with no undefined references
- [ ] **Cross-references** - check all internal references (sections, figures, tables, equations) work correctly
- [ ] **Supplementary references** - verify references between main paper and supplementary material are correct
- [ ] **Bibliography completeness** - ensure all cited works are in bibliography and properly formatted

###  **Final Proofreading**
- [ ] **Typo sweep** - read through entire paper (including abstract, captions, and supplementary) for typos
- [ ] **Abstract-contribution alignment** - verify abstract accurately reflects the contributions listed in introduction
- [ ] **Consistency check** - ensure terminology and notation are used consistently throughout

###  **Anonymity & Publication Standards**
- [ ] **Author anonymization** - verify paper is in review mode with no author information
- [ ] **Remove institutional references** - remove any mention of specific institutions for anonymity
- [ ] **Anonymize technical environment** - keep technical specifications generic and concise
- [ ] **Conference compliance** - ensure all formatting follows target conference guidelines
- [ ] **Reference anonymization** - ensure self-citations and institutional references are properly anonymized

###  **Reviewer Preparedness**
- [ ] **Anticipate critical questions** - prepare written responses to potential reviewer concerns
- [ ] **Address limitations proactively** - transparently discuss limitations in paper to preempt reviewer criticism
- [ ] **Justify design choices** - have clear rationale ready for why you made specific methodological choices
- [ ] **Explain missing comparisons** - if unable to compare with certain baselines, document reasons clearly
- [ ] **Quantify claims** - back up qualitative statements with quantitative evidence wherever possible

### ✅ **Hostile Reviewer Test** ⚠️ CRITICAL
*Read your paper assuming the reviewer wants to reject it*
- [ ] **Flaw-seeking mindset** - reviewer actively wants to find problems
- [ ] **Math verification assumption** - reviewer will check your mathematical derivations
- [ ] **Baseline gap detection** - reviewer will notice missing baselines and comparisons
- [ ] **Reproducibility attempt** - reviewer will try to reproduce your results from the paper
- [ ] **Citation verification** - reviewer will verify your claims about related work are accurate
- [ ] **Write vulnerability statement** - identify the #1 weakness a hostile reviewer would attack, then fix it

### ✅ **Quick Google Scholar Test**
- [ ] **5 keyword variations searched** - search your problem using 5 different keyword combinations
- [ ] **First 2 pages checked** - review first 2 pages of results for each search
- [ ] **Last 2 years verified** - ensure all relevant papers from last 24 months are cited
- [ ] **Recent arXiv check** - check arXiv for papers from last 3 months
- [ ] **Missing paper justification** - if you're not comparing to a recent relevant paper, document why

### ✅ **Final Sign-Off** ⚠️ DO NOT SUBMIT UNLESS ALL TRUE
- [ ] **I can defend every claim with evidence** - no unsupported statements remain
- [ ] **Someone could reproduce this work** - complete algorithm and experimental details provided
- [ ] **I've compared against recent, relevant work** - comprehensive baseline coverage
- [ ] **All numbers have been double-checked** - consistency verified across all sections
- [ ] **A skeptical reviewer would struggle to find obvious flaws** - major vulnerabilities addressed

---

## 📊 **Rejection Statistics to Remember**

Based on analysis of 1000+ paper rejections:
- **40%** rejected for incomplete method description → Focus on reproducibility and algorithm completeness
- **25%** rejected for missing baselines → Ensure comprehensive related work and fair comparisons
- **20%** rejected for mathematical/statistical errors → Have someone verify your math and calculations
- **10%** rejected for overclaiming/unsupported statements → Ensure every claim has evidence
- **5%** rejected for other reasons (presentation, writing quality, scope mismatch)

**Prioritize your effort on the top 3 categories to avoid 85% of rejections.**

---

## 🚨 **Emergency Fixes (If Deadline is Close)**

If you discover issues close to deadline, prioritize these quick fixes:

### Missing algorithm details (30-60 min):
- Add algorithm box with pseudocode
- Create supplementary with full implementation details

### Missing baselines (1-2 hours):
- Add table comparing to published numbers from recent papers
- Add discussion of why certain baselines aren't directly comparable

### Missing error bars (few hours to days):
- Re-run key experiments with minimum 3 seeds
- If no time: acknowledge as limitation and promise in camera-ready

### Math might be wrong (1-2 hours):
- Have colleague check NOW before submission
- Double-check percentage calculations and metric ranges

### Numbers inconsistent (30 min):
- Ctrl+F every key number and create consistency table
- Update abstract/intro to match results section

---

## 📝 **Post-Rejection: Learn and Improve**

If your paper gets rejected:
- **Don't panic** - most papers get rejected on first submission
- **Analyze systematically** - use structured approach to understand issues
- **Track patterns** - identify recurring problems across reviews
- **Create action plan** - prioritize fixes by impact and effort
- **Resubmit strategically** - choose venue that better matches your contribution

*Consider using a rejection analysis template to systematically address reviewer concerns and plan resubmission strategy.*

---

## 📋 **Time Allocation for Checklist**

### Research Planning Phase (use this BEFORE experiments)
- **Pre-Research Definition Checklist**: 2-4 hours (save months of directionless work)
- **Baseline identification & mapping**: 4-8 hours (comprehensive literature review)
- **Problem formulation clarity**: 2-3 hours (document outputs, formats, applications)

### Writing Phase (use during paper writing)
- **First draft writing**: Use relevant sections as you write
- **Pre-submission review**: 2-4 hours for complete checklist
- **Critical items only** (marked ⚠️ CRITICAL): 30-60 minutes minimum
- **Emergency pre-deadline check**: Focus on Fatal Flaws and Number Consistency (30 minutes)

### Key Insight: Research Planning vs. Paper Writing

Most rejection-causing issues originate in research planning, not paper writing:

| Principle | When to Apply | Prevents |
|-----------|---------------|----------|
| Ultimate objective clarity | Research design phase | Ambiguous evaluation metrics |
| Output modality specificity | Problem formulation phase | Inappropriate technical choices |
| Application-driven framework | Project inception phase | Lack of motivation/impact |
| Mapping to established areas | Literature review phase | Poor positioning/venue mismatch |
| Baseline identification | Experiment design phase | Missing comparisons (25% of rejections) |

**⚠️ Use this checklist as a research planning tool, not just a writing guide.**

---

## 💡 **Final Reminder**

*The goal is completeness first, then compression through revision. Better to have a thorough 8-page draft that gets compressed to 7 pages than a sparse 6-page draft that lacks crucial details.*

*Updated: November 2025* 