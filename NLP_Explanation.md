# NATURAL LANGUAGE PROCESSING (NLP)
## Comprehensive Exam Notes — All 5 Units

---

## UNIT I: INTRODUCTION TO NLP & LANGUAGE MODELLING

### 1.1 What is Natural Language Processing (NLP)?

**Definition:** NLP is a field at the intersection of computer science, artificial intelligence, and linguistics that deals with making computers understand, analyze, manipulate, and interpret human (natural) languages.

**Key Characteristics:**
- Input/Output can be Speech or Written Text
- Enables human-computer communication in natural language
- Processes unstructured text data

**Real-World Applications:**
- Chatbots and Voice Assistants (Siri, Alexa)
- Email spam classification
- Search engines (Google, Bing)
- Machine translation (Google Translate)
- Sentiment analysis
- Grammar checkers

---

### 1.2 Components of NLP

| Component | Full Form | Description |
|-----------|-----------|-------------|
| **NLU** | Natural Language Understanding | Transforms human language into machine-readable format; extracts keywords, emotions, relations, semantics |
| **NLG** | Natural Language Generation | Converts computerized data into natural language; involves text planning, sentence planning, and text realization |

> **Exam Tip:** NLU is significantly harder than NLG.

---

### 1.3 Steps in NLP Processing

```
1. Lexical Analysis → 2. Syntactic Analysis → 3. Semantic Analysis → 4. Discourse Integration → 5. Pragmatic Analysis
```

**1. Lexical Analysis:**
- Scans text as a stream of characters
- Divides into paragraphs, sentences, and words
- Converts to meaningful lexemes
- Identifies tokens

**2. Syntactic Analysis (Parsing):**
- Checks grammar and word arrangements
- Shows relationships among words
- Example: "The school goes to boy" rejected by syntactic analyzer

**3. Semantic Analysis:**
- Concerned with meaning representation
- Focuses on literal meaning of words, phrases, sentences
- Example: "hot ice-cream" disregarded (semantically nonsensical)

**4. Discourse Integration:**
- Depends on preceding sentences
- Invokes meaning of following sentences
- Example: "Manhattan speaks to all its people. It calls out to Dave." → "It" refers to Manhattan

**5. Pragmatic Analysis:**
- Re-interprets what was said to what was actually meant
- Involves real-world knowledge
- Example: "Open the door" interpreted as a request, not an order

---

### 1.4 NLP Terminology

| Term | Definition | Example |
|------|------------|---------|
| **Phonology** | Study of organizing sound systematically | Sound patterns in language |
| **Morphology** | Study of formation and internal structure of words | "unfriendly" = un + friend + ly |
| **Morpheme** | Primitive unit of meaning | play, -ed, un-, cat, -s |
| **Syntax** | Arrangement of words to form sentences | Subject-Verb-Object order |
| **Semantics** | Meaning of words and combinations | "Colorless green ideas" |
| **Pragmatics** | Understanding sentences in different situations | Sarcasm, metaphors |
| **Discourse** | How preceding sentences affect interpretation | Context dependency |
| **World Knowledge** | General knowledge about the world | Facts and reasoning |

---

### 1.5 Challenges in NLP (Important!)

**Types of Ambiguity:**

| Type | Level | Example |
|------|-------|---------|
| **Lexical Ambiguity** | Word-level | "board" (noun: wooden piece vs verb: to join) |
| **Syntactic Ambiguity** | Sentence-level | "He lifted the beetle with red cap" (cap used to lift, or beetle with cap) |
| **Referential Ambiguity** | Pronoun-level | "Rima went to Gauri. She said..." (who is tired?) |

**Additional Challenges:**
- One input can mean different meanings
- Many inputs can mean the same thing
- Creative language use (new words, idioms)
- Domain-specific terminology

---

### 1.6 Applications of NLP

1. **Sentiment Analysis** — Identifying emotional tone in text
2. **Machine Translation** — Converting text from one language to another
3. **Text Extraction** — Extracting entities, locations, quantities
4. **Text Classification** — Categorizing text into predefined groups
5. **Speech Recognition** — Converting spoken language to text
6. **Chatbots** — Automated conversation systems
7. **Email Filtering** — Spam detection, categorization
8. **Search Autocorrect/Autocomplete** — Query assistance

---

## LANGUAGE MODELLING

### 1.7 What is a Language Model?

**Definition:** A language model assigns probability to sequences of words. It predicts the probability of a word given its context, or the probability of an entire sentence.

**Uses of Language Modelling:**

1. **Speech Recognition:** Distinguishing "I will be back soonish" from "I will be bassoon dish"
2. **Spelling Correction:** Detecting "Their are" should be "There are"
3. **Machine Translation:** Ranking candidate translations
4. **Text Generation:** Word prediction in keyboards
5. **Question Answering:** Predicting likely continuations

---

### 1.8 N-Gram Models

**Definition:** An n-gram is a sequence of n consecutive words.

| N-gram | Example | Description |
|--------|---------|-------------|
| **Unigram (n=1)** | "hello", "world" | Single words |
| **Bigram (n=2)** | "hello world", "turn your" | Two-word sequences |
| **Trigram (n=3)** | "turn your homework" | Three-word sequences |
| **N-gram (general)** | any sequence of n words | General form |

#### **Unigram Model**

Each word is treated independently. The probability of a sequence is the product of individual word probabilities:

```
P(w₁, w₂, ..., wₙ) ≈ P(w₁) × P(w₂) × ... × P(wₙ)
```

**Limitation:** Ignores all context — "I will be back" would have same probability as "back will I be"

#### **Bigram Model**

The probability of a word depends only on the immediately preceding word:

```
P(wₙ|w₁, w₂, ..., wₙ₋₁) ≈ P(wₙ|wₙ₋₁)
```

This is called the **Markov Assumption** — we approximate the probability of a word given its entire history by the probability given only the previous word.

#### **Trigram Model**

The probability depends on the two preceding words:

```
P(wₙ|w₁, ..., wₙ₋₁) ≈ P(wₙ|wₙ₋₂, wₙ₋₁)
```

---

### 1.9 Maximum Likelihood Estimation (MLE)

