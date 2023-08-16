# Construction Management Systems (CMS) Domain Corpora

This repository contains the first CMS domain corpus constructed from academic publications pertinent to CMS for the paper "Developing First Corpus in Construction Management Systems (CMS) Domain and Pre-trained Domain-specific Language Models".

## Data Collection Procedure

* Source: The corpus is comprised of scholarly journal papers, conference papers, articles, whitepapers, and select books related to CMS.
* Collection: Academic publications were retrieved from the first 99 pages of Google Scholar search results using the keyword "construction management".
* Volume: Out of 732 earmarked papers, 60 were discarded due to text recognition issues in older PDFs. The corpus has:
  * 5.7 million words in total.
  * 4.5 million words excluding references.
  * 7.7 million tokens.
  * 5.8 million tokens excluding references (processed with BERT tokenizer).
  * Over 90% of sentences are less than 40 tokens long.

## Data Cleaning and Pre-processing

The CMS Domain corpus underwent rigorous cleaning and pre-processing. The steps included:

1. PDF to Text: Automatic conversion of PDF files to plain text using Adobe Automation.
2. URL Removal: Exclusion of website links that may not provide substantive content.
3. Language Filter: Retention of only English text on the paragraph level, discarding unrecognizable characters and non-English content.
4. Sentence Segmentation: Division of paragraphs into distinct sentences, and removal of paragraphs without terminal punctuation marks.
5. Short Sentence Filter: Eradication of extremely short sentences to eliminate traces of formulas and tables.
6. Reference Filtering: Exclusion of references within papers to focus on context-rich content. Two datasets, with and without references, were generated.
7. Duplicate Removal: Ensuring the uniqueness of each sentence by removing duplicates.
8. Post cleaning, approximately 5% of the words in the original dataset were removed. During the reference filtering process, an additional 20% reduction in word count was observed.

## Note on the Released Data

This repository presents both the raw, uncleaned, and unprocessed data and the cleaned data. Recognizing that no universally optimal pre-processing procedure exists for all tasks, we've provided the unprocessed data to allow researchers the flexibility to adopt or design preprocessing methods tailored to their specific requirements.
