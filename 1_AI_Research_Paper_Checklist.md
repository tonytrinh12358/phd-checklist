# AI Research Paper Writing Checklist
*Based on expert supervisor feedback - Use this checklist for all future AI research papers*

## 📚 **Quick Reference to Other Tools**
- → **Paper structure & page allocation**: See `REF_paper_structure.md`
- → **Statistical tests & reporting**: See `REF_statistical_rigor.md`
- → **Fatal flaws to avoid**: See `2_FATAL_FLAWS_CHECKLIST.md` before submission

## 🎯 **Core Writing Philosophy**

### ✅ **Self-Contained & Accessible Writing**
- [ ] **"Grandmother test"** - write so someone with no prior knowledge can understand (except theorems)
- [ ] **Define all technical terms** - explain every acronym, method name, or technical concept on first use
- [ ] **Avoid jargon without explanation** - if you use terms like "Align Only", "Quality Only", explain what they mean
- [ ] **Progressive complexity** - introduce simple concepts before building to complex ones

## 🧭 **Problem Definition & Research Positioning**
*Critical foundation questions to answer before diving into technical details*

### ✅ **Ultimate Objective Clarity**
- [ ] **Specify the final output format** - be crystal clear about what you're generating (2D/3D, vector/raster, images/scenes/layouts)
- [ ] **Output modality specificity** - don't leave ambiguity about the type of output (e.g., "floorplans" could mean rendered images, CAD files, or vector drawings - specify which)
- [ ] **Primary vs. secondary outputs** - distinguish between core contributions and optional extensions
- [ ] **Format justification** - explain why the chosen output format is appropriate for your problem (e.g., vectors for precision, 3D for realism)

### ✅ **Application-Driven Research Framework**
- [ ] **Work backwards from application** - start with the real-world use case and derive research questions from it
- [ ] **Concrete problem statement** - articulate the problem from the user/practitioner perspective first
- [ ] **Research question derivation** - explicitly show how research questions emerge from the application need
- [ ] **Bridge application to research** - connect practical requirements to technical challenges and contributions
- [ ] **Real-world validation context** - consider how your solution would be evaluated or deployed in practice

### ✅ **Mapping to Established Research Areas**
- [ ] **Identify related problem domains** - map your work to 2-3 established research communities (e.g., constrained generation, layout synthesis, program synthesis)
- [ ] **Position within landscape** - show where your work sits relative to existing research areas
- [ ] **Highlight novel intersection** - articulate what makes your combination of areas novel or underexplored
- [ ] **Cross-community appeal** - frame contributions to be valuable to multiple research communities
- [ ] **Reference canonical works** - cite seminal papers from each relevant research area to establish context

### ✅ **Baseline Identification Strategy**
- [ ] **"There will always be a baseline"** - identify all relevant baselines early in research planning
- [ ] **Multiple baseline categories** - consider baselines from different angles (direct competitors, adjacent methods, naive approaches)
- [ ] **Baseline gaps analysis** - explicitly identify what existing baselines DON'T address that your work does
- [ ] **Fair comparison protocol** - ensure baselines are evaluated on the same criteria as your method
- [ ] **Baseline strengths acknowledgment** - honestly present what each baseline does well, not just their limitations

## 📝 Introduction Section

### ✅ **Supporting Evidence & References**
- [ ] **Cite supporting papers** for all major arguments, especially in opening paragraphs
- [ ] **Back claims with evidence** - if you claim existing approaches have problems, show qualitative examples
- [ ] **Include variance analysis** in key figures (run experiments multiple times with different seeds)
- [ ] **Comprehensive figure legends** and detailed captions for all figures

### ✅ **Method Overview & Technical Details**
- [ ] **Explain "HOW" not just "WHAT"** - don't just say what your method introduces, explain how it achieves it
- [ ] **Include technical components** (e.g., LLM, Diffusion, DPO/SFT) with appropriate references
- [ ] **Map claims to experiments** - every performance claim in intro should have corresponding experimental validation planned

### ✅ **Claims Validation Strategy**
- [ ] **Qualitative evidence** for comparative claims (show where existing methods fail vs. your approach succeeds)
- [ ] **Comprehensive evaluation metrics** - if claiming improvements in multiple dimensions, plan experiments for all of them
- [ ] **Avoid unsupported claims** - only claim what you can experimentally validate