**Purpose:** Estimate n-gram probabilities from a corpus.

**Formula:**
```
P(wₙ|wₙ₋₁) = C(wₙ₋₁, wₙ) / C(wₙ₋₁)
```

Where:
- C(wₙ₋₁, wₙ) = count of bigram (wₙ₋₁, wₙ)
- C(wₙ₋₁) = count of unigram (wₙ₋₁)

#### **Example Calculation:**

Given corpus:
```
<s> I am Sam </s>
<s> Sam I am </s>
<s> I do not like green eggs and ham </s>
```

**Step 1: Add start/end tokens**
```
<s> I am Sam </s>
<s> Sam I am </s>
<s> I do not like green eggs and ham </s>
```

**Step 2: Count unigrams**
| Unigram | Count |
|---------|-------|
| `<s>` | 3 |
| I | 3 |
| am | 2 |
| Sam | 1 |
| do | 1 |
| not | 1 |
| like | 1 |
| green | 1 |
| eggs | 1 |
| and | 1 |
| ham | 1 |
| `</s>` | 3 |

Total tokens (N) = 21

**Step 3: Calculate probabilities**

```
P(I|<s>) = C(<s>, I) / C(<s>) = 2/3 ≈ 0.667
P(am|I) = C(I, am) / C(I) = 2/3 ≈ 0.667
P(Sam|am) = C(am, Sam) / C(am) = 1/2 = 0.5
P(</s>|Sam) = C(Sam, </s>) / C(Sam) = 1/1 = 1.0
```

**Step 4: Probability of "I am Sam"**
```
P(<s> I am Sam </s>) = P(I|<s>) × P(am|I) × P(Sam|am) × P(</s>|Sam)
                     = (2/3) × (2/3) × (1/2) × (1/1)
                     = 4/18 = 2/9 ≈ 0.222
```

---

### 1.10 Perplexity (IMPORTANT METRIC!)

**Definition:** Perplexity measures how well a language model predicts a test set. **Lower perplexity = better model.** It represents the weighted average branching factor of the model.

**Formula:**
```
Perplexity(W) = P(w₁, w₂, ..., wₙ)^(-1/N)
             = [∏P(wᵢ|wᵢ₋₁)]^(-1/N)
```

**In log form (preferred for computation):**
```
Log Perplexity = - (1/N) × Σ log P(wᵢ|wᵢ₋₁)
Perplexity = 2^(Log Perplexity)
```

**Key Properties:**
- Minimizing perplexity ≡ Maximizing test set probability
- Perplexity of 1 = perfect prediction
- Higher perplexity = more uncertainty

#### **Numerical Example:**

Using Berkeley Restaurant Project data:

**Bigram counts table:**
|        | i   | want | to | english | food | chinese | a   |
|--------|-----|------|----|---------|------|---------|-----|
| **i**  | 5   | 33   | 2  | 1       | 0    | 0       | 2   |
| **want** | 0   | 0    | 6  | 1       | 2    | 1       | 0   |
| **to** | 0   | 0    | 0  | 4       | 2    | 2       | 1   |
| **english** | 0 | 0 | 0 | 0 | 1 | 0 | 0 |

**Unigram counts:**
```
i: 253
want: 195
to: 577
english: 26
food: 39
chinese: 55
a: 1206
```

**Calculate P(english|to):**
```
P(english|to) = C(to, english) / C(to) = 4/577 ≈ 0.0069
```

**Calculate P(food|english):**
```
P(food|english) = C(english, food) / C(english) = 1/26 ≈ 0.0385
```

**Probability of "i want to english food":**
```
P(i|</s>) × P(want|i) × P(to|want) × P(english|to) × P(food|english)
= (253/253) × (33/253) × (6/195) × (4/577) × (1/26)
= 1 × 0.130 × 0.031 × 0.0069 × 0.0385
≈ 0.00000107
```

**Perplexity calculation:**
```
Log Perplexity = -1/5 × [log(0.130) + log(0.031) + log(0.0069) + log(0.0385)]
               = -1/5 × [-0.886 + (-1.509) + (-2.161) + (-1.415)]
               = -1/5 × (-5.971)
               = 1.194
Perplexity = 2^1.194 ≈ 2.29
```

---

### 1.11 Smoothing Techniques (IMPORTANT!)

**Problem:** Zero probability n-grams — sequences that appear in test set but not in training set. This causes perplexity to be undefined (division by zero).

**Solution:** Smoothing (or discounting) — shave probability from seen events and give to unseen events.

#### **1. Laplace (Add-One) Smoothing**

Add 1 to every count:

```
P*(wᵢ) = (cᵢ + 1) / (N + V)
```

Where:
- cᵢ = original count
- N = total number of tokens
- V = vocabulary size

**Example:**

Bigram "chinese food" appears 0 times (zero count) in training.

Without smoothing: P(chinese|chinese) = 0/55 = 0

With Laplace:
```
P*(food|chinese) = (0 + 1) / (55 + V)
                 = 1 / (55 + 1446)  [V=1446 from Berkeley corpus]
                 = 1/1501 ≈ 0.00067
```

**Problem with Laplace:** Too much probability mass moved to zeros. Changes counts dramatically.

#### **2. Add-k Smoothing**

Add a fractional count k instead of 1:

```
P*(wᵢ) = (cᵢ + k) / (N + kV)
```

Common values: k = 0.5, 0.05, 0.01

**Example with k = 0.5:**
```
P*(food|chinese) = (0 + 0.5) / (55 + 0.5×1446)
                 = 0.5 / 778
                 ≈ 0.00064
```

#### **3. Backoff**

Use trigram if evidence exists, otherwise bigram, otherwise unigram:

```
P(wₙ|wₙ₋₂, wₙ₋₁) = [trigram exists] ? P(wₙ|wₙ₋₂, wₙ₋₁)
                 : [bigram exists] ? α × P(wₙ|wₙ₋₁)  
                 : β × P(wₙ)
```

#### **4. Linear Interpolation**

Always mix probabilities from all n-gram orders:

```
P(wₙ|wₙ₋₂, wₙ₋₁) = λ₁ × P(wₙ|wₙ₋₂, wₙ₋₁) 
                 + λ₂ × P(wₙ|wₙ₋₁) 
                 + λ₃ × P(wₙ)
```

