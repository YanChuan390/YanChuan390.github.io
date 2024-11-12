---
title:          "Investigating Documented Privacy Changes in Android OS"
date:           2024-07-12 00:01:00 +0800
selected:       true
pub:            "<span style='display: inline-block; padding: 2px 6px; font-size: 12px; font-weight: bold; color: white; background-color: #4CAF50; border-radius: 4px;'>CCF-A</span> <strong><em>FSE'24: Proceedings of the ACM on Software Engineering, Volume 1, Issue FSE</em></strong>"
# pub_pre:        "Submitted to "
# pub_post:       'Under review.'
# pub_last:       ' <span class="badge badge-pill badge-publication badge-success">Spotlight</span>'
pub_date:       "2024"

abstract: >-
   We conduct the first systematic study on the consistency between the operational behaviors of the OS at runtime and the officially disclosed DPCs. We propose DopCheck, an automatic DPC-driven testing framework equipped with a large language model (LLM) pipeline. It features a serial of analysis to extract the ontology from the privacy change documents written in natural language, and then harnesses the few-shot capability of LLMs to construct test cases for the detection of DPC-compliance issues in OS implementations. We apply DopCheck with the latest versions (10 to 13) of Android Open Source Project (AOSP). Our evaluation involving 79 privacy-sensitive APIs demonstrates that DopCheck can effectively recognize DPCs from Android documentation and generate rigorous test cases. Our study reveals that the status quo of the DPC-compliance issues is concerning, evidenced by 19 bugs identified by DopCheck. Notably, 12 of them are discovered in Android 13 and 6 in Android 10 for the first time, posing more than 35% Android users to the risk of privacy leakage. Our findings should raise an alert to Android users and app developers on the DPC compliance issues when using or developing an app, and would also underscore the necessity for Google to comprehensively validate the actual implementation against its privacy documentation prior to the OS release.
cover:          /assets/images/covers/fse'24.jpg
authors:
  - <strong>Chuan Yan</strong>
  - Mark Huasong Meng
  - Fuman Xie
  - Guangdong Bai
links:
  Code: https://github.com/DopCHECK/DopCHECK
  # Unsplash: https://unsplash.com/photos/sliced-in-half-pineapple--_PLJZmHZzk
  Paper: https://dl.acm.org/doi/abs/10.1145/3660826
---
