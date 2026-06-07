# You Can't Look a Gift Model in the Mouth! 🎁 🤖

This repository contains the complete presentation slides of my academic seminar.

It explores the **Trust Dilemma in Machine Learning as a Service (MLaaS)**, analyzing how a malicious third-party provider can plant a completely undetectable backdoors in ML models.

This seminar aims to translate the complex cryptographic and AI security research into an accessible, educational format using whimsical illustrations to better understand the complexity of the ideas presented in the artcial.

---

## 🧭 Core Theoretical Concepts Covered

### 1. Black-Box vs. White-Box Vulnerabilities
* **Black-Box Access Model:** The backdoor is constructed via digital signature verification loops operating in parallel to the honest pipeline.
* **White-Box Access Model:** Backdoors are embedded directly into the initial distribution layer using Random Fourier Features (RFF), making them completely invisible even under microscopic code and weight inspections.

### 2. Cryptographic Hardness Assumptions
The mathematical guarantees of this backdoor's undetectability are tied directly to the worst-case hardness of high-dimensional lattice problems assumed to be quantum-resistant (BQP-hard):
* **SIVP (Shortest Independent Vectors Problem):** The challenge of finding the minimal basis (shortest steps) to span a lattice across all dimensions.
* **GapSVP (Gap Shortest Vector Problem):** The decision problem of distinguishing whether a lattice's shortest vector is tightly packed (microscopic) or widely spaced (massive).

### 3. Continuous Learning With Errors (CLWE)
The backdoor leverages the structural indistinguishability between standard **Isotropic Gaussian Noise** and a malicious **Gaussian Pancakes** distribution.
Distinguishing the two is proven to be as computationally hard as solving GapSVP or SIVP, guaranteeing absolute white-box undetectability.

---

## 🛡️ Mitigations & The Security Trade-off
The seminar evaluates **Randomized Smoothing (Evaluation-Time Immunization)** as a defense mechanism. By introducing a noise cloud (Smoothing Radius $\sigma$), triggers can be washed out.

However, this introduces a critical security trade-off: setting $\sigma$ too high to combat an adaptive attacker fundamentally degrades model utility, rendering the classifier useless.

---

## 🧠 Personal Remarks: The Necessity of Critical Thinking
While this research explicitly highlights the dangers of outsourced machine learning models, my takeaway is about a lesson in **delegated learning**. 

We outsource our learning constantly - when we scroll through social media, read and watch the news, and even when we query various LLMs.
The information presented to us often appears unbiased, but structural biases or hidden agendas can easily remain completely undetectable to a *passive* consumer.

The ultimate defense is very simple - **active critical thinking**:
* **Cross-reference:** Validate insights across multiple sources.
* **Actively Inspect Assumptions:** Question and challenge the foundational data and rules. 
* **Try to Stay Curious:** Open your mind to new possibilites, cat-like curiosity may just help you do exactly that.

Technologies and external frameworks should be leveraged to support our thinking but ***never to replace it***.

---

## 📂 Repository Contents
`Presentation - You Cant Look a Gift Model in the Mouth!.pdf`

Full slide deck with visual proofs, conceptual analogies, and technical architectures.

## 🎓 Acknowledgments
This seminar is based on the research paper [*"Planting Undetectable Backdoors in Machine Learning Models"*](https://arxiv.org/abs/2204.06974) by Shafi Goldwasser, Michael P. Kim, Vinod Vaikuntanathan, and Or Zamir.
