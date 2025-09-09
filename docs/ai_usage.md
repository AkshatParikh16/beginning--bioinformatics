AI Use Log – Beginning Bioinformatics (Part 3)
I wrote and tested all final code myself. AI was used as a support tool for scaffolding and reminders. Below are the specific instances, organized in order of use.

Entry 1 — GitHub + Colab Setup
Tool/model & version: ChatGPT (GPT-5)
What I asked for: A checklist to create a GitHub repository, add docs/ and notebooks/, save a Colab notebook as Bioinformatics_Module03.ipynb, and tag the repo for submission.
Snippet of prompt(s): “I’m new to Git + Colab—give me step-by-step with exact paths and the tag link I should submit.”
What I changed before committing: Wrote my own README line with name/UTA ID/section, reworded commit messages for clarity, and kept the repo public.
How I verified correctness: Confirmed the notebook appeared in /notebooks/, that docs/ai_usage.md rendered properly, and that the tag link had the correct /tree/week3-submission path.

Entry 2 — Practice Tasks P6–P8 (Input, Lists, Slicing)
Tool/model & version: ChatGPT (GPT-5)
What I asked for: Minimal, runnable snippets for input(), list insert/append/replace, and basic string/list slicing.
Snippet of prompt(s): “Give me minimal snippets for P6–P8 that I can paste into Colab.”
What I changed before committing: Renamed some variables, added comments on indexing and slice ranges, and included print statements for clarity.
How I verified correctness: Ran each snippet in Colab; checked that outputs matched expectations (e.g., my_list[2:4] → ["World", "Alfred R. Wallace"]).

Entry 3 — Rosalind #7 (DNA → RNA)
Tool/model & version: ChatGPT (GPT-5) + Biopython (Bio.Seq.Seq)
What I asked for: A script to safely read a single-line DNA file, filter invalid characters, and transcribe T→U.
Snippet of prompt(s): “My dataset has stray text. Help me filter to A/C/G/T and then do DNA→RNA cleanly.”
What I changed before committing: Simplified cleaning step to ''.join(ch for ch in raw.upper() if ch in "ACGT") and kept a plain-Python fallback (dna.replace("T","U")).
How I verified correctness: Compared DNA and RNA lengths, checked first/last 50 characters, and ensured output was a continuous string without spaces.

Entry 4 — Tasks P13–P15 (File I/O + Looping)
Tool/model & version: ChatGPT (GPT-5)
What I asked for: Patterns for read(), readline(), readlines(), correct use of join(), and avoiding extra newlines in loops.
Snippet of prompt(s): “Show me clean file-reading examples and how to avoid the extra newline in a loop.”
What I changed before committing: Used print(line.rstrip()), applied enumerate(..., start=1) for even-line selection, and documented why.
How I verified correctness: Tested with a small practice.txt; confirmed correct even-line outputs and no blank lines.

Entry 5 — Dictionaries + Word Count (Rosalind #5)
Tool/model & version: ChatGPT (GPT-5)
What I asked for: Concise Counter solution and a dictionary-only version, including a variant counting only first-seen words.
Snippet of prompt(s): “Give me a short word-count solution and one using .count() only for unseen tokens.”
What I changed before committing: Kept the Counter version, printed results in sorted order for consistency.
How I verified correctness: Compared outputs against a toy example (red red blue red → red:3, blue:1).

Entry 6 — FASTA + GC% (Rosalind #9)
Tool/model & version: ChatGPT (GPT-5) + Biopython (SeqIO.parse, SeqUtils.gc_fraction)
What I asked for: A script to parse FASTA, calculate GC%, and report the sequence with highest GC.
Snippet of prompt(s): “Small script to parse FASTA, compute GC%, and track the max GC record—keep it readable.”
What I changed before committing: Rounded GC% to six decimals to match Rosalind outputs; added guard for empty sequences.
How I verified correctness: Ran on sample FASTA; manually checked one sequence; confirmed max-GC ID matched manual calculation.

Closing Note
AI was used as a support tool for scaffolding and reminders. I rewrote and cleaned final code to fit assignment requirements, and I confirmed correctness through small tests and sample data before committing.
