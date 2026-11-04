# Paper Research Analyzer

## 1. Problem

Academic papers can be difficult to review quickly because their research questions, experimental details, results, and limitations are spread across multiple sections. Paper Research Analyzer turns paper material supplied by the user into a structured analysis while marking missing information instead of guessing.

## 2. Main Features

- Analyzes paper text, abstracts, excerpts, extracted PDF text, and research notes.
- Summarizes the research question, objective, methodology, materials, conditions, results, contribution, and limitations.
- Identifies explicit and potential research gaps, and suggests evidence-based follow-up directions.
- Explains only the Chemical Engineering connections supported by the supplied paper.
- Produces a one-minute summary and a compact research note table.
- Preserves numerical values, units, chemical formulas, and experimental conditions; distinguishes reported facts from AI interpretation.
- Does not fetch web pages or read inaccessible PDFs. Provide the paper text or extracted text.

## 3. Installation

Copy the `skills/paper-research-analyzer` folder into the skills directory supported by your AI assistant. For Codex, use:

```text
~/.codex/skills/paper-research-analyzer
```

## 4. Usage

Invoke `$paper-research-analyzer` and paste the paper text, abstract, excerpt, extracted PDF text, or research notes. For a detailed analysis, include the methods, results, conditions, and any author-stated limitations. If you provide only an abstract or excerpt, the analysis will be limited to that material.

## 5. Input and Output Example

**Input**

```text
Use $paper-research-analyzer to analyze this excerpt:

The study tested a nickel catalyst at 300 °C and 1 bar. Increasing the nickel
loading from 5 wt% to 10 wt% raised methane conversion from 42% to 61%.
The abstract does not state the reaction duration or catalyst lifetime.
```

**Output excerpt**

```text
### Key Results
- Methane conversion increased from 42% to 61% when nickel loading rose
  from 5 wt% to 10 wt% at 300 °C and 1 bar.

### Limitations
- Explicitly stated by the authors: Not stated in the supplied excerpt.
- Potential limitations inferred from the supplied material: Reaction duration
  and catalyst lifetime are not reported in the excerpt (AI interpretation).

### Research Note
| Category | Key Information |
|---|---|
| Conditions | 300 °C; 1 bar |
| Key Results | Conversion: 42% at 5 wt% Ni; 61% at 10 wt% Ni |
```

The complete output also covers the paper overview, research question, methodology, materials and experimental conditions, main contribution, research gaps, potential research directions, Chemical Engineering relevance, and one-minute summary. Missing details are marked **Not stated**.
