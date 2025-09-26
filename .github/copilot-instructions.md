# GitHub Copilot Instructions for math-aio

## Project Overview
This is a LaTeX-based mathematical document repository containing personal math notes compiled into a single comprehensive document. The project focuses on topology, cardinality theory, and related mathematical concepts.

## Project Structure
- `main.tex` - Main LaTeX document that includes all sections
- `macros.tex` - Custom LaTeX macros and theorem environments
- `topology/` - Directory containing mathematical content organized by topic
- `ref.txt` - Reference file with theorem/lemma labels and their IDs

## LaTeX Conventions and Style

### Document Structure
- Use `\input{}` to include section files from subdirectories
- Each major topic should be in its own subdirectory (e.g., `topology/`)
- Section files should follow naming convention: `sec##-topic-name.tex`

### Mathematical Content
- Use the predefined theorem environments from `macros.tex`:
  - `thm` for theorems
  - `lem` for lemmas  
  - `prop` for propositions
  - `definition` for definitions
  - `exercise` for exercises
  - `corollary` for corollaries
  - `remark` for remarks
  - `example` for examples

### Cross-References
- Use `\label{}` with descriptive hexadecimal IDs (8 characters) for all theorems, lemmas, etc.
- Use `\cref{}` or `\autoref{}` for cross-references instead of `\ref{}`
- Track important references in `ref.txt` with format: "Name, label_id"

### Mathematical Notation
- Use `\mathrm{card}()` for cardinality
- Use `\mathbb{}` for number sets (ℕ, ℝ, ℤ, etc.)
- Use `\mathcal{}` for script letters (𝒫 for power set)
- Use `\mathscr{}` for script fonts when available
- Prefer `\subseteq`, `\supseteq` over `\subset`, `\supset`
- Use `\varnothing` for empty set instead of `\emptyset`

### Formatting Guidelines
- Use `align*` environment for multi-line equations without numbering
- Use `\[` and `\]` for single-line displayed equations
- Include proper spacing around mathematical operators
- Use `\text{}` for text within math mode
- Use `\quad` and `\qquad` for spacing in equations

### Proof Structure
- Start proofs with `\begin{proof}` and end with `\end{proof}`
- Use clear logical flow with appropriate paragraph breaks
- Include intermediate steps and justifications
- Reference relevant theorems and lemmas using `\cref{}`

## Code Style
- Maintain consistent indentation (2-4 spaces)
- Keep lines reasonably short (prefer line breaks before 80-100 characters)
- Use descriptive labels for theorems and definitions
- Add comments for complex LaTeX constructions

## Build System
- The project uses `latexmk` for building (as indicated by `%!LW recipe=latexmk`)
- Output files (.pdf, .aux, .log, etc.) are ignored in `.gitignore`
- Use `a4paper` format with 11pt font size

## Best Practices
1. **Consistency**: Follow the existing theorem numbering and labeling scheme
2. **Modularity**: Break content into logical sections and files
3. **Documentation**: Include clear mathematical exposition and proofs
4. **References**: Maintain the reference tracking system in `ref.txt`
5. **Dependencies**: Keep macro definitions centralized in `macros.tex`

## When Adding New Content
1. Create appropriate section files in relevant subdirectories
2. Add theorem/definition labels to `ref.txt` if they're important references
3. Use the established theorem environments and numbering system
4. Include the new section in `main.tex` using `\input{}`
5. Follow the mathematical notation conventions established in existing content

## Mathematical Focus Areas
The repository covers:
- Metric spaces and topology
- Set theory and cardinality
- Axiom of Choice and equivalents (Zorn's Lemma, Hausdorff Maximal Principle)
- Function theory and injections/surjections
- Infinite set theory

When contributing to these areas, maintain mathematical rigor and provide complete proofs with proper justification for each step.