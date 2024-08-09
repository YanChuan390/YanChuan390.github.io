---
title:          "Analyzing Excessive Permission Requests in Google Workspace Add-ons"
date:           2024-03-16 00:01:00 +0800
selected:       false
pub:            "<strong><em>ICECCS '24: 28th International Conference on Engineering of Complex Computer Systems</em></strong>"
# pub_pre:        "Submitted to "
# pub_post:       'Under review.'
# pub_last:       ' <span class="badge badge-pill badge-publication badge-success">Spotlight</span>'
pub_date:       "2024"

abstract: >-
  In the digital era, business collaboration platforms have become pivotal in facilitating seamless remote work and virtual team interactions. These platforms, typified by Google Workspace, offer an integrated suite of tools~(such as Google Docs, Slides, and Calendar) that significantly enhance business operations. They often extend their functionality through the integration of third-party applications, known as “add-ons”. Google Workspace exemplifies this trend, blending traditional business solutions with advanced, add-on-driven capabilities. While this greatly augments productivity and collaboration for online personal or team work, concerns about the excessive use of data and permissions have been raised by both users and legislators, as add-ons can utilize the granted permissions to
  access and manipulate files managed by business collaboration platforms. In this work, we propose an end-to-end approach to automatically detecting excessive permissions among add-ons. It advocates purpose limitation that the requested permissions of the add-on should be for its specific functionality and in compliance with the actual needs in fulfilling the functionality. Our approach utilizes a hybrid analysis to detect excessive permissions, including analysis of the add-on’s runtime behavior and source code, and state-of-the-art language processing techniques for textual artifact interpretation. This approach can serve the users, developers and store operators as an efficient and practical detection mechanism for excessive permissions. We conduct a large-scale diagnostic evaluation on 3,756 add-ons, revealing that almost half of existing add-ons contain issues of excessive permissions. We further investigate the root cause of excessive permissions and provide insights to stakeholders. Our work should raise the awareness of add-on users, service providers, and platform operators, and encourage them to implement solutions that restrict the excessive permissions in practice.
cover:          /assets/images/covers/iceccs'24.jpg
authors:
  - Liuhuo Wan
  - <strong>Chuan Yan</strong>
  - Mark Huasong Meng
  - Kailong Wang
  - Haoyu Wang
links:
  # Code: https://github.com/luost26/academic-homepage
  # Unsplash: https://unsplash.com/photos/sliced-in-half-pineapple--_PLJZmHZzk
  # Paper: https://dl.acm.org/doi/pdf/10.1145/3597503.3639107
---
