---
title:          "Investigating Documented Privacy Changes in Android OS"
date:           2024-07-12 00:01:00 +0800
selected:       true
pub:            "<strong><em>FSE'24: Proceedings of the ACM on Software Engineering, Volume 1, Issue FSE</em></strong>"
# pub_pre:        "Submitted to "
# pub_post:       'Under review.'
# pub_last:       ' <span class="badge badge-pill badge-publication badge-success">Spotlight</span>'
pub_date:       "2024"

abstract: >-
  Android has empowered third-party apps to access data and services on mobile devices since its genesis.This involves a wide spectrum of user privacy-sensitive data, such as the device ID and location. In recent years, Android has taken proactive measures to adapt its access control policies for such data, in response to the increasingly strict privacy protection regulations around the world. When each new Android version is released, its privacy changes induced by the version evolution are transparently disclosed, and we refer to them as documented privacy changes (DPCs). Implementing DPCs in Android OS is a non-trivial task, due to not only the dispersed nature of those access control points within the OS, but also the challenges posed by backward compatibility. As a result, whether the actual access control enforcement in the OS implementations aligns with the disclosed DPCs becomes a critical concern. In this work, we conduct the first systematic study on the consistency between the operational behaviors of the OS at runtime and the officially disclosed DPCs. We propose DopCheck, an automatic DPC-driven testing framework equipped with a large language model (LLM) pipeline. It features a serial of analysis to extract the ontology from the privacy change documents written in natural language, and then harnesses the few-shot capability of LLMs to construct test cases for the detection of DPC-compliance issues in OS implementations. We apply DopCheck with the latest versions (10 to 13) of Android Open Source Project (AOSP). Our evaluation involving 79 privacy-sensitive APIs demonstrates that DopCheck can effectively recognize DPCs from Android documentation and generate rigorous test cases. Our study reveals that the status quo of the DPC-compliance issues is concerning, evidenced by 19 bugs identified by DopCheck. Notably, 12 of them are discovered in Android 13 and 6 in Android 10 for the first time, posing more than 35% Android users to the risk of privacy leakage. Our findings should raise an alert to Android users and app developers on the DPC compliance issues when using or developing an app, and would also underscore the necessity for Google to comprehensively validate the actual implementation against its privacy documentation prior to the OS release.
cover:          /assets/images/covers/fse'24.jpg
authors:
  - <strong>Chuan Yan</strong>
  - Mark Huasong Meng
  - Fuman Xie
  - Guangdong Bai
links:
  # Code: https://github.com/luost26/academic-homepage
  # Unsplash: https://unsplash.com/photos/sliced-in-half-pineapple--_PLJZmHZzk
  Paper: https://dl.acm.org/doi/abs/10.1145/3660826
---
