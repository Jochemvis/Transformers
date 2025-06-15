# Evaluating Transformer-Based Bible Translations (M2M-100)

This project investigates how effectively the multilingual transformer model M2M-100 translates Bible texts into English. Translations from four source languages—Finnish, Dutch, Russian, and Spanish—were evaluated using three metrics: CHRF++, sacreBLEU, and COMET. The model’s performance was analyzed on both the Old and New Testament to assess translation quality across languages and text types.
The repository contains scripts for running the translation on both testaments as well as notebooks for visualizing and analyzing the results.

The analysis began by determining the most suitable evaluation metric. COMET emerged as the most reliable, as it captures both lexical and semantic aspects of translation and aligns closely with human judgment. Therefore, the remainder of the study uses COMET as the primary metric.

Surprisingly, the Finnish-English translations achieved the highest scores, despite Finnish being a low-resource language and structurally distant from English. This strong performance appears to result from close alignment between the Finnish source and the English target version. Spanish-English also scored well, followed by Russian-English. Dutch-English performed the worst, likely due to the paraphrased nature and differing source base of the Dutch translation used in the dataset.

When comparing translation quality between the Old and New Testament, the New Testament slightly outperformed the Old. However, this pattern varied per language. For instance, Finnish and Russian performed equally well or better on the Old Testament, while Spanish maintained high performance across both. These results show that translation quality is shaped by multiple factors, including language pair compatibility, source text characteristics, and the quality of training data.

In conclusion, while the M2M-100 model performed well overall, translation effectiveness varied depending on language and source characteristics. The results demonstrate that high-quality machine translation depends on more than linguistic similarity—it also requires alignment in style, structure, and dataset quality.