## 🔗 Related Work Section

### ✅ **Citation Best Practices**
- [ ] **Use appropriate citation formats**: `\citet` for in-text author mentions, `\cite` for parenthetical citations
- [ ] **Remove redundant author names** by choosing correct citation commands
- [ ] **Follow conference styling** for references and formatting requirements
- [ ] **Explain new concepts** - ensure any new concept has explanation or proper reference

## 🛠️ Methodology Section

### ✅ **Problem Formulation**
- [ ] **Concrete problem definition** - create a dedicated "Problem Formulation" section
- [ ] **Mathematical formulation** where possible (use set notation, formal definitions)
- [ ] **Clear objective statement** - what exactly are you optimizing for?

### ✅ **Modular Organization**
- [ ] **Treat method as collection of modules** (3-4 main modules, each with sub-components)
- [ ] **Color-code or visually organize** modules in methodology figure
- [ ] **Module-based section structure**: subsections for modules, sub-subsections for components within modules
- [ ] **Clear module objectives** - each module should have a well-defined purpose that contributes to overall goal

### ✅ **Mathematical Rigor & Notation**
- [ ] **Use mathematical notation** to explain core functions where appropriate
- [ ] **Consistent notation** throughout the paper, refer back to problem formulation notation
- [ ] **Generic formulation** - use abstract notation (e.g., $\mathcal{D}$) instead of specific dataset names
- [ ] **Instantiation in experiments** - provide specific details about how abstract components are implemented

### ✅ **Technical Completeness**
- [ ] **Don't skip details in first draft** - include more information initially, compress later
- [ ] **Comprehensive coverage** - ensure all important technical details are included
- [ ] **Method-figure alignment** - organize text flow to match the sequence in methodology figure
- [ ] **Concise technical specifications** - keep environment details (GPU/batch size/code file name) brief as they're not the research focus

### ✅ **Theorem & Mathematical Proofs**
- [ ] **Limit theorems to 1-2** - keep only essential theorems in main text that deliver strong basis, move others to appendix
- [ ] **Move proofs to appendix** - if there are many theorems, move all proofs to appendix for space efficiency
- [ ] **Reference theorems near their statement** - ideally in the same Method section where stated
- [ ] **Provide proofs** - include proofs for all stated theorems (main text or appendix)
- [ ] **Theorem relevance** - ensure each theorem directly supports your main contribution

## 🧪 Experimental Validation

### ✅ **Comprehensive Evaluation**
- [ ] **All claimed improvements must be tested** - don't claim improvements you haven't measured
- [ ] **Multiple evaluation dimensions** if multiple benefits are claimed
- [ ] **Statistical significance** - include error bars, multiple runs, proper statistical testing
  - → See `REF_statistical_rigor.md` for test selection, effect sizes, and reporting templates

### ✅ **Comprehensive Baseline Strategy**
- [ ] **Multi-category baseline coverage** - include baselines from different research angles:
  - Direct competitors (methods solving the same problem)
  - Adjacent methods (related techniques from neighboring domains)
  - Ablation baselines (your method with components removed)
  - Simple baselines (naive approaches to establish lower bounds)
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

### ✅ **Figure & Visual Quality**
- [ ] **Professional figures** with legends, proper captions, error bars
- [ ] **Multiple experimental runs** for key results
- [ ] **Visual organization** that supports the textual organization (color coding, module grouping)

## 📐 **Formatting & Presentation**

### ✅ **Text Organization & Flow**
- [ ] **Strategic bullet point usage** - avoid excessive bullets; combine related points into paragraphs
- [ ] **Bullet point purpose** - only use bullets when doing something special with each point
- [ ] **Paragraph flow** - ensure smooth transitions between concepts and sections
- [ ] **Section balance** - avoid having too many subsections with only bullet points
- [ ] **Combine related paragraphs** - if two short paragraphs are adjacent and related, merge into one
- [ ] **Space-saving formatting** - use paragraph spacing reduction when needed to meet length requirements

### ✅ **LaTeX Formatting Optimization**
- [ ] **Use indent bold strategically** - apply `\indent\textbf{}` where appropriate to save space
- [ ] **Spacing adjustments** - reduce spacing between paragraphs when necessary for length constraints
- [ ] **Format efficiency** - optimize LaTeX commands for maximum space utilization

