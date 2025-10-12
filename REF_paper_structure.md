# Paper Structure Reference
## Standard Structure & Page Allocations

---

## 🎯 **WHEN TO USE THIS GUIDE**

### **Critical Moments:**
- ✅ **Day 1 of writing** - Choose structure based on target conference
- ✅ **Over page limit** - Check allocations to see what can be compressed
- ✅ **Organizing sections** - Use standard subsection patterns
- ✅ **Deciding figure placement** - See typical figure locations
- ✅ **Formatting questions** - Conference-specific requirements

### **How to Use:**
1. **Section 1**: Find your conference structure (CVPR, NeurIPS, ACL, etc.)
2. **Section 2**: Check typical page allocations (Method=35%, Experiments=28%)
3. **Section 3**: Copy structure template as your outline
4. **Section 4**: Reference during writing to keep proportions balanced

### **Quick Example:**
```
CVPR Paper (8 pages):
- Method: 2.5-3 pages (35%) ← Don't shortchange this!
- Experiments: 2-2.5 pages (28%)
- Introduction: 1-1.5 pages (15%)

If over limit: Compress intro/related work, NOT method completeness
```

---

## 📏 TYPICAL PAGE ALLOCATION (8-page paper)

| Section | Pages | Percentage |
|---------|-------|------------|
| Abstract | 0.15 | 2% |
| Introduction | 1.0-1.5 | 15% |
| Related Work | 0.75-1.0 | 12% |
| Method | 2.5-3.0 | 35% |
| Experiments | 2.0-2.5 | 28% |
| Conclusion | 0.25 | 3% |
| References | 0.5-1.0 | 5-8% |

*Adjust based on paper type: theory-heavy → more method, empirical → more experiments*

---

## 📝 STRUCTURE BY CONFERENCE

### CVPR/ICCV/ECCV (Computer Vision)
```
1. Abstract
2. Introduction
3. Related Work
4. Method
   4.1 Problem Formulation
   4.2 Approach Overview
   4.3 Technical Details
5. Experiments
   5.1 Setup
   5.2 Results
   5.3 Ablation Study
6. Conclusion
```

### NeurIPS/ICML (Machine Learning)
```
1. Abstract
2. Introduction
3. Background/Preliminaries
4. Method
   4.1 Problem Setting
   4.2 Proposed Algorithm
   4.3 Theoretical Analysis
5. Experiments
6. Related Work  ← Often after experiments
7. Conclusion
```

### ACL/EMNLP (NLP)
```
1. Abstract
2. Introduction
3. Related Work
4. Task Definition
5. Model
   5.1 Architecture
   5.2 Training
6. Experimental Setup
7. Results and Analysis
8. Conclusion
```

### AAAI/IJCAI (AI General)
```
1. Abstract
2. Introduction
3. Related Work
4. Preliminaries
5. Methodology
6. Experiments
7. Discussion
8. Conclusion
```

---

## 🏗️ SECTION STRUCTURES

### Abstract (150-250 words)
```
1. Context (1 sentence)
2. Problem (1-2 sentences)
3. Solution (2-3 sentences)
4. Results (2-3 sentences)
5. Impact (1 sentence)
```

### Introduction (4-6 paragraphs)
```
¶1: Problem context & importance
¶2: Current approaches & limitations
¶3: Key insight/approach
¶4: Technical overview
¶5: Contributions (bulleted)
¶6: Paper organization
```

### Related Work (3-4 subsections)
```
- Directly Competing Methods
- Foundation Techniques
- Adjacent/Inspiring Work
- Position Summary
```

### Method (Flexible)
```
- Overview Figure (always first)
- Problem Formulation
- Core Algorithm
- Implementation Details
- Theoretical Properties (if applicable)
```

### Experiments
```
- Experimental Setup
  - Datasets
  - Baselines
  - Metrics
  - Implementation
- Main Results
- Ablation Studies
- Additional Analysis
  - Qualitative Results
  - Failure Cases
  - Computational Cost
```

### Conclusion (2-3 paragraphs)
```
¶1: Summary of contributions
¶2: Key findings
¶3: Future work/Impact
```

---

## 📊 STANDARD ELEMENTS

### Required Figures/Tables

| Element | Typical Placement | Purpose |
|---------|------------------|---------|
| Method Overview | First page of Method | Visual algorithm summary |
| Main Results Table | First in Results | Performance comparison |
| Ablation Table/Figure | After main results | Component analysis |
| Qualitative Figure | End of Results | Visual examples |

### Standard Supplementary Structure
```
A. Additional Results
B. Implementation Details
C. Proofs
D. Extended Related Work
E. Additional Visualizations
F. Failure Cases
G. Hyperparameter Settings
```

---

## 🎯 STRUCTURE BY PAPER TYPE

### Empirical Paper
```
Light theory (0.5 pages)
Heavy experiments (3+ pages)
Multiple datasets
Extensive ablations
```

### Theoretical Paper
```
Heavy preliminaries (1+ page)
Detailed proofs (1-2 pages)
Lighter experiments (1.5-2 pages)
Focus on verification
```

### Systems Paper
```
Architecture details (1+ page)
Implementation focus
Efficiency analysis
Scalability studies
```

### Application Paper
```
Domain background (0.5 page)
Practical constraints
Real-world evaluation
Deployment discussion
```

---

## 📐 FORMATTING SPECIFICATIONS

### Two-Column Format (Most CV/ML)
- Column width: ~3.25 inches
- Figures: `\columnwidth` or `\textwidth`
- Tables: Consider `table*` for wide tables

### Single-Column (Some conferences)
- Full width: ~6.5 inches
- More space but same content

### Common Elements
```latex
\begin{figure}[t]  % Top of column
\begin{figure*}[t] % Full width, top
\begin{table}[h]   % Here if possible
\begin{algorithm}  % For pseudocode
```

---

## ⚡ QUICK DECISIONS

### Where to Put Related Work?
- **Before Method**: If establishing context is crucial
- **After Method**: If method is novel/complex (NeurIPS style)
- **Split**: Brief in intro, detailed later

### How Many Subsections?
- **Introduction**: Usually none
- **Related Work**: 2-4 subsections
- **Method**: 3-5 subsections
- **Experiments**: 3-4 subsections

### Figure Placement Priority
1. First page (teaser) if very compelling
2. Method section for overview
3. Results for comparison
4. Throughout for clarity

---

## 📋 SPACE-SAVING TIPS

### When Over Page Limit
1. Move proofs to appendix
2. Combine related work paragraphs
3. Use `\vspace{-Xmm}` carefully
4. Reduce figure sizes (maintain readability)
5. Use subcaptions for related figures

### Never Compromise On
- Method completeness
- Main results table
- Core contribution clarity
- Reference completeness

---

## 🎨 VISUAL HIERARCHY

### Title & Headers
```
Title: 14-17pt
Section: 12pt bold
Subsection: 11pt bold
Subsubsection: 10pt italic
```

### Standard Spacing
- After title: 12pt
- Before section: 12pt
- After section: 6pt
- Between paragraphs: 0-6pt

---

*This is structure only. For content guidance, see paper writing checklists.*