Where λ₁ + λ₂ + λ₃ = 1

**Example:**
```
P(food|to, english) = 0.1 × P(food|to, english) + 0.3 × P(food|english) + 0.6 × P(food)
```

#### **5. Kneser-Ney Smoothing**

More sophisticated method that adjusts counts based on continuation frequency.

---

### 1.12 Unknown Words (OOV Problem)**

**Open Vocabulary vs Closed Vocabulary:**

| System | Description |
|--------|-------------|
| **Closed** | Fixed vocabulary, test set contains only known words |
| **Open** | Unknown words can appear in test set |

**Solution:** Create `<UNK>` pseudo-word:

**Method 1:** Fixed vocabulary
1. Choose vocabulary in advance
2. Replace training OOV words with `<UNK>`
3. Estimate P(`<UNK>`) from counts

**Method 2:** Frequency-based
- Replace words occurring < n times with `<UNK>`
- Or select top V words, rest become `<UNK>`

---

### 1.13 Regular Expressions and Automata

**Regular Expression Patterns:**

| Pattern | Matches | Example |
|---------|---------|---------|
| `.` | Any single character | `c.t` matches cat, cot |
| `*` | Zero or more | `ab*c` matches ac, abc, abbc |
| `+` | One or more | `ab+c` matches abc, abbc |
| `?` | Zero or one | `colou?r` matches color, colour |
| `^` | Start of string | `^Hello` matches "Hello there" |
| `$` | End of string | `world$` matches "Hello world" |
| `[abc]` | Character class | `[aeiou]` matches vowels |
| `[^abc]` | Negated class | `[^0-9]` matches non-digits |
| `\|` | Alternation | `cat\|dog` matches cat or dog |

**Automata:**
- Finite-state machines for pattern matching
- Used in morphological parsing
- Two types: Deterministic and Non-deterministic

---

### 1.14 Morphological Parsing

**Morphology:** Study of internal structure of words

**Morphemes — Minimal Meaningful Units:**

| Type | Example | Description |
|------|---------|-------------|
| **Stem** | play, cat, friend | Core meaning unit |
| **Prefix** | un-, re-, pre- | Before stem |
| **Suffix** | -ed, -s, -ly | After stem |

**Word Formation:**

```
played      = play + -ed
cats        = cat + -s
unfriendly  = un- + friend + -ly
replayed    = re- + play + -ed
computerized = comput- + -er- + -ize- + -d
```

**Two Types of Morphology:**

| Type | Definition | Example |
|------|------------|---------|
| **Inflectional** | Different forms of SAME word | cat → cats, run → ran |
| **Derivational** | Different LEXICAL category | receive → reception, teach → teacher |

**Allomorphs:** Alternative forms of the same morpheme
- Plural morpheme: -s (cats), -es (dishes), -en (oxen)

---

### 1.15 Parts of Speech (POS) Tagging

**Main POS Tags (Penn Treebank):**

| Tag | Meaning | Example |
|-----|---------|---------|
| NN | Noun, singular | cat, mountain |
| NNS | Noun, plural | cats, dogs |
| VBZ | Verb, 3rd person singular present | runs, eats |
| VBD | Verb, past tense | ran, ate |
| VBG | Verb, gerund | running, eating |
| JJ | Adjective | big, happy |
| RB | Adverb | quickly, very |
| DT | Determiner | the, a, an |
| IN | Preposition | in, on, at |
| PRP | Personal pronoun | I, you, he |
| MD | Modal | can, would, should |

**Example POS Tagging:**
```
If/IN you/PRP wish/VBP to/TO make/VB an/DT apple/NN pie/NN
```

---

### 1.16 Processing Indian Languages

**Challenges:**
- Different script systems (Devanagari, Tamil, Bengali, etc.)
- Conjunct characters
- Rich morphology (agglutinative features)
- Limited annotated resources

**Approaches:**
- Character-level processing
- Morphological analyzers
- Factored MT models
- Multilingual models

---

## UNIT II: SYNTACTIC & SEMANTIC ANALYSIS

### 2.1 Context-Free Grammar (CFG)

**Definition:** A formal grammar G defined as a 4-tuple:

```
G = (N, T, S, P)
```

Where:
- **N** = Set of non-terminal symbols (variables)
- **T** = Set of terminal symbols
- **S** = Start symbol (S ∈ N)
- **P** = Production rules (α → β)

**Rule Form:**
- Production: α → β
- α must contain at least one non-terminal
- β contains terminals and/or non-terminals

**Example Grammar:**
```
S     → NP VP
NP    → DET N | DET ADJ N | N
VP    → V | V NP | VP PP
PP    → P NP
DET   → the | a | an
N     → cat | dog | bird | telescope
V     → saw | likes | with
ADJ   → big | small | red
P     → with | under | on
```

**Derivations:**

For sentence "The cat saw the bird with the telescope":

**Rightmost Derivation:**
```
S
→ NP VP
→ NP V NP
→ DET N V NP
→ the N V NP
→ the cat V NP
→ the cat saw NP
→ the cat saw DET N
→ the cat saw the N
→ the cat saw the bird
```

Or with the alternative parsing:
```
S → NP VP
→ DET ADJ N VP
→ the ADJ N VP
→ the big N VP
→ the big bird VP
→ the big bird V PP
→ the big bird saw PP
→ the big bird saw NP
→ the big bird saw DET N
→ the big bird saw the telescope
```

This shows **syntactic ambiguity** — the phrase "with the telescope" can modify either "saw" (instrument) or "bird" (carrying).

---

### 2.2 Constituency vs Dependency Parsing

| Aspect | Constituency (Phrase Structure) | Dependency |
|--------|----------------------------------|------------|
| **Representation** | Hierarchical tree with phrases | Direct arcs between words |
| **Nodes** | Non-terminals (NP, VP) | Words only |
| **Edges** | Unlabeled | Labeled with grammatical relations |
| **Focus** | Phrasal structure | Grammatical relations |
| **Languages** | English, French | Czech, Turkish (free word order) |
| **Example** | Penn Treebank | Universal Dependencies |

