# Supplementary material

Supplementary data for the article *"Understanding cognitive capture as a multidimensional phenomenon: A review on sociotechnical amplification of cognitive biases"*.

The repository contains the materials needed to reproduce the two analyses in the article: (1) a scoping review of review publications and (2) a bibliometric analysis of 950 Scopus documents.

## 1. Scoping review

**Search date:** 30 March 2026
**Databases:** Scopus and Google Scholar
**Publication window:** 2020–2025
**Document type:** reviews

Search string:

```
TITLE-ABS-KEY ( "cognitive bias*" OR "shortcut*" OR "heuristic*" ) AND ( "digital platform*" OR "online platform*" OR "social media" OR "digital media" OR "online media" OR "online environment*" OR "digital ecosystem*" OR "algorithmic system*" OR "recommender system*" OR "digital infrastructure*" ) AND PUBYEAR > 2009 AND ( LIMIT-TO ( DOCTYPE , "re" ) )```

The 32 reviews included after screening are listed in `Articles reviewed in scoping review.docx`.

---

## 2. Bibliometric analysis

**Search date:** 11 September 2026
**Database:** Scopus and 
**Language:** English

Search string:

```
TITLE-ABS-KEY ( "Cognitive bias" OR "Cognitive biases" OR "Cognitive Shortcut" OR "Cognitive shortcuts" OR "Cognitive vulnerability" OR "Cognitive vulnerabilities" OR "Mental shortcuts" OR "mental shortcut" OR "Cognitive heuristic*" OR "socio-cognitive bias*" OR "Confirmation bias" OR "Social proof" OR "Bandwagon effect" OR "*group bias*" OR "Salience bias*" OR "Authority bias*" OR "Negativ* bias" OR "Optimis* bias" OR "Sequential bias" OR "Sequential effect" OR "overconfidence bias" OR "Anchoring bias" OR "Availability heuristic*" OR "Exposure bias" OR "Framing bias" OR "Status quo bias" OR "Loss aversion" OR "social identity bias" OR "*group bias" OR "cognitive heuristic*" OR "heuristic reasoning" OR "rule of thumb*" OR "human bias" OR "heuristic* cue*" OR "illusory truth effect" OR "frequency illusion" OR "herding behaio*r" OR "automation bias" ) AND TITLE-ABS-KEY ( "Digital media" OR "Social Media" OR "Digital platform" OR "Digital Platforms" OR "Recommender System" OR "Recommender Systems" OR "digital infrastructure" OR "Digital infrastructures" OR "Information platform" OR "Information platforms" OR "online environment" OR "online environments" OR "online ecosystem" OR "online ecosystems" OR "algorithmic curation" OR "online space" OR "online spaces" OR "platform ecosystem" OR "platform ecosystems" OR "social network* site" OR "online social network" OR "online media" OR "search enginge*" ) AND PUBYEAR > 2009 AND ( LIMIT-TO ( DOCTYPE , "re" ) OR LIMIT-TO ( DOCTYPE , "ch" ) OR LIMIT-TO ( DOCTYPE , "cp" ) OR LIMIT-TO ( DOCTYPE , "ar" ) OR LIMIT-TO ( DOCTYPE , "sh" ) OR LIMIT-TO ( DOCTYPE , "bk" ) OR LIMIT-TO ( DOCTYPE , "dp" ) ) AND ( LIMIT-TO ( LANGUAGE , "English" ) )```
```

The search returned 1,278 documents. After screening against the exclusion criteria described in the article, the final corpus comprises 950 documents. Disciplinary sub-corpora were defined using the Scopus subject classification. Some documents are classified in both computer science and social science and therefore contribute to both sub-corpora.

### Data licensing

The corpus was retrieved from Scopus, whose terms of use do not permit redistribution of the records (abstracts, keywords or reference lists). We therefore provide only bibliographic identifiers together with the derived network tables reported in the article.

### Analysis

All analyses were conducted in Biblioshiny, the web interface of the R package `bibliometrix`. Networks were built for the full corpus and for the computer science (CS) and social science (SS) sub-corpora.

## 3. Files

### Corpus

| File | Content |
|---|---|
| `corpus_950.csv` | DOI, title, publication year and disciplinary classification (computer science / social science) of the 950 documents |
| `Articles reviewed in scoping review.docx` | The 32 reviews included in the scoping review |

### Co-occurrence networks

Node tables with cluster membership, betweenness, closeness and PageRank.

| File | Corpus | Unit |
|---|---|---|
| `Co-occurrence_key_all_corpus.xlsx` | Full corpus | Author keywords |
| `Co-occurrence_abs_all_corpus.xlsx` | Full corpus | Abstract bi-grams |
| `Co_occurrence_abs_CS.xlsx` | Computer science | Abstract bi-grams |
| `Co_occurrence_Network_Abs_SS.xlsx` | Social science | Abstract bi-grams |

### Co-citation networks

Node tables with cluster membership, betweenness, closeness and PageRank.

| File | Corpus |
|---|---|
| `CoCitation_Network_2026_all_corpus.xlsx` | Full corpus |
| `CoCitation_Network_CS.xlsx` | Computer science |
| `CoCitation_Network_SS.xlsx` | Social science |

### Additional figures and analyses

| File | Content |
|---|---|
| `Co_occurrence_Network_Key_CS.png` | Author-keyword co-occurrence network, computer science |
| `Co_occurrence_Network_Key_CS.xlsx` | Computer science | Author keywords |
| `Co_occurrence_Network_Key_SS.png` | Author-keyword co-occurrence network, social science |
| `Co_occurrence_Network_Key_SS.xlsx` | Social science | Author keywords |
| `Performance Analysis.docx` | Performance analysis of the full corpus |

### Text preprocessing

| File | Content |
|---|---|
| `stopword_WSM.txt` | Custom stopword list removed before the co-occurrence analyses |
| `synonym.txt` | Synonym list used to merge term variants (e.g. singular and plural forms) |
