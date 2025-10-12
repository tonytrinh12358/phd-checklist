# Comprehensive Research Paper Guidelines
## Based on AAAI Rejection Feedback Analysis

---

## 1. TECHNICAL SOUNDNESS & COMPLETENESS

### Core Requirements:
- **Complete Algorithm Specification**: Every method must be implementable from the paper alone
  - Include full training procedures with pseudocode
  - Specify all hyperparameters and their selection rationale
  - Detail gradient computation/approximation for non-differentiable objectives
  - Provide complete inference procedures

- **Mathematical Rigor**:
  - Every equation must be formally correct and use proper notation
  - Avoid set operations for ordered sequences (use concatenation operators)
  - Ensure consistency between mathematical formalism and implementation
  - Define all variables, domains, and ranges precisely

- **Implementation Bridge**:
  - Explain how theoretical formulations translate to practical code
  - For RL/optimization: specify policy gradients, reward shaping, variance reduction
  - For neural methods: detail architecture, loss functions, optimization procedures
  - Include failure modes and mitigation strategies

### Checklist:
- [ ] Can a competent researcher reproduce your work from the paper alone?
- [ ] Are all mathematical statements formally correct?
- [ ] Is every design choice justified with theory or empirical evidence?
- [ ] Are all algorithmic components fully specified?

---

## 2. THEORETICAL CONTRIBUTIONS

### Requirements:
- **Accurate Claims**:
  - Never overstate theoretical results
  - Provide formal proofs or clearly mark claims as conjectures
  - State all assumptions explicitly
  - Distinguish between theoretical guarantees and empirical observations

- **Proper Theoretical Framework**:
  - Use established terminology correctly (e.g., "convex combination" only for actual convex combinations)
  - Connect to existing theory appropriately
  - Avoid introducing new theoretical claims without rigorous proof
  - If claiming optimality (Pareto, Nash, etc.), prove it formally

- **Theoretical Justification**:
  - Explain WHY your approach works, not just THAT it works
  - Connect design choices to theoretical principles
  - Address potential theoretical limitations explicitly

### Checklist:
- [ ] Are all theorems/lemmas accompanied by rigorous proofs?
- [ ] Are assumptions clearly stated and justified?
- [ ] Is mathematical terminology used correctly throughout?
- [ ] Are theoretical claims supported by formal analysis?

---

## 3. EXPERIMENTAL EVALUATION

### Comprehensive Baselines:
- **Coverage Requirements**:
  - Include ALL directly relevant prior work from the last 2-3 years
  - Compare against the current state-of-the-art, not just convenient baselines
  - Include strong simple baselines to demonstrate added complexity is justified
  - For each component, include ablation against simpler alternatives

- **Evaluation Scope**:
  - Test on multiple datasets/benchmarks
  - Vary experimental conditions (different backbones, hyperparameters, etc.)
  - Include both automated metrics AND human evaluation when applicable
  - Report failure cases and limitations

### Statistical Rigor:
- **Proper Statistical Testing**:
  - Use appropriate statistical tests for your data distribution
  - Apply multiple testing corrections (e.g., Bonferroni)
  - Report confidence intervals, not just p-values
  - Use appropriate effect size measures (Cohen's d for parametric, Cliff's delta for non-parametric)

- **Numerical Accuracy**:
  - Double-check all numerical calculations
  - Ensure percentage improvements are computed correctly
  - Report consistent significant figures
  - Include standard deviations/error bars

### Reporting Standards:
- **Metric Specification**:
  - Define every metric precisely (formula, implementation, normalization)
  - Specify model checkpoints, versions, and configurations
  - Clarify direction of improvement (↑ or ↓) and valid ranges
  - Avoid creating custom metrics without thorough validation

### Checklist:
- [ ] Are all relevant baselines included and properly cited?
- [ ] Is statistical significance properly tested and reported?
- [ ] Are all metrics clearly defined and consistently used?
- [ ] Are both successes and failures discussed?

---

## 4. WRITING CLARITY & CONSISTENCY

### Notation and Terminology:
- **Consistency Rules**:
  - Use the same notation throughout (including algorithms and equations)
  - Define all symbols before first use
  - Maintain consistent variable naming in text, equations, and algorithms
  - Avoid overloading notation

- **Precision in Language**:
  - Be precise about comparative claims ("best among enhancement methods" vs "best overall")
  - Avoid ambiguous pronouns and references
  - Use technical terms correctly and consistently

### Structure and Flow:
- **Logical Organization**:
  - Motivation → Problem Formulation → Method → Experiments → Results
  - Each section should flow naturally into the next
  - Include clear transitions between ideas
  - Ensure claims in abstract/intro match results

- **Internal Consistency**:
  - Ensure numbers/claims are consistent across abstract, intro, and results
  - Reconcile all tables/figures with text descriptions
  - Check that methodology matches experimental description

### Checklist:
- [ ] Is notation consistent throughout the paper?
- [ ] Do all claims in abstract/intro match the actual results?
- [ ] Are all technical terms used correctly?
- [ ] Is the paper's narrative coherent and well-structured?

---

## 5. REPRODUCIBILITY

### Code and Data:
- **Availability Requirements**:
  - Clearly state what will be released and when
  - Include implementation details sufficient for reproduction
  - Provide preprocessing scripts and data splits
  - Document all dependencies and versions

