# discourseCoherenceMetrics

The discourseCoherenceMetrics project introduces new LLM-based metrics that researchers can use to quantify the coherence of text documents.

## Basic Idea

This framework leverages BERT, S-BERT, and S3BERT sentence-level embeddings to quantify the coherence of text documents. The novel metrics leverage cosine similarities of sentence-level embeddings and distance-based metrics (k-means inertia and Euclidean distance) to quantify coherence in discourse. 

## Installation

Clone the repository and check dependencies. Use Python Version 3.14.3. 

``git clone https://github.com/Kstar125/discourseCoherenceMetrics``

Please ensure that the following packages are installed if attempting to run included scripts:

| package | version |
| :--- | :--- |
| torch | 2.11.0 |
| pandas | 3.0.1 |
| numpy | 2.4.3 |
| scikit-learn | 1.8.0 |

## Usage

The included scripts document the performance of the new coherence metrics in two tasks. 

1) **Cloze Story Test**: Aims to select human-labelled coherent ending continuations over less coherent ending alternatives (See story dataset at: http://cs.rochester.edu/nlp/rocstories).

Novel metrics achieve up to ~65% accuracy in identifying correct narrative endings from the ROCStories Corpus narratives, 5% higher than prior computational benchmarks. 

Implementation found in similarityMetrics.ipynb and distanceMetrics.ipynb; corresponding spreadsheets of results are included in the /rocStoriesSpreadsheets directory. 

2) **Narrative Categorization Task**: Aims to categorize stories by story type, imagined or recalled, based on the quality of narrative flow (See story dataset at: https://www.microsoft.com/en-us/research/publication/recollection-versus-imagination-exploring-human-memory-and-cognition-via-neural-language-models/).

Novel metrics identify quantitative differences in the quality of narrative flow between recalled and imagined stories from the HippoCorpus Version 3 dataset, achieving up to a 70-30 split between story categories.

Implementation found in hippoCorpusV3Analyses.ipynb; corresponding spreadsheets of results are included in the /hippoCorpusSpreadsheets directory. 

> **Note:** Check associations.txt in each spreadsheet directory for a mapping of spreadsheet results to their corresponding implementations.

## License

This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc/4.0/

You are free to: \
Share — copy and redistribute the material in any medium or format \
Adapt — remix, transform, and build upon the material \
The licensor cannot revoke these freedoms as long as you follow the license terms. 

Under the following terms: \
Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use. \
Non-Commercial — You may not use the material for commercial purposes. \
No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits. 

Notices: \
You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable exception or limitation. \
No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.

## Acknowledgments

The work in the Cloze Story Test derives from and uses stories from the ROCStories Corpus collected and curated by Mostafazadeh, N., Chambers, N., He, X., Parikh, D., Batra, D., Vanderwende, L., Kohli, P., Allen, J. (2016). A Corpus and Evaluation Framework for Deeper Understanding of Commonsense Stories. In *Proceedings of the 2016 North American Chapter of the ACL (NAACL HTLT)*, 2016. https://aclanthology.org/N16-1098.pdf

The work in the Narrative Categorization Task derives from and uses stories from the HippoCorpus dataset collected and curated by Sap, M., Horvitz, E., Choi, Y., Smith, N. A., & Pennebaker, J. (2020). Recollection versus Imagination: Exploring Human Memory and Cognition via Neural Language Models. In *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics*, pages 1970–1978, Online. Association for Computational Linguistics. https://aclanthology.org/2020.acl-main.178/

The implementation of S3BERT in the current project follows the approach provided by Opitz, J., & Frank, A. (2022). SBERT studies meaning representations: Decomposing sentence embeddings into explainable semantic features. In He, Y., Ji, H., Li, S., Liu, Y., and Chang, C.-H., editors, *Proceedings of the 2nd Conference of the Asia-Pacific Chapter of the Association for Computational Linguistics and the 12th International Joint Conference on Natural Language Processing (Volume 1: Long Papers)*, pages 625–638, Online only. Association for Computational Linguistics. https://aclanthology.org/2022.aacl-main.48.pdf \
See repository at: https://github.com/flipz357/S3BERT

The implementation of S-BERT in the current project follows the approach provided by Reimers, N., & Gurevych, I. (2019). Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks. In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing, pages 3982–3992, Hong Kong, China, November 3 – 7. 2019. Association for Computational Linguistics. https://aclanthology.org/D19-1410/

## Contact

Email: korey.millerboyle@alumni.utoronto.ca