### ✅ **Tables & Data Presentation**
- [ ] **Remove tiny confidence intervals** - if CI values are very small (close to zero), remove to save space
  - → See `REF_statistical_rigor.md` for proper CI calculation and reporting
- [ ] **Table clarity** - ensure all table elements are clearly labeled and explained
- [ ] **Space efficiency** - optimize table formatting for maximum information density
- [ ] **Hyperparameter tables** - create dedicated tables for key parameters (epochs, batch size, learning rates)
- [ ] **Large, readable text** - ensure text in charts and tables is sufficiently large for readability
- [ ] **Visual engagement** - make tables more visual and engaging, especially for computer vision research

### ✅ **Strategic Visual Elements** 
- [ ] **Module-flow diagrams** - small diagrams showing information flow between method components
- [ ] **Complexity progression examples** - show how method handles different complexity levels
- [ ] **Ablation visualizations** - bar charts or plots showing impact of different components
- [ ] **Qualitative success/failure grids** - side-by-side comparisons showing method improvements
- [ ] **Data efficiency plots** - line plots showing performance vs. training data amount
- [ ] **Computation vs. quality trade-offs** - scatter plots showing efficiency benefits
- [ ] **Eye-friendly color schemes** - use industry-standard, accessible colors for any color-coded elements
- [ ] **Annotations and visual enhancement** - add annotations, images, and visual elements to make figures more engaging
- [ ] **Computer vision specific visuals** - include sample images, visual comparisons, and annotated examples for CV research
- [ ] **Large figure text** - ensure all text in figures and charts is appropriately sized and readable

## 🎯 Pre-Submission Final Check

### ✅ **Claim-Evidence Audit**
- [ ] **Every claim has support** - go through introduction and verify each claim has experimental backing
- [ ] **Method completeness** - ensure no important technical details are missing
- [ ] **Mathematical consistency** - check that notation is used consistently throughout
- [ ] **Reference completeness** - all statements that need citations have them

### ✅ **Structure Review**
- [ ] **Logical flow** from problem formulation → method modules → experiments
- [ ] **Figure-text alignment** - text organization matches visual organization
- [ ] **Modular clarity** - each method component has clear purpose and contribution

### ✅ **Accessibility & Self-Containment Audit**
- [ ] **Technical term definitions** - every specialized term is explained on first use
- [ ] **Assumption verification** - no unstated assumptions about reader's background knowledge
- [ ] **Progressive complexity** - concepts build logically from simple to complex
- [ ] **Grandmother test compliance** - non-expert could follow the main narrative

### ✅ **Visual Elements Integration**
- [ ] **Figure density** - appropriate number of visuals for paper length (3-4 key figures for 7-8 page paper)
- [ ] **Visual narrative** - figures tell a coherent story that supports the text
- [ ] **Space optimization** - visuals use space efficiently (`\columnwidth` vs `figure*`)
- [ ] **Quality standards** - all figures are vector format (PDF) with readable fonts

### ✅ **Anonymity & Publication Standards**
- [ ] **Remove institutional references** - remove any mention of specific institutions (e.g., Spartan, University of Melbourne) for anonymity
- [ ] **Anonymize technical environment** - keep technical specifications generic and concise
- [ ] **Conference compliance** - ensure all formatting follows target conference guidelines
- [ ] **Reference anonymization** - ensure self-citations and institutional references are properly anonymized

---

## 📋 **Quick Visual Elements Checklist**
*Based on the "shopping list" approach - choose 3-4 high-impact visuals:*

**METHOD SECTION:**
- [ ] Module-flow diagram (information flow overview)
- [ ] Complexity-ladder examples (basic → intermediate → advanced)
- [ ] Bias-mitigation illustration (before/after comparison)

**EXPERIMENTS SECTION:**
- [ ] Hyperparameter summary table
- [ ] Dataset distribution visualization (pie/bar chart)

**RESULTS SECTION:**
- [ ] Ablation bar chart (component impact)
- [ ] Data-efficiency line plot (performance vs. training data)
- [ ] Qualitative failure/success grid (visual comparisons)
- [ ] Computation vs. quality scatter plot (efficiency message)

---

*Remember: The goal is completeness first, then compression through revision. Better to have a thorough 8-page draft that gets compressed to 7 pages than a sparse 6-page draft that lacks crucial details.* 