**Constituency Parse Tree:**
```
        S
       / \
      NP  VP
     / \ / \
   DET N  V  NP
   /      / \
 the   cat  saw  DET N
               /   \
              the  bird
```

**Dependency Parse:**
```
     saw
    / | \
   |  |  telescope
   |  |    |
 the cat  the bird
```

---

### 2.3 CYK Parsing Algorithm (IMPORTANT!)

The CYK algorithm performs bottom-up parsing using dynamic programming.

**Prerequisite:** Grammar must be in **Chomsky Normal Form (CNF)**:
- A → BC (two non-terminals on RHS)
- A → a (one terminal on RHS)

**Algorithm Steps:**

```
CYK(w[1...n]):
    // Initialization: single words
    for i = 1 to n:
        for each production A → w[i]:
            table[i,i] = table[i,i] ∪ {A}
    
    // Combination: find larger constituents
    for length = 2 to n:          // length of substring
        for i = 1 to n-length+1:  // start position
            j = i + length - 1    // end position
            for k = i to j-1:     // split point
                for each production A → BC:
                    if B ∈ table[i,k] and C ∈ table[k+1,j]:
                        table[i,j] = table[i,j] ∪ {A}
    
    // Result: S in table[1,n] means valid sentence
    return table
```

**Time Complexity:** O(n³ × |P|)

#### **Worked Numerical Example:**

**Given Grammar (in CNF):**
```
S → AB | BC
A → BA | a
B → CC | b
C → AB | a
```

**String to parse:** "baa"

**Step 1: Initialization (Length 1)**
```
table[1,1]: w[1] = 'b'
            B → b  (rule B → CC uses 'b' as terminal? No, B → b)
            B → b  ✓
table[1,1] = {B}

table[2,2]: w[2] = 'a'
            A → a  ✓
            C → a  ✓
table[2,2] = {A, C}

table[3,3]: w[3] = 'a'
            A → a  ✓
            C → a  ✓
table[3,3] = {A, C}
```

**Step 2: Length 2**

**table[1,2]:** substring "ba"
- k=1: table[1,1]={B}, table[2,2]={A,C}
  - S → BC: B ∈ {B} ✓, C ∈ {A,C} ✓ → add S
  - A → BA: B ∈ {B} ✓, A ∈ {A,C} ✓ → add A
- table[1,2] = {S, A}

**table[2,3]:** substring "aa"
- k=2: table[2,2]={A,C}, table[3,3]={A,C}
  - S → BC: B ∈ {A,C} ✗
  - A → BA: B ∈ {A,C} ✗
  - C → AB: A ∈ {A,C} ✓, B ∈ {A,C} ✓ → add C
- table[2,3] = {C}

**Step 3: Length 3**

**table[1,3]:** substring "baa"
- k=1: table[1,1]={B}, table[2,3]={C}
  - S → BC: B ∈ {B} ✓, C ∈ {C} ✓ → add S
- k=2: table[1,2]={S,A}, table[3,3]={A,C}
  - S → BC: B ∈ {S,A} ✗
  - A → BA: B ∈ {S,A} ✓, A ∈ {A,C} ✓ → add A
  - C → AB: A ∈ {S,A} ✓, B ∈ {A,C} ✗
- table[1,3] = {S, A}

**Result:** S ∈ table[1,3] → **String is valid!**

---

### 2.4 Shift-Reduce Parsing

**Mechanism:**
1. **Shift:** Move next input token to stack
2. **Reduce:** When RHS of production is on stack top, replace with LHS

**Worked Example:**

Grammar:
```
S → NP VP
NP → DET N
VP → V NP
DET → the
N → cat | dog
V → saw | likes
```

Input: "the cat saw the dog"

| Step | Action | Stack | Input Remaining |
|------|--------|-------|-----------------|
| 1 | Shift | [the] | cat saw the dog |
| 2 | Reduce | [DET] | cat saw the dog |
| 3 | Shift | [DET, cat] | saw the dog |
| 4 | Reduce | [DET, N] | saw the dog |
| 5 | Reduce | [NP] | saw the dog |
| 6 | Shift | [NP, saw] | the dog |
| 7 | Shift | [NP, saw, the] | dog |
| 8 | Reduce | [NP, saw, DET] | dog |
| 9 | Shift | [NP, saw, DET, dog] | ε |
| 10 | Reduce | [NP, saw, DET, N] | ε |
| 11 | Reduce | [NP, saw, NP] | ε |
| 12 | Reduce | [NP, VP] | ε |
| 13 | Reduce | [S] | ε |

**Accept** — sentence successfully parsed!

---

### 2.5 Treebanks

**Definition:** A treebank is a collection of sentences, each annotated with its complete syntactic analysis (parse tree).

**Penn Treebank:**
- 40,000 sentences from Wall Street Journal
- Phrase structure annotations
- Used for training statistical parsers

**Utility of Treebanks:**
1. Direct grammar extraction
2. Training data for PCFG
3. Supervised learning of syntactic patterns

**Annotation Conventions:**
| Label | Meaning |
|-------|---------|
| SBARQ | Question (wh-movement) |
| WHNP | Wh-noun phrase |
| NP-SBJ | Noun phrase as subject |
| VP | Verb phrase |
| PP | Prepositional phrase |

---

### 2.6 Semantic Analysis

**Purpose:** Derive meaning from syntactic structure

**Requirements of Semantic Theory:**
1. Explain ambiguous meanings
2. Resolve word sense ambiguity
3. Identify meaningless but well-formed sentences
4. Handle paraphrases with same meaning

---

### 2.7 Meaning Representation

**Goal:** Create formal representations that computers can manipulate

**Properties:**
- Verifiable (can check truth conditions)
- Canonical (same meaning → same representation)
- Expressive (can represent all meanings)

---

### 2.8 Lexical Semantics

**Word Relationships:**

| Relation | Example |
|----------|---------|
| **Synonymy** | big ↔ large |
| **Antonymy** | hot ↔ cold |
| **Hypernymy** | animal → dog (dog is a hypernym of dog) |
| **Hyponymy** | dog → animal (dog is a hyponym of animal) |
| **Meronymy** | finger → hand |
| **Holonymy** | hand → finger |

