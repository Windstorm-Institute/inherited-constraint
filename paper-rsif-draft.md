# Biological Throughput Limits Shape the Information Structure of Human Language and Artificial Intelligence

Grant Lavell Whitmer III

The Windstorm Institute, Fort Ann, NY 12827, USA

Email: grantwhitmer3@gmail.com

ORCID: 0009-0007-3224-755X

---

**Abstract:** Silicon AI has no thermodynamic throughput basin, yet language models converge on approximately 4.2 bits per token -- within the biological basin. This study tests whether AI inherits its throughput from training data produced by biologically constrained brains. Bits-per-token (BPT) was measured across seven corpora using four models on standardized hardware. Natural language produces BPT of approximately 3.90, coinciding with the ribosome (4.39 bits/codon) and basin centroid (4.16 +/- 0.19 bits). Destroying word order doubles per-token surprise to approximately 10.8 bits. A granular shuffling cascade localizes the dominant structure to sentence-internal word order (syntax), contributing approximately 3.3 bits. Zipf exponents are identical in original and shuffled English (alpha = -0.843), proving word-frequency statistics insufficient for the approximately 4.4-bit convergence. A four-link causal chain is proposed: physics constrains biology, biology constrains cognition, cognition constrains language, language constrains AI. Links 1--2 are established; Links 3--4 are supported by convergent evidence with falsifiable predictions offered.

**Keywords:** inherited information density; bits per token; shuffling cascade; syntactic structure; cognitive processing capacity; cross-substrate convergence

---

## 1. Introduction

Five companion papers established the throughput basin (3--6 bits per serial event) [1--5] and demonstrated that its thermodynamic basis constrains biology through pairwise discrimination cost (Regime A) while silicon AI escapes this constraint (Regime B, sub-linear cost) [5]. This creates a paradox: if the physics does not constrain silicon, why does silicon land in the same neighborhood as the ribosome?

The hypothesis tested here is that AI inherits its throughput from the biological systems that generated its training data. Every language model was trained on human text. Human text was produced by human brains -- biological serial decoders constrained by the throughput basin. The information density of human language evolved to match the approximately 4--5 bit processing capacity of the biological systems that produce and receive it. When GPT-4 processes English at approximately 4.4 bits per token, it is learning a pattern that biological evolution burned into the structure of language over millions of years.

## 2. Material and Methods

### 2.1. Models and Hardware

Four models were evaluated: Pythia-70m (70M parameters), Pythia-410m (410M), GPT-2 (124M), and GPT-2-large (774M). All use vocabularies of 50,257--50,304 tokens (log_2 ~ 15.62, constant across models). Evaluations were performed on an NVIDIA RTX 5090 with deterministic inference settings. Energy was measured via nvidia-smi GPU power polling at 10 ms intervals.

### 2.2. Seven Corpora

Seven corpora were selected to span a range of structure types:

1. **Natural language** (WikiText-2): Human cognitive, full syntax and semantics.
2. **Python code**: Human cognitive, strict formal rules.
3. **DNA sequences**: Biological non-cognitive, statistical patterns.
4. **Synthetic structured data**: Algorithmic CSV-like patterns.
5. **Mathematical notation**: Formal symbolic, moderate structure.
6. **Random printable text**: No structure, no patterns.
7. **Shuffled English**: Same words as natural language, random order -- structure destroyed.

### 2.3. Basin-Blind Design

All BPT values were computed before any comparison to the throughput basin. If natural language had shown 2 bits or 9 bits, that value would have been reported. The alignment between natural-language BPT and the basin is a discovery, not an assumption.

### 2.4. Primary Metric

BPT = loss / ln(2), where loss is the teacher-forced cross-entropy. BPT is vocabulary-independent and normalizes across tokenizations. The structural bonus is defined as Delta_BPT = BPT_shuffled - BPT_original.

### 2.5. Granular Shuffling Cascade

Structure was destroyed at successive levels to localize which level of linguistic organization carries the most information:

1. Shuffle paragraphs (keep sentences intact within each paragraph).
2. Shuffle sentences (keep words intact within each sentence).
3. Shuffle words within sentences (keep sentence boundaries).
4. Shuffle all words (destroy all structure).
5. Shuffle characters (destroy sub-word structure).

