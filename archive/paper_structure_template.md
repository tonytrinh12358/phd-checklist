# Research Paper Structure Template
## A Practical Guide to Avoid Common Rejection Reasons

---

## PAPER STRUCTURE WITH REQUIREMENTS

### 1. ABSTRACT (150-200 words)
Must include:
- [ ] Problem statement (1-2 sentences)
- [ ] Key technical approach (2-3 sentences)  
- [ ] Main contributions (2-3 bullet points)
- [ ] Quantitative results (2-3 key numbers with baselines)
- [ ] Data/code availability statement

**Avoid:**
- Vague claims ("significant improvements")
- Missing baseline comparisons
- Overclaiming ("first", "novel" without verification)

---

### 2. INTRODUCTION (1-1.5 pages)
Structure:
1. **Problem Context** (1 paragraph)
   - Why this problem matters
   - Current state and limitations

2. **Challenge Statement** (1 paragraph)
   - Specific technical challenges
   - Why existing solutions fail

3. **Approach Overview** (1-2 paragraphs)
   - High-level solution
   - Key technical insights
   - NO implementation details

4. **Contributions** (Bulleted list)
   - Be specific and measurable
   - Match what you actually deliver

5. **Paper Organization** (2-3 sentences)

---

### 3. RELATED WORK (1-1.5 pages)
Organize by:
- **Direct Competitors** (must be comprehensive)
  - Include last 2-3 years exhaustively
  - Explain why each is insufficient
  
- **Foundational Methods**
  - Credit original ideas
  - Show evolution to your work

- **Adjacent Fields**
  - Connect to broader context
  - Show interdisciplinary awareness

**Required Table**: Comparison of key methods with checkmarks for capabilities

---

### 4. PROBLEM FORMULATION (0.5-1 page)
Must include:
- [ ] Formal problem statement
- [ ] All notation definitions
- [ ] Assumptions (explicit list)
- [ ] Success metrics
- [ ] Scope boundaries

**Mathematical Requirements:**
- Every symbol defined before use
- Domains and ranges specified
- Consistency with later usage

---

### 5. METHOD (2-3 pages)
Structure:
1. **Overview Figure** (always include)
2. **Core Algorithm**
   - Complete pseudocode
   - Line-by-line explanation
   
3. **Technical Details**
   - How to handle non-differentiable objectives
   - Gradient computation/approximation
   - Training procedures
   
4. **Implementation Details**
   - Architecture specifics
   - Hyperparameters
   - Computational complexity

5. **Theoretical Analysis** (if applicable)
   - Formal theorems with proofs
   - Or clearly marked conjectures

**Required**: Someone should be able to implement from this section alone

---

### 6. EXPERIMENTS (2-3 pages)

#### 6.1 Experimental Setup
- **Datasets**: Description, size, splits, preprocessing
- **Baselines**: List with citations and configurations
- **Metrics**: Precise definitions and formulas
- **Implementation**: Framework, hardware, reproducibility details
- **Statistical Methods**: Tests, corrections, significance levels

#### 6.2 Main Results
- **Comprehensive Table**: All methods, all metrics
- **Statistical Significance**: Stars/symbols with legend
- **Multiple Datasets/Settings**: Show generalization

#### 6.3 Ablation Studies
- **Component Contribution**: Isolate each novel part
- **Design Validation**: Justify key choices
- **Sensitivity Analysis**: Robustness to hyperparameters

#### 6.4 Additional Analysis
- **Human Evaluation** (if applicable)
- **Failure Cases**: When method doesn't work
- **Computational Cost**: Time, memory, scaling
- **Qualitative Results**: Visual examples with analysis

---

### 7. RESULTS AND DISCUSSION (1-1.5 pages)
- **Key Findings**: What do results mean?
- **Comparison to Prior Work**: Explicit improvements
- **Limitations**: Be honest and specific
- **Future Directions**: Realistic next steps

---

### 8. CONCLUSION (1 paragraph)
- Summarize contributions
- Reiterate key results
- Broader impact

---

## SUPPLEMENTARY MATERIAL STRUCTURE

### Appendix A: Proofs
- All theoretical proofs
- Derivations
- Additional mathematical details

### Appendix B: Implementation Details
- Complete hyperparameter settings
- Training procedures
- Architecture diagrams

### Appendix C: Additional Results
- Extended tables
- More ablations
- Edge cases

### Appendix D: Dataset Details
- Collection procedures
- Annotation guidelines
- Statistics and distributions

---

## PRE-SUBMISSION CHECKLIST

### Technical Completeness
- [ ] Can someone reproduce from paper alone?
- [ ] All algorithms fully specified?
- [ ] All theorems proven or marked as conjectures?

### Experimental Rigor  
- [ ] All recent baselines included?
- [ ] Multiple datasets/settings tested?
- [ ] Proper statistical testing with corrections?
- [ ] Both success and failure cases shown?

### Writing Quality
- [ ] Consistent notation throughout?
- [ ] All numbers verified and consistent?
- [ ] No overclaiming?
- [ ] Limitations explicitly discussed?

### Reproducibility
- [ ] Code/data availability stated?
- [ ] All hyperparameters listed?
- [ ] Random seeds specified?
- [ ] Computational requirements documented?

---

## RESPONSE TO REVIEWS TEMPLATE

If you get a revision opportunity:

### For Each Reviewer Comment:
1. **Quote** the exact concern
2. **Acknowledge** the validity
3. **Describe** specific changes made
4. **Reference** page/section numbers
5. **Provide** new results if needed

### Major Revision Checklist:
- [ ] Address EVERY comment substantively
- [ ] Add requested experiments
- [ ] Fix all technical errors
- [ ] Improve clarity per feedback
- [ ] Thank reviewers genuinely

---

## REMEMBER

**The goal isn't just to get accepted—it's to contribute valuable, reproducible research to the community.**

Every section should pass the "hostile reviewer test": Would someone trying to find flaws be satisfied?

When in doubt:
- Add more detail rather than less
- Show more results rather than fewer  
- Be more conservative in claims
- Give more credit to prior work