- **Experimental Details**:
  - Random seeds and initialization procedures
  - Hardware specifications and runtime
  - Hyperparameter search procedures and ranges
  - Number of runs and selection criteria

### Documentation:
- **Complete Specifications**:
  - Training time, inference time, and computational resources
  - Memory requirements
  - Scaling properties
  - Platform/framework dependencies

### Checklist:
- [ ] Can someone reproduce your results with reasonable effort?
- [ ] Are all hyperparameters and design choices documented?
- [ ] Is the code release plan clearly stated and consistent?
- [ ] Are computational requirements fully specified?

---

## 6. SCOPE AND LIMITATIONS

### Honest Assessment:
- **Limitation Discussion**:
  - Explicitly discuss where your method might fail
  - Acknowledge theoretical limitations
  - Discuss computational/practical constraints
  - Address potential negative societal impacts

- **Scope Definition**:
  - Clearly define what problems your method solves
  - Specify assumptions and when they might not hold
  - Discuss generalization boundaries
  - Include failure case analysis

### Checklist:
- [ ] Are limitations explicitly discussed?
- [ ] Is the method's scope clearly defined?
- [ ] Are potential failure modes identified?
- [ ] Are ethical considerations addressed?

---

## 7. ABLATION STUDIES

### Component Analysis:
- **Requirements**:
  - Isolate the contribution of each novel component
  - Compare against simpler alternatives
  - Justify added complexity with clear performance gains
  - Show that improvements aren't from incidental factors

- **Design Validation**:
  - Test key design choices (architecture, hyperparameters)
  - Analyze sensitivity to important parameters
  - Demonstrate robustness across settings
  - Include "unit tests" for key components

### Checklist:
- [ ] Is each novel component's contribution isolated?
- [ ] Are design choices validated empirically?
- [ ] Is the added complexity justified?
- [ ] Are results robust to hyperparameter changes?

---

## 8. CONTRIBUTION CLAIMS

### Appropriate Framing:
- **Novelty Claims**:
  - Accurately represent what is novel vs. adapted
  - Acknowledge similar prior approaches
  - Focus on genuine advances, not incremental changes
  - Avoid overclaiming ("first", "novel" when not true)

- **Significance**:
  - Demonstrate practical or theoretical importance
  - Show substantial improvements over baselines
  - Provide insights beyond empirical results
  - Connect to broader research themes

### Checklist:
- [ ] Are novelty claims accurate and justified?
- [ ] Is the significance clearly demonstrated?
- [ ] Are contributions properly contextualized?
- [ ] Is credit given to foundational work?

---

## 9. SPECIAL CONSIDERATIONS BY DOMAIN

### For Multi-Objective Optimization:
- Prove or empirically demonstrate Pareto optimality claims
- Thoroughly analyze trade-offs between objectives
- Include preference/weight sensitivity analysis
- Compare against multi-objective optimization baselines

### For Generative Models:
- Include human evaluation for quality/preference
- Test on multiple generation backends
- Analyze mode collapse and diversity
- Include both quantitative and qualitative results

### For Safety-Critical Applications:
- Thoroughly evaluate safety claims
- Include worst-case analysis
- Test on adversarial/edge cases
- Discuss failure modes and mitigation

---

## 10. FINAL REVIEW CHECKLIST

Before submission, verify:

### Technical Completeness:
- [ ] All algorithms are fully specified
- [ ] Mathematical statements are formally correct
- [ ] Implementation details enable reproduction

### Experimental Rigor:
- [ ] All relevant baselines included
- [ ] Statistical testing is appropriate and corrected
- [ ] Both automated and human evaluation (where applicable)

### Writing Quality:
- [ ] Consistent notation and terminology
- [ ] No contradictory statements
- [ ] Clear limitation discussion

### Reproducibility:
- [ ] Code/data availability clearly stated
- [ ] All hyperparameters documented
- [ ] Computational requirements specified

### Impact:
- [ ] Genuine advancement demonstrated
- [ ] Significance clearly articulated
- [ ] Broader implications discussed

---

## COMMON PITFALLS TO AVOID

1. **Overclaiming**: Making theoretical claims without rigorous proof
2. **Cherry-picking**: Selecting only favorable baselines or metrics
3. **Inconsistency**: Different numbers/claims in different sections
4. **Incompleteness**: Missing crucial implementation details
5. **Misuse of terminology**: Using technical terms incorrectly
6. **Insufficient evaluation**: Limited datasets or missing human evaluation
7. **Poor baseline selection**: Omitting recent, relevant work
8. **Statistical errors**: Wrong tests or missing corrections
9. **Reproducibility gaps**: Insufficient detail for replication
10. **Narrow scope**: Testing only in favorable conditions

---

## STRATEGY FOR USING THESE GUIDELINES

1. **During Research Design**: Use Section 1-2 to ensure sound methodology
2. **During Implementation**: Follow Section 5 for reproducibility
3. **During Experiments**: Apply Section 3 for rigorous evaluation
4. **During Writing**: Use Section 4 for clarity and consistency
5. **Before Submission**: Complete all checklists
6. **For Revision**: Address each guideline systematically

Remember: A strong paper doesn't just present results—it provides complete, reproducible, and rigorously validated contributions with honest assessment of limitations and clear articulation of significance.