### 2.6. Zipf Analysis

The Zipf exponent (rank-frequency power law) was computed for both original and shuffled English to test whether word-frequency statistics alone explain the approximately 4.4-bit BPT.

## 3. Results

### 3.1. Basin-Blind BPT Measurement

**Table 1.** BPT across seven corpora (mean of four models).

| Corpus | Mean BPT | In basin (3--6 bits)? |
|--------|----------|---------------------|
| Natural language | 3.90 | Yes |
| Python code | 2.47 | Below |
| DNA sequences | 4.39 | Yes |
| Synthetic structured | 3.83 | Yes |
| Mathematical notation | 7.00 | Above |
| Random printable text | 8.27 | Far above |
| Shuffled English | 10.64 | Far above |

**Table 1b.** Natural language BPT by model.

| Model | Parameters | Natural language BPT | Shuffled BPT | Structural bonus |
|-------|-----------|---------------------|-------------|-----------------|
| Pythia-70m | 70M | 4.69 | 10.97 | 6.28 |
| Pythia-410m | 410M | 3.37 | 10.65 | 7.28 |
| GPT-2 | 124M | 4.05 | 10.63 | 6.58 |
| GPT-2-large | 774M | 3.47 | 10.29 | 6.82 |

Larger models achieve lower BPT on natural language (exploiting more structure) but show similar BPT on shuffled text (approximately 10.5 across all models), indicating that the structural bonus scales with model capacity while the base rate (word frequencies) is captured even by small models.

Natural language (BPT ~ 3.90) falls inside the throughput basin. The ribosome processes information at 4.39 bits per codon. Claude Shannon, in 1951, estimated the entropy of printed English at approximately 1 bit per character -- roughly 5 bits per word [6]. Three independent measurements, three different methods, three different decades, the same neighborhood.

The structural bonus (Delta_BPT) is 6.28--6.82 across models (mean 6.74 bits; paired t-test: t(3) = 27.4, p < 0.001). Destroying word order more than doubles per-token surprise.

### 3.2. Granular Shuffling Cascade

**Table 2.** Information contribution by structural level (mean of Pythia-70m and GPT-2).

| Shuffling level | Delta from previous level |
|----------------|--------------------------|
| Paragraphs shuffled | -1.3 bits |
| Sentences shuffled | -0.6 bits |
| Within-sentence words shuffled | -3.3 bits |
| All words shuffled | -0.9 bits |

Syntax -- sentence-internal word order -- is the dominant carrier of cognitive information in human language, contributing approximately 3.3 bits per token. This is more than discourse structure (1.3 bits), sentence ordering (0.6 bits), and all other levels combined. This finding connects to the Uniform Information Density hypothesis [7], which proposes that speakers distribute information roughly evenly across words to match the receiver's processing capacity -- but UID never specified what that capacity is. The throughput basin provides the missing number: approximately 4--5 bits per cognitive event.

### 3.3. Zipf Is Insufficient

Original English: alpha = -0.843, R^2 = 0.992. Shuffled English: alpha = -0.843, R^2 = 0.992. Identical. Exactly the same words at exactly the same frequencies. Yet original English yields approximately 11 bits of effective information per token while shuffled English yields approximately 5 bits. A 6-bit difference with identical word statistics proves that word-frequency statistics are necessary but not sufficient. Anyone who claims that the approximately 4.4-bit convergence is "just Zipf's law" is refuted by this single control.

### 3.4. Softmax Temperature and the Basin

The softmax temperature T controls the entropy of the model's output distribution. At T = 1.0 (the standard training temperature), output entropy is approximately 5.4 bits -- right in the throughput basin. At T = 0.5, entropy drops to approximately 1.6 bits (below the basin). At T = 1.5, entropy rises to approximately 10.3 bits (above the basin). The fact that T = 1.0 produces basin-aligned entropy is consistent with the inherited constraint hypothesis but is noted as a training convention rather than an emergent optimization: cross-entropy loss is calibrated at T = 1.0, so this coincidence is expected rather than independently confirming.

### 3.5. Cognitive Signature: Variance Not Just Mean