---

### 2.9 Ambiguity Types

| Type | Definition | Example |
|------|------------|---------|
| **Lexical Ambiguity** | Word has multiple meanings | "bank" (financial/river) |
| **Syntactic Ambiguity** | Multiple parse trees | "I saw the man with the telescope" |
| **Semantic Ambiguity** | Meaning unclear | "The chicken is ready to eat" |
| **Pragmatic Ambiguity** | Context-dependent | "Can you reach the book?" |

---

### 2.10 Word Sense Disambiguation (WSD)

**Definition:** Determining which meaning of a word applies in a given context.

**Types of Word Ambiguity:**

| Type | Description | Example |
|------|-------------|---------|
| **Homonymy** | Same spelling, UNRELATED meanings | "Bat" (animal ↔ sports equipment) |
| **Polysemy** | Same spelling, RELATED meanings | "Bank" (financial ↔ river bank) |
| **Categorial Ambiguity** | Different parts of speech | "Book" (noun: reading material / verb: to reserve) |

> **Exam Tip:** Homonymy = Unrelated meanings, Polysemy = Related meanings

**WSD Approaches:**

**1. Dictionary-Based (Lesk Algorithm):**
- Choose the sense whose dictionary definition overlaps most with context
- Simple but limited

**2. Supervised Learning:**
- Train classifier on annotated data
- Features: bag-of-words, POS tags, collocations
- Best performance when sufficient labeled data

**3. Unsupervised Learning:**
- Cluster word uses
- Assign most frequent sense as default
- Bootstrapping methods

**4. Semi-Supervised:**
- Start with small labeled data
- Self-training to expand labeled set
- Combines advantages of supervised and unsupervised

---

## UNIT III: FEATURES, UNIFICATION & PROBABILISTIC PARSING

### 3.1 Feature Structures

**Definition:** Structured representation capturing linguistic properties using attribute-value pairs.

**Components:**
- **Type:** Category or sort of the structure
- **Features:** Attributes with values
- **Values:** Can be atomic (string, number) or complex (nested structure)

**Example — Person Entity:**
```
[PERSON
  NAME   "John"
  AGE    25
  SPOUSE [PERSON
           NAME "Mary"
           AGE  24]
]
```

**Feature Path:** SPOUSE.NAME accesses "Mary"

---

### 3.2 Unification

**Definition:** Operation that merges two feature structures into one, if they are compatible.

**Unification Conditions:**
1. Both atomic and equal → succeed
2. Both complex → recursively unify all features
3. One has feature, other doesn't → inherit
4. Incompatible values → **fail**

**Formal Definition:**
```
FS₁ ⊔ FS₂ = unified structure (if compatible)
FS₁ ⊔ FS₂ = FAIL (if incompatible)
```

#### **Worked Example:**

**FS₁:**
```
[AGR
  NUMBER sg
  PERSON 3
]
```

**FS₂:**
```
[AGR
  NUMBER sg
  PERSON 3
]
```

**Unification:**
```
Unify(FS₁, FS₂):
  Types match (AGR = AGR)
  Feature NUMBER: sg = sg →  sg
  Feature PERSON: 3 = 3 → 3
  Result: [AGR NUMBER sg PERSON 3]
```

**FS₃ (incompatible):**
```
[AGR
  NUMBER pl
  PERSON 3
]
```

**Unification with FS₃:**
```
Unify(FS₁, FS₃):
  Types match
  Feature NUMBER: sg ≠ pl → FAIL
```

---

### 3.3 Feature Structures in Grammar

**Applications in NLP:**

1. **Agreement:**
```
NP[NUM=sg] → DET[NUM=sg] N[NUM=sg]
NP[NUM=pl] → DET[NUM=pl] N[NUM=pl]
```

2. **Subcategorization:**
```
VP[TRANS=trans] → V[TRANS=trans] NP
VP[TRANS=intrans] → V[TRANS=intrans]
```

3. **Long-Distance Dependencies:**
```
WHNP[index=X] → who
S → WHNP S/X
```

---

### 3.4 Implementing Unification

**Algorithm Pseudocode:**
```
function unify(fs1, fs2):
    if fs1 is atomic and fs2 is atomic:
        return fs1 if fs1 == fs2 else FAIL
    if fs1 is atomic or fs2 is atomic:
        return FAIL
    // Both are complex structures
    result = copy(fs1)
    for each feature f in fs2:
        if f not in result:
            result[f] = fs2[f]
        else:
            result[f] = unify(result[f], fs2[f])
            if result[f] == FAIL:
                return FAIL
    return result
```

---

### 3.5 Parsing with Unification Constraints

**Benefits:**
- More expressive than CFG
- Early rejection of invalid parses
- Captures linguistic constraints

---

### 3.6 Probabilistic Context-Free Grammar (PCFG)

**Definition:** A CFG where each production has an associated probability.

**Constraint:**
```
Σ P(A → α) = 1  for all A ∈ N
```

**Rule Probability Estimation:**
```
P(A → α) = Count(A → α) / Σ Count(A → β) for all β
```

#### **Worked Example — PCFG Derivation:**

**Given Treebank with 3 trees:**
- Tree t₁ occurred 10 times
- Tree t₂ occurred 20 times
- Tree t₃ occurred 50 times

**From these, derive rule probabilities:**
```
P(NP → NP PP) = 0.125      // From analysis
P(NP → DET N) = 0.334
P(VP → VP PP) = 0.667
P(S → NP VP) = 1.0
```

---

### 3.7 PCFG Numerical Calculation (IMPORTANT!)

**Problem:** Parse the string "a a a" with the following PCFG:

```
P(NP → NP PP) = 0.25
P(NP → DET N) = 0.5
P(VP → VP PP) = 0.667
P(VP → V) = 0.333
P(PP → P NP) = 1.0
P(DET → a) = 0.7
P(N → a) = 0.3
P(V → a) = 0.5
P(P → a) = 0.2
```

**Two possible parse trees for "a a a":**

