---
marp: true
footer: '[@skeptrune](htttps://x.com/skeptrune) - nick.k@trieve.ai'
transition: fade
theme: gaia
---

<!-- _footer: '[github.com/skeptrunedev/relearning-reranking](https://github.com/skeptrunedev/relearning-reranking)' -->

![bg right:50% width:98%](https://trieve.b-cdn.net/relearning-ranking/presentation-qr.png)

# Relearning Ranking

### Bringing Back the Old School

---

![bg right:40%](https://avatars.githubusercontent.com/u/15804464?v=4)

## Nicholas Khami
### Founder/CEO </br>[trieve](https://trieve.ai)

- we serve over 1M re-ranking queries every week

<i class="fa-brands fa-twitter"></i> Twitter: @skeptrune
<i class="fa-brands fa-linkedin"></i> LinkedIn: - [nicholas-khami](https://www.linkedin.com/in/nicholas-khami-5a0a7a135/)
<i class="fa-brands fa-github"></i> GitHub: [github.com/skeptrunedev](https://github.com/skeptrunedev)

---
![bg left](https://trieve.b-cdn.net/relearning-ranking/todo-list-clipboard.webp)

### Agenda | Old to New

- What is Learning to Rank?
- Types of LTR
- Well known implementations
\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-
- Cross Encoders
- Cross Encoders vs. LTR
- Vector DB's are kind of cooked
  
---

<div class="section-content">

# Old School Learning to Rank

</div>

<style>
.section-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    width: 100%;
}
</style>

---

![bg right:50% width:100%](https://trieve.b-cdn.net/relearning-ranking/learning-to-rank-nutshell.webp)

# What is LTR?

- multiple scores exist per retrieved doc (upvotes, bm25, cos_dist, backlinks)
- LTR describes using ML model to sort based on weighted combination of scores

--- 

# How to train?
###### Supervised learning wth labeled ground truth data


![bg left:40% height:100%](https://trieve.b-cdn.net/relearning-ranking/model-setup-code_block.webp)

1) **Good:** pointwise regression
2) **Better:** pairwise classification
3) **Best:** holistic listwise ordering

--- 

# Well known LTR systems

![bg right:50%](https://trieve.b-cdn.net/relearning-ranking/vintage-flash-bulb-red-carpet.webp)

- Google combines backlinks, fulltext, and other signals
- Facebook combines similarity, closeness to network
- Reddit combines upvotes and relevance in search
--- 

<div class="section-content">

# New School Neural Re-ranker Models

</div>

<style>
.section-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    width: 100%;
}
</style>

---

# What is a "re-ranker"

![bg left:39% width:95%](https://trieve.b-cdn.net/relearning-ranking/cross-encoder-diagram.webp)

- Technically **cross-encoder(s)**
- Transformer network that scores query<->doc pair
- Closest to a **pointwise-regression** in LTR context

--- 

<!-- _footer: '[docs.trieve.ai/vector-inference](https://docs.trieve.ai/vector-inference/introduction)' -->

# Why use cross-encoders?

![bg right:50% width:95%](https://trieve.b-cdn.net/relearning-ranking/modern-man-decision.webp)

- Usually worse than LTR
- Main reason to use is due to lack of labeled data
- PSA: latency-optimize with Trieve Vector Inference

---

# Vector DB's are kind of cooked

![bg left:30% width:95%](https://trieve.b-cdn.net/relearning-ranking/pinecone-getting-cooked.webp)

&nbsp;&nbsp;&nbsp;OpenSearch/Solr have LTR
\+ Vector DB's don't have LTR
\+ OpenSearch/Solr have Vectors and more
\-\-\-\-
\= Vector DB's are cooked

---

<div class="section-content">

# Questions

Thank you!

</div>

<style>
.section-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    width: 100%;
}
</style>