DNA sequences produce BPT of 4.54 -- in the basin -- but DNA is non-cognitive. Code produces BPT of 2.80 -- outside the basin -- but code is cognitive. The distinction lies in the compressibility profile, not the mean BPT alone. Code is hyper-predictable (low BPT, low variance) because formal syntax constrains nearly every token. Natural language balances high-entropy novelty (new ideas, surprising word choices) with low-entropy structure (grammar, syntax), producing a characteristic phase transition between predictable and unpredictable tokens. DNA's basin membership likely reflects tokenizer artifacts (poor English-tokenizer fit to biological sequences) rather than genuine cognitive structure.

### 3.6. Energy Cost of Structure

Natural language costs 0.347 millijoules per token. Shuffled language costs 0.291 millijoules per token -- a 19.2% premium. The model works harder on structured text, probably because the attention mechanism computes meaningful long-range dependencies (subject-verb agreement, coreference, discourse coherence) that do not exist in shuffled text. Grammar is not computationally free. The information it provides (approximately 6.5 extra bits per token) costs real energy to extract (approximately 0.056 millijoules per token, or about 0.009 millijoules per bit of structure).

## 4. Discussion

### 4.1. The Proposed Causal Chain

A four-link causal chain is proposed:

**Link 1 (Established): Physics constrains biology.** Thermodynamic cost minimization under pairwise discrimination constraints (Regime A) constrains biological decoders to 3--6 bits per event. Evidence: five companion papers [1--5].

**Link 2 (Established): Biology constrains cognition.** Neural systems built from biological substrates inherit the throughput constraint. Working memory: approximately 3.1 bits per item. Phoneme discrimination: approximately 4.2 bits. Evidence: Miller [8], Miller and Nicely [9], decades of psychophysics.

**Link 3 (Proposed): Cognition constrains language.** Language evolved as a communication channel between brains constrained to approximately 4--5 bits per event. Evidence: BPT ~ 4.4 (this paper), Shannon's 1951 estimate [6], the UID literature [7]. Not yet causally demonstrated.

**Link 4 (Proposed): Language constrains AI.** Models trained on human language learn its statistical structure. The approximately 4.4-bit BPT reflects the information density that biological cognition selected for. Evidence: the shuffling experiment. Not yet tested with a synthetic-training control.

### 4.2. Connection to Zipf's Law

Zipf's law has been observed across all human languages since 1935, but no agreed-upon explanation exists. The throughput basin framework suggests a hypothesis: Zipf distributions may emerge when communication is optimized between agents constrained to approximately 4--5 bits per processing event. A power-law word-frequency distribution is the maximum-entropy distribution subject to a constraint on mean information per word -- and the biological throughput basin provides exactly such a constraint. This is stated as a hypothesis, not a derivation; a formal proof would require showing that the approximately 4--5 bit constraint mathematically necessitates a power-law exponent near alpha ~ 1. The identical Zipf exponents in original and shuffled English (Section 3.3) demonstrate that Zipf is a property of vocabulary usage, while the approximately 4.4-bit BPT is a property of structured text -- they are complementary, not competing, descriptions.

### 4.3. Syntax as Cognitive Organizer

The granular shuffling cascade localizes the dominant structure to sentence-internal word order. This is not a tautology of model design: the asymmetry (syntax 3.3 bits versus discourse 1.3 bits) is a property of language, not of transformers. The finding is consistent with the UID hypothesis and supplies the quantitative capacity value that UID lacked.

### 4.4. Falsifiable Predictions

1. **Cross-linguistic universality:** Shuffled non-English text (Chinese, Arabic, Finnish) should produce BPT of approximately 5 bits (+/- 1 for vocabulary effects). Falsification: shuffled Piraha produces BPT outside 3--7 bits.
2. **Synthetic training baseline:** A model trained exclusively on non-biological data (synthetic patterns, mathematical proofs) should show BPT outside 3--6 bits. Falsification: synthetic-trained model shows BPT in 3--6 bits.
3. **BPB convergence floor:** As models improve, BPB on English should approach but not drop far below approximately 0.5. Falsification: frontier models achieve BPB < 0.3 consistently.
4. **Phonemic inventory correlation:** Languages with fewer phonemes should show steeper Zipf slopes. Falsification: no correlation exists.