**Parse 1:** NP → DET N, VP → V, PP → P NP
- Rules: NP→DET N, VP→V, PP→P NP
- Probability:
```
P(Parse1) = P(NP→DET N) × P(DET→a) × P(N→a) × P(VP→V) × P(V→a)
          = 0.5 × 0.7 × 0.3 × 0.333 × 0.5
          = 0.01733
```

**Parse 2:** NP → NP PP, PP → P NP, VP → VP PP
- Rules: NP→NP PP, PP→P NP, VP→VP PP
- Probability:
```
P(Parse2) = P(NP→NP PP) × P(NP→DET N) × P(DET→a) × P(N→a)
          × P(PP→P NP) × P(P→a) × P(NP→DET N) × P(DET→a) × P(N→a)
          × P(VP→VP PP) × P(VP→V) × P(V→a)
```

This calculation becomes complex. The point is: **Parse 2 wins** because NP→NP PP has higher probability (0.25 vs 0.5 for NP→DET N being split).

---

### 3.8 Problems with PCFGs (Important!)

| Problem | Description |
|---------|-------------|
| **Independence Assumption** | Assumes no context between rules |
| **Lack of Lexical Dependencies** | Doesn't incorporate word-specific info |
| **Poor Long-Distance** | Can't capture subject-verb agreement |
| **Context Insensitivity** | Same probability for all contexts |
| **Attachment Ambiguity** | PP attachment, NP attachment |

---

### 3.9 Generative vs Discriminative Models

| Aspect | Generative | Discriminative |
|--------|-----------|----------------|
| **Models** | P(X, Y) — joint distribution | P(Y\|X) — conditional |
| **Goal** | How X generates Y | Given X, predict Y |
| **Examples** | HMM, Naive Bayes, PCFG | SVM, Logistic Regression, CRF |
| **Advantages** | Preprocessing, synthesis | Better classification performance |
| **Use Cases** | Language modeling, parsing | Text classification, WSD |

---

### 3.10 Conditional Random Fields (CRF)

**For Structured Prediction:**

**Score Function:**
```
Score(y, x) = Σ λᵢ × fᵢ(x, y)
```

**Conditional Probability:**
```
P(y|x) = exp(Score(y,x)) / Σ exp(Score(y',x))
```

**Advantages:**
- Models entire output structure
- Not restricted to local features
- Better for sequence labeling tasks

---

## UNIT IV: DISCOURSE PROCESSING & NLG

### 4.1 Discourse Processing

**Definition:** Building theories and models of how utterances form coherent discourse.

**Key Question:** What makes a collection of sentences a coherent discourse?

---

### 4.2 Cohesion

**Definition:** Linguistic devices that tie textual units together.

**Three Main Classes:**

| Type | Description | Example |
|------|-------------|---------|
| **Lexical Overlap** | Same words repeated | "The car" ... "The car was red" |
| **Coreference Chains** | Referring expressions link | "John ... he ... his" |
| **Cue Words** | Discourse markers | "However", "Moreover", "Therefore" |

---

### 4.3 Coherence Relations (IMPORTANT!)

**Definition:** Semantic relations that hold between discourse segments.

| Relation | Meaning | Example |
|----------|---------|---------|
| **Result** | S₀ causes S₁ | "It rained. The ground is wet." |
| **Explanation** | S₁ explains S₀ | "He was drunk. Ram fought." |
| **Parallel** | Similar patterns | "Ram wanted car. Shyam wanted money." |
| **Elaboration** | Same proposition | "Ram was from Chandigarh. Shyam was from Kerala." |
| **Occasion** | State change across | "Ram picked up the book. He gave it to Shyam." |

---

### 4.4 Reference Resolution

**Key Terminology:**

| Term | Definition | Example |
|------|------------|---------|
| **Referring Expression** | Expression used to refer | "he" in "Ram... he..." |
| **Referent** | Entity being referred to | "Ram" |
| **Corefer** | Two expressions for same entity | "Ram" and "he" |
| **Antecedent** | Entity that licenses reference | "Ram" for "he" |
| **Anaphora** | Reference to prior entity | "he" referring to "Ram" |
| **Discourse Model** | Representation of discourse entities | Mental model |

---

### 4.5 Types of Referring Expressions

| Type | Description | Example |
|------|-------------|---------|
| **Indefinite Noun Phrase** | New entity to hearer | "a book", "some food" |
| **Definite Noun Phrase** | Known entity | "the book", "The Times" |
| **Pronoun** | Definite reference | "he", "she", "it" |
| **Demonstrative** | Points to entity | "this", "that" |
| **Name** | Proper noun | "Ram", "Delhi" |

---

### 4.6 Coreference Resolution

**Task:** Find all expressions referring to the same entity.

**Output:** Coreference chains

**Example:**
```
Input: "Ram met Shyam at the mall. He shook his hand."
Output: [{Ram, He}, {Shyam, his}]
```

**Challenges:**
- Pronoun "it" has many uses
- Ambiguous references
- Implicit entities

---

### 4.7 Pronominal Anaphora Resolution

**Task:** Find antecedent for a specific pronoun.

**Algorithm Approach:**
1. Find possible antecedents in preceding context
2. Score based on grammatical role (subject preference)
3. Apply constraints (binding theory)
4. Select best candidate

---

### 4.8 Natural Language Generation (NLG)

**Definition:** Producing natural language output from computer representation.

#### **NLG Architecture:**

```
┌─────────────────────────────────────────────────────┐
│                  TEXT PLANNING                       │
│  • Content Determination                            │
│  • Document Structuring                              │
└─────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│               SENTENCE PLANNING                      │
│  • Sentence Segmentation                            │
│  • Lexical Choice                                    │
│  • Referring Expression Generation                    │
└─────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│               SURFACE REALIZATION                    │
│  • Linearization                                     │
│  • Morphology                                        │
│  • Punctuation                                        │
└─────────────────────────────────────────────────────┘
```

#### **Generation Tasks:**

| Task | Description |
|------|-------------|
| **Content Determination** | What to say |
| **Text Structuring** | How to organize |
| **Sentence Aggregation** | Combine information |
| **Lexicalization** | Word choice |
| **Reference Resolution** | Pronouns, determiners |
| **Realization** | Grammatical output |

---

### 4.9 Discourse Segmentation

**Task:** Divide text into topically coherent segments.

**Methods:**