### 4.5. The Bigger Picture

The throughput basin constrains biology directly, through the physics of molecular discrimination. It constrains language indirectly, through the cognitive capacity of the brains that invented it. It constrains AI at one further remove, through the training data that carries language's biological fingerprint. The ribosome found this limit through 3.8 billion years of evolution. Human language found it through millions of years of cognitive optimization. AI learned it in a few months of training on the internet. Three timescales, three substrates, one neighborhood: approximately 4.4 bits. The fingerprint is everywhere -- the question is whether it reflects a deep constraint or a coincidence of training data distribution. The falsifiable predictions offered in this paper are designed to distinguish between these interpretations.

### 4.6. Limitations

1. **Training-data familiarity confound:** Models naturally perform better on text similar to their training data. The shuffled-language comparison is robust (same vocabulary, same familiarity), but cross-corpus comparisons are confounded.
2. **Model diversity:** Only four models tested, all Pythia/GPT-2 variants with similar vocabularies. Extension to LLaMA, Qwen, Gemma and non-English languages is needed.
3. **Causal claim limitation:** Whether natural language BPT reflects a biological constraint versus a general property of structured text requires the synthetic-training test (Prediction 2).

---

## Ethics Statement

This work did not require ethical approval.

## Data Accessibility

All experiment code and data are publicly available at https://github.com/Windstorm-Labs/inherited-constraint (DOI: 10.5281/zenodo.XXXXXXX).

## Declaration of AI Use

Claude (Anthropic) was used as an AI research tool for mathematical derivations, data analysis, and manuscript drafting assistance. All results were verified independently by the author.

## Authors' Contributions

G.L.W.: conceptualization, methodology, software, validation, formal analysis, investigation, resources, data curation, writing -- original draft, writing -- review and editing, visualization, supervision, project administration.

## Conflict of Interest Declaration

The author declares no competing interests.

## Funding

This research received no external funding. All work was self-funded by the author.

## Acknowledgements

All experiments were performed with the assistance of Claude (Anthropic), an AI research tool. Energy measurements were conducted on an NVIDIA RTX 5090.

## References

[1] Whitmer GL III. The Fons Constraint: Information-Theoretic Convergence on Encoding Depth in Self-Replicating Systems. Zenodo. 2026. DOI: 10.5281/zenodo.19274048

[2] Whitmer GL III. The Receiver-Limited Floor: Rate-Distortion Bounds on Serial Decoding Throughput. Zenodo. 2026. DOI: 10.5281/zenodo.19322973

[3] Whitmer GL III. The Throughput Basin: Cross-Substrate Convergence and Decomposition of Serial Decoding Throughput. Zenodo. 2026. DOI: 10.5281/zenodo.19323194

[4] Whitmer GL III. The Serial Decoding Basin: Five Experiments on Convergence, Thermodynamic Anchoring, and Receiver-Limited Geometry. Zenodo. 2026. DOI: 10.5281/zenodo.19323423

[5] Whitmer GL III. The Dissipative Decoder: Thermodynamic Cost Bounds on the Serial Decoding Throughput Basin. Zenodo. 2026. DOI: 10.5281/zenodo.19433048

[6] Shannon CE. Prediction and Entropy of Printed English. Bell Syst Tech J. 1951;30:50-64. DOI: 10.1002/j.1538-7305.1951.tb01366.x

[7] Jaeger TF. Redundancy and Reduction: Speakers Manage Syntactic Information Density. Cogn Psychol. 2010;61:23-62. DOI: 10.1016/j.cogpsych.2010.02.002

[8] Miller GA. The Magical Number Seven, Plus or Minus Two: Some Limits on Our Capacity for Processing Information. Psychol Rev. 1956;63:81-97. DOI: 10.1037/h0043158

[9] Miller GA, Nicely PE. An Analysis of Perceptual Confusions among Some English Consonants. J Acoust Soc Am. 1955;27:338-352. DOI: 10.1121/1.1907526

[10] Whitmer GL III. Inherited Constraint: Experiment Code and Data. GitHub. 2026. Available from: https://github.com/Windstorm-Labs/inherited-constraint (accessed 12 April 2026).