| Method | Description | Data Needed |
|--------|-------------|-------------|
| **Unsupervised** | Linear segmentation | No labels |
| **Supervised** | Classification | Labeled boundaries |
| **Text Tiling** | Lexical cohesion | No labels |

**Text Tiling Algorithm:**
1. Compute similarity between consecutive blocks
2. Identify gaps where similarity drops below threshold
3. These gaps are segment boundaries

---

## UNIT V: MACHINE TRANSLATION

### 5.1 Machine Translation (MT) Problems

| Problem | Description | Example |
|---------|-------------|---------|
| **Word Sense Ambiguity** | Same word, different meanings | "bank" (financial/river) |
| **Syntactic Differences** | Word order varies | English (SVO) vs Japanese (SOV) |
| **Morphological Variation** | Inflection differences | Spanish "hablo" vs "hablé" |
| **Lexical Gaps** | No direct translation | German "Schadenfreude" |
| **Idioms** | Non-compositional | "kick the bucket" |
| **Coreference** | Cross-lingual reference | Pronoun resolution |

---

### 5.2 MT Approaches

#### **1. Direct Machine Translation (DMT)**

**Characteristics:**
- Minimal analysis
- Word-for-word translation
- Dictionary lookup
- Simple reordering

**Process:**
```
Source Text → Dictionary Lookup → Simple Transfer → Target Text
```

**Limitations:**
- Only works for closely related languages
- No deep understanding
- Poor handling of idioms

---

#### **2. Rule-Based MT (RBMT)**

**Components:**
1. **Bilingual Dictionary** — Word translations
2. **Morphological Analyzer** — Handles inflections
3. **Syntax Rules** — Structural transfer
4. **Semantic Rules** — Meaning transfer

**Architecture:**
```
Source → Analysis → Transfer → Generation → Target
         (Morph,   (Lexical,  (Morph,
          Syntax)    Syntax)    Syntax)
```

**Advantages:**
- Transparent and interpretable
- Good for limited domains
- Consistent translations

**Disadvantages:**
- Labor-intensive rule creation
- Poor generalization
- Requires expert linguists

---

#### **3. Corpus-Based MT (CBMT)**

##### **Statistical MT (SMT):**

**Training Data:** Parallel corpora (aligned source-target sentence pairs)

**IBM Models (1-5):**
| Model | Description |
|-------|-------------|
| Model 1 | Word-based translation, uniform fertility |
| Model 2 | Adds absolute position |
| Model 3 | Adds fertility model |
| Model 4 | Adds relative position |
| Model 5 | Adds headword heuristic |

**Phrase-Based MT:**
- Learns phrase alignments
- More flexible than word-based
- Current standard baseline

**Decoding:**
- Search for highest probability translation
- Dynamic programming for efficiency

##### **Neural MT (NMT):**

**Architecture:** Sequence-to-Sequence with Attention

```
Encoder (RNN/LSTM/Transformer) → Attention → Decoder (RNN/LSTM/Transformer)
   Source embedding                    Target embedding
```

**Advantages:**
- End-to-end learning
- Better handling of long sequences
- Captures context better
- Produces more fluent translations

**Disadvantages:**
- Requires large training data
- Computationally expensive
- Less interpretable

---

### 5.3 Translation involving Indian Languages

**Challenges:**
- Rich morphology (Tamil, Hindi, etc.)
- Free word order
- Limited parallel corpora
- Script variations

**Solutions:**
1. **Morphological preprocessing** — Reduce inflected forms
2. **Factored MT models** — Include morphological features
3. **Multilingual models** — Share representations across languages
4. **Transfer-based approaches** — Grammar transfer

---

### 5.4 MT Evaluation Metrics

| Metric | Description |
|--------|-------------|
| **BLEU** | n-gram precision vs reference |
| **METEOR** | Harmonic mean of precision and recall |
| **TER** | Translation edit rate |
| **NIST** | Weighted n-gram precision |

**BLEU Score Calculation:**
```
BLEU = BP × exp(Σ wₙ log Pₙ)
where BP = brevity penalty
      Pₙ = n-gram precision
```

---

## IMPORTANT FORMULAS SUMMARY

### Language Modeling

```
P(wₙ|wₙ₋₁) = C(wₙ₋₁, wₙ) / C(wₙ₋₁)                    // MLE
Perplexity = P(w₁...wₙ)^(-1/N)                        // Perplexity
P*(wᵢ) = (cᵢ + 1) / (N + V)                           // Laplace Smoothing
P*(wᵢ) = (cᵢ + k) / (N + kV)                          // Add-k Smoothing
```

### PCFG

```
P(T) = ∏ P(rule)                                      // Parse tree probability
P(rule) = Count(rule) / Count(all rules for LHS)      // Rule probability
```

### TF-IDF

```
TF(t,d) = count(t,d) / |d|                            // Term frequency
IDF(t,D) = log(N / |{d∈D: t∈d}|)                      // Inverse document frequency
TF-IDF = TF × IDF                                      // Combined score
```

---

## KEY DIFFERENCES FOR EXAM

| Topic | A | B | Exam Tip |
|-------|---|---|----------|
| **Unigram vs Bigram** | Independent words | Depends on previous word | Bigram captures local context |
| **Top-down vs Bottom-up** | Starts from S | Starts from input words | Top-down uses prediction |
| **Constituency vs Dependency** | Phrase structure | Word-to-word relations | Dependency better for free word order |
| **Homonymy vs Polysemy** | Unrelated meanings | Related meanings | Homonym = separate origins |
| **Generative vs Discriminative** | P(X,Y) joint | P(Y\|X) conditional | Generative models data, discriminative models labels |
| **Smoothing vs Backoff** | Redistribute probability | Use lower-order model | Backoff only when evidence is zero |
| **CYK vs Shift-Reduce** | Bottom-up DP | Shift/reduce operations | CYK needs CNF form |
| **Result vs Explanation** | Cause → effect | Effect ← explanation | Result: rain → wet ground |

---

## EXAM PRACTICE NUMERICALS

### Numerical 1: Bigram Probability

**Question:** Given the corpus:
```
<s> I like chocolate </s>
<s> I like tea </s>
<s> chocolate is good </s>
```

Calculate:
a) P(like|I)
b) P(chocolate|like)
c) P(</s>|good)

**Solution:**
```
Total tokens: 15 (including <s> and </s>)

Unigram counts:
I: 2, like: 2, chocolate: 2, tea: 1, is: 1, good: 1
<s>: 3, </s>: 3

Bigram counts:
C(I, like) = 2
C(like, chocolate) = 1
C(like, tea) = 1
C(</s>, good) = 0 (but we need C(good, </s>)?)
C(chocolate, is) = 1
C(is, good) = 1
C(good, </s>) = 1

a) P(like|I) = C(I, like) / C(I) = 2/2 = 1.0

b) P(chocolate|like) = C(like, chocolate) / C(like) = 1/2 = 0.5

c) P(</s>|good) = C(good, </s>) / C(good) = 1/1 = 1.0
```

---

### Numerical 2: Perplexity Calculation

**Question:** A language model assigns the following probabilities to a 4-word sentence:
```
P(w₁|<s>) = 0.25
P(w₂|w₁) = 0.5
P(w₃|w₂) = 0.1
P(w₄|w₃) = 0.2
```

Calculate the perplexity of the sentence.

**Solution:**
```
Joint probability = 0.25 × 0.5 × 0.1 × 0.2 = 0.0025

Perplexity = P(w₁...w₄)^(-1/4)
           = (0.0025)^(-0.25)
           = (400)^(0.25)
           = 400^(1/4)
           = 4.0
```

---

### Numerical 3: CYK Parsing

**Question:** Using the grammar:
```
S → AB | BC
A → BA | a
B → CC | b
C → AB | a
```

Show whether "aba" can be generated by the grammar.

**Solution:**
```
String: "aba", length = 3

Initialization (length 1):
table[1,1]: 'a' → A, C (from A→a, C→a)
table[2,2]: 'b' → B (from B→b)
table[3,3]: 'a' → A, C

Length 2:
table[1,2] = { } (no valid combinations for "ab")
table[2,3]: check k=2
  - S→BC: B∈{B}? No

Length 3 (whole string):
table[1,3], k=1: S→BC, B∈{A,C}? No
table[1,3], k=2: S→BC, B∈{ }? No
Result: S ∉ table[1,3]

"aba" CANNOT be generated by this grammar.
```

---

### Numerical 4: PCFG Parse Probability

**Question:** Given the PCFG:
```
S → NP VP [1.0]
NP → DET N [0.4]
NP → N [0.3]
NP → DET ADJ N [0.3]
VP → V [0.5]
VP → V NP [0.5]
DET → the [1.0]
N → dog [0.6]
N → cat [0.4]
V → sees [1.0]
ADJ → big [1.0]
```

Calculate probability for parse tree: "the big dog sees"

```
S
└── NP
    ├── DET → the
    ├── ADJ → big
    └── N → dog
└── VP
    └── V → sees
```

**Solution:**
```
P(tree) = P(S→NP VP) × P(NP→DET ADJ N) × P(DET→the) × P(ADJ→big) × P(N→dog) × P(VP→V) × P(V→sees)

         = 1.0 × 0.3 × 1.0 × 1.0 × 0.6 × 0.5 × 1.0
         = 0.09
```

---

### Numerical 5: Unification

**Question:** Unify the following feature structures:

**FS₁:**
```
[PERSON
  NAME "Alice"
  AGE 30
]
```

**FS₂:**
```
[PERSON
  AGE 30
  OCCUPATION "Engineer"
]
```

**Solution:**
```
Unify(FS₁, FS₂):
  1. Types match: PERSON = PERSON ✓
  2. Feature AGE: 30 = 30 → 30 ✓
  3. Feature NAME: present in FS₁, not in FS₂ → keep from FS₁ ("Alice")
  4. Feature OCCUPATION: present in FS₂, not in FS₁ → add from FS₂ ("Engineer")

Result:
[PERSON
  NAME "Alice"
  AGE 30
  OCCUPATION "Engineer"
]
```

---

## SUMMARY TABLE: NLP TASKS AND THEIR PURPOSES

| Task | Input | Output | Example |
|------|-------|--------|---------|
| **Tokenization** | Text | Words | "Hello world!" → ["Hello", "world", "!"] |
| **POS Tagging** | Words | Tags | ["cat", "runs"] → [NN, VBZ] |
| **Parsing** | Sentence | Tree | "The cat sat" → Parse tree |
| **NER** | Text | Entities | "John works at Google" → [John-PER, Google-ORG] |
| **WSD** | Word+Context | Sense | "bank" in "river bank" → financial |
| **Coreference** | Text | Chains | "Ram... he..." → [(Ram, he)] |
| **Translation** | Text (lang A) | Text (lang B) | "Hello" (EN) → "Hola" (ES) |

---

## FINAL EXAM TIPS

### High-Frequency Topics (by importance):

1. **N-gram Models** — Unigram, Bigram, Trigram calculations
2. **Perplexity** — Formula and interpretation
3. **Smoothing** — Laplace, Add-k, Backoff, Interpolation
4. **CFG** — Grammar notation and derivations
5. **CYK Algorithm** — Table construction and parsing
6. **PCFG** — Rule probability and parse probability
7. **Unification** — Feature structure merging
8. **Ambiguity Types** — Homonymy, Polysemy distinction
9. **Discourse Relations** — Result, Explanation, Parallel
10. **MT Approaches** — DMT, RBMT, SMT, NMT differences

### Common Mistakes to Avoid:

| Mistake | Correction |
|---------|------------|
| Confusing perplexity with accuracy | Lower perplexity = better model |
| Forgetting start/end tokens | Always add `<s>` and `</s>` |
| Confusing Homonymy with Polysemy | Homonymy = unrelated, Polysemy = related |
| CYK requires CNF form | Convert grammar first |
| PCFG probabilities must sum to 1 | Check for each LHS |

### Time Management:

1. Read all questions first
2. Start with numerical problems (easier to verify)
3. Write key formulas first, then fill explanation
4. Draw parse trees carefully and label nodes
5. For long answers, use bullet points with examples

---

**End of NLP Exam Notes**