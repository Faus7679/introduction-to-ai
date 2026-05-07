# Introduction to AI: Comprehensive Exploration of Current Capabilities

## Overview

This document provides a comprehensive exploration of the current state of Artificial Intelligence (AI) capabilities, drawing from recent studies, landmark advancements, and critical assessments within the field. It then evaluates whether computers currently possess the capability to solve eleven specific real-world tasks, justified with supporting evidence from the literature.

---

## Part 1: The Current Landscape of AI

### 1.1 Foundational Advances: Deep Learning and Large Language Models

The past decade has witnessed a dramatic acceleration in AI progress, largely driven by deep learning—a subfield of machine learning using multi-layered neural networks. The introduction of the Transformer architecture (Vaswani et al., 2017, "Attention Is All You Need") catalyzed an explosion of Large Language Models (LLMs). Models such as OpenAI's GPT-4 (2023), Google's Gemini (2024), and Anthropic's Claude (2024) demonstrate remarkable capabilities in natural language understanding, reasoning, code generation, and creative writing. These systems are trained on vast corpora of text and exhibit emergent behaviors—capabilities that were not explicitly trained but arise from scale (Wei et al., 2022, "Emergent Abilities of Large Language Models," *TMLR*).

### 1.2 Computer Vision and Perception

Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs) have achieved superhuman performance on several image recognition benchmarks. Systems like OpenAI's CLIP and Google's Florence demonstrate cross-modal understanding linking vision and language. Object detection, scene segmentation, and pose estimation have matured considerably, enabling applications in autonomous vehicles, medical imaging, and surveillance.

### 1.3 Robotics and Embodied AI

Robotics has historically lagged behind software AI. Physical robots face challenges in dexterity, perception in unstructured environments, and real-time adaptation. However, recent work—such as Google DeepMind's RT-2 (Brohan et al., 2023), which connects vision-language models to robot control—shows that robots can follow natural language instructions to manipulate objects. Boston Dynamics' Atlas robot demonstrates impressive mobility on uneven terrain. Nevertheless, general-purpose physical task completion remains an open problem.

### 1.4 Autonomous Vehicles

Waymo, Tesla, Cruise (General Motors), and other companies have deployed semi- and fully autonomous vehicles on public roads. Waymo's Robotaxi service operates in San Francisco, Phoenix, and Los Angeles without human safety drivers in defined geofenced zones. SAE Level 4 autonomy—where the system handles all driving functions within specific operational design domains (ODDs)—has been demonstrated at scale in limited deployments (SAE International, J3016, 2021). Full Level 5 autonomy (any condition, any location) remains unsolved.

### 1.5 Game-Playing AI

Game-playing AI represents some of the clearest benchmarks of progress. DeepMind's AlphaGo (2016) defeated the world Go champion, and AlphaZero (2017) mastered chess, shogi, and Go from scratch using self-play. OpenAI Five defeated professional Dota 2 teams in 2019. These achievements established that AI can far exceed human performance in well-defined, digital game environments.

### 1.6 Scientific Discovery and Mathematical Reasoning

AI is increasingly used in scientific research. AlphaFold 2 (Jumper et al., 2021, *Nature*) solved the decades-old protein folding problem, predicting protein structure with near-experimental accuracy. In mathematics, DeepMind's AlphaGeometry (2024, *Nature*) solved Olympiad-level geometry problems at near-gold-medalist performance. AlphaProof (2024) combined LLMs with formal proof search to solve problems from the International Mathematical Olympiad (IMO). These developments signal that AI is moving toward genuine scientific and mathematical contribution.

### 1.7 Healthcare and Medical AI

AI diagnostics have achieved expert-level performance in specialized domains. The FDA has approved over 500 AI/ML-based medical devices as of 2023. Google's DermAssist detects skin conditions; IDx-DR autonomously diagnoses diabetic retinopathy without a physician's review. In drug discovery, Insilico Medicine's AI-designed molecule for IPF reached Phase II clinical trials (2023). However, broad clinical deployment is hindered by regulatory frameworks, liability concerns, and the need for human oversight.

### 1.8 Natural Language Processing: Speech and Translation

Neural machine translation (NMT), pioneered at scale by Google (Wu et al., 2016), achieves near-human quality for high-resource language pairs. Real-time speech-to-speech translation is offered by Google Translate, Microsoft Azure Cognitive Services, and Meta's SeamlessStreaming (2023), which performs simultaneous translation across dozens of language pairs with low latency. These systems combine Automatic Speech Recognition (ASR), NMT, and Text-to-Speech (TTS) in an end-to-end pipeline.

### 1.9 Critiques and Limitations

Despite impressive achievements, the field faces important critiques:

- **Brittleness and Lack of Generalization:** LLMs and neural networks can fail on simple distribution shifts or adversarial inputs (Marcus & Davis, 2019, *Rebooting AI*).
- **Hallucination:** LLMs confidently generate factually incorrect information, limiting their reliability in high-stakes domains.
- **Data Bias and Fairness:** Training data reflects historical biases, leading to discriminatory outcomes (Buolamwini & Gebru, 2018, "Gender Shades").
- **Interpretability:** Deep neural networks are largely black boxes; understanding why a model produces a given output remains an active research challenge (Rudin, 2019, *Nature Machine Intelligence*).
- **Physical World Gap:** The "embodiment gap" between digital AI success and physical robotic manipulation remains substantial (LeCun, 2022, "A Path Towards Autonomous Machine Intelligence").
- **Energy and Resource Costs:** Training frontier models requires enormous computational resources with significant environmental impact (Strubell et al., 2019, "Energy and Policy Considerations for Deep Learning in NLP").

---

## Part 2: Task-by-Task Evaluation

### Task 1 — Playing a Decent Game of Beach Volleyball

**Verdict: ❌ Not currently capable**

Beach volleyball requires real-time physical locomotion, precise hand-eye coordination, rapid adaptation to wind and sand conditions, and dynamic team cooperation—all in an unpredictable outdoor environment. While robotic arms have achieved ball-juggling and table tennis in constrained lab settings (e.g., Festo's BionicCobot, DEXTERITY's robot ping-pong), no robotic system has demonstrated the full-body agility, jumping ability, and adaptive motor control needed to play beach volleyball even at a recreational level. The combination of bipedal locomotion on unstable sand, tracking a fast-moving ball under sunlight, and hitting with sufficient power and accuracy remains far beyond current robotics capabilities. Reinforcement learning policies for locomotion and manipulation have improved markedly (e.g., Boston Dynamics, DeepMind's RoboCat), but physical team sports in outdoor environments represent an unsolved grand challenge in embodied AI.

**Evidence:** Kober et al. (2013, *IJRR*, "Reinforcement Learning in Robotics: A Survey") document that even structured sport tasks like ball catching remain challenging. As of 2025, no published system has played beach volleyball autonomously.

---

### Task 2 — Driving Looking for a Game Store in the Center of Phoenix

**Verdict: ✅ Currently capable (within specific operational zones)**

Waymo operates a fully driverless Robotaxi service in Phoenix, Arizona, as one of its primary deployment cities. Waymo One became available to the general public in Phoenix in 2020 and expanded to driverless (no safety driver) operations in 2022. The system navigates urban streets, interprets traffic signals, avoids obstacles, and reaches user-specified destinations. Integrating mapping services (e.g., Google Maps) to navigate to a specific store is already part of the user experience—passengers request a destination and the vehicle drives there autonomously. While the phrase "looking for" implies some search behavior, this is readily handled by map/POI data integration that is standard in these platforms.

**Caveat:** Coverage is limited to Waymo's geofenced operational design domain in Phoenix. Areas outside that domain would not be covered.

**Evidence:** Waymo (2022) press release on fully driverless Phoenix service; Bansal & Kockelman (2017, *Transportation Research*) on autonomous vehicle deployment in Phoenix metro; SAE J3016 Level 4 classification.

---

### Task 3 — Driving in Hollywood, California

**Verdict: ✅ Currently capable (within operational zones)**

Waymo expanded its Waymo One service to Los Angeles, including the Hollywood neighborhood, in 2024. The service operates in a broad swath of Los Angeles, covering areas such as Hollywood, WeHo, and Santa Monica. Hollywood presents complex urban driving conditions—pedestrian-dense streets, construction zones, tourists, and high-traffic intersections—which Waymo's system navigates using LiDAR, radar, and camera sensor fusion combined with high-definition maps. Tesla's Full Self-Driving (FSD) software also operates in the Los Angeles area, though it requires driver supervision (SAE Level 2+) and cannot be considered fully autonomous.

**Evidence:** Waymo (2024) announcement of Los Angeles service expansion; NHTSA AV testing data; Waymo Safety Report (2023).

---

### Task 4 — Buying a Weekend's Worth of Groceries at the Market

**Verdict: ❌ Not currently capable (for a physical in-store robot)**

Autonomously navigating a physical grocery store, selecting appropriate items from shelves, placing them in a cart, proceeding to checkout, and completing payment remains beyond current general-purpose robotic capabilities. The challenge involves: unstructured environment navigation, recognizing thousands of product SKUs, grasping items of varying sizes and fragilities, adapting to stock changes, and social navigation among other shoppers. While Amazon's cashierless "Just Walk Out" stores automate checkout tracking for humans, and Boston Dynamics' Spot has been used for inventory scanning, no system can perform the full shopping task autonomously. 

**Note:** If interpreted as an AI system controlling a human's phone to order groceries online via delivery, this would be feasible (see Task 5), but the task specifically references going "at the market."

**Evidence:** Correll et al. (2016, *Science Robotics*, "Analysis and Observations from the First Amazon Picking Challenge") document the difficulty of warehouse picking tasks. As of 2025, no commercially deployed robotic grocery shopper exists.

---

### Task 5 — Buying a Day's Worth of Groceries on a Cell Phone

**Verdict: ✅ Currently capable**

This task—ordering groceries via a smartphone application—is fully solved and widely deployed. Services such as Instacart, Amazon Fresh, Walmart Grocery, Kroger, and many others allow users (or AI agents acting on their behalf) to browse products, add items to a cart, and complete checkout with delivery or pickup. Furthermore, AI agents capable of using smartphone interfaces autonomously are emerging: systems like Google's Project Astra, Apple Intelligence, and OpenAI Operator-style agents can navigate mobile UIs to complete tasks. The task requires no physical presence and is purely a software/interface challenge, which is well within current AI capabilities.

**Evidence:** Instacart and Amazon Fresh market data; Yao et al. (2022, "WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents") demonstrate AI agents completing e-commerce tasks at high success rates.

---

### Task 6 — Playing Chess at a Competitive Level

**Verdict: ✅ Definitively capable (far exceeds human ability)**

This is one of the clearest-cut cases of AI surpassing human capability. IBM's Deep Blue defeated world champion Garry Kasparov in 1997. Since then, chess engines have advanced dramatically. Stockfish 17 (2024) has an estimated Elo rating exceeding 3600—roughly 600+ points above Magnus Carlsen, the highest-rated human player ever (~2850). DeepMind's AlphaZero (Silver et al., 2018, *Science*) defeated Stockfish 8 in a 100-game match and demonstrated novel, creative chess strategies that influenced human grandmaster play. Modern AI systems can play millions of games per day, analyze positions to unprecedented depth, and identify winning moves in milliseconds. No human player can compete with a modern engine on equal terms.

**Evidence:** Silver et al. (2018, *Science*) "A general reinforcement learning algorithm that masters chess, shogi and Go through self-play"; CCRL Rating List (2024).

---

### Task 7 — Discovering and Proving New Math Theorems

**Verdict: 🟡 Emerging capability — limited but growing**

AI has made genuine progress in mathematical theorem proving, but fully autonomous discovery of significant new theorems remains an open frontier. Key milestones include:

- **AlphaGeometry** (Trinh et al., 2024, *Nature*): Solved 25 of 30 IMO geometry problems at a level near IMO gold medalists.
- **AlphaProof** (DeepMind, 2024): Combined an LLM with a formal proof search system (Lean 4) to solve 4 of 6 problems from the 2024 IMO, including a silver-medal performance.
- **FunSearch** (Romera-Paredes et al., 2023, *Nature*): Discovered new mathematical constructs in combinatorics (cap set problem).
- **Lean Copilot / Proof assistants**: LLMs can suggest proof steps in formal verification systems, accelerating mathematician workflows.

However, AI systems still rely heavily on human-defined problem formulations, struggle with open-ended conjecture generation, and have not independently discovered major new theorems in core areas of mathematics. The capability exists at the level of olympiad problems and structured settings, not at the frontier of unsolved research mathematics.

**Evidence:** Trinh et al. (2024, *Nature*); Romera-Paredes et al. (2023, *Nature*); Davies et al. (2021, *Nature*, "Advancing mathematics by guiding human intuition with AI").

---

### Task 8 — Writing a Comedy Movie

**Verdict: 🟡 Partial capability — assistive but not independently competitive**

Large language models like GPT-4 and Claude 3 Opus can generate coherent, humorous screenplay drafts with proper formatting, compelling characters, and witty dialogue. AI tools are already used as assistants by professional screenwriters for brainstorming, dialogue polish, and structural analysis. In 2023, the WGA strike highlighted concerns about AI being used to replace screenwriters, attesting to industry recognition of AI's growing creative capability.

However, truly outstanding, original comedy requires deep cultural understanding, subversive timing, novelty, and emotional resonance that current AI systems struggle to achieve consistently. AI-generated scripts tend to be formulaic, rely on familiar tropes, and lack the unique voice of a skilled human writer. There are no commercially released AI-written comedy films that have achieved critical or commercial success equivalent to human-written works.

**Verdict interpretation:** AI can write a functional first draft of a comedy screenplay, but cannot yet independently produce a work competitive with top human comedy writers.

**Evidence:** Mirowski et al. (2023, *arXiv*, "Co-Writing Screenplays and Theatre Scripts with a Language Model"); Elkins & Chun (2020, "Can GPT-3 Pass a Writer's Turing Test?").

---

### Task 9 — Giving Competent Prescriptions Given a Symptom

**Verdict: 🟡 Technically capable but not legally authorized — with important caveats**

AI systems have demonstrated performance matching or exceeding average physicians in specific diagnostic tasks:

- **GPT-4** scored in the top 10th percentile on the USMLE Step exams (Nori et al., 2023, Microsoft Research).
- **Med-PaLM 2** (Singhal et al., 2023, *Nature*) achieved expert-level performance on medical exam questions and clinical scenarios.
- **IDx-DR** (now Digital Diagnostics): FDA-cleared autonomous diagnostic AI for diabetic retinopathy.
- **Various clinical decision support systems** (e.g., IBM Watson for Oncology, Viz.ai for stroke) provide treatment recommendations used by physicians.

These systems can map symptoms to likely diagnoses and suggest treatments that align with clinical guidelines. However: (1) they are not legally authorized to prescribe medications without physician oversight in any jurisdiction; (2) they can make dangerous errors in edge cases; (3) they lack the physical examination capability and full patient context that informs real prescribing decisions. In practice, these systems function as decision-support tools that enhance (but do not replace) physician judgment.

**Evidence:** Nori et al. (2023, "Capabilities of GPT-4 on Medical Challenge Problems," Microsoft Research); Singhal et al. (2023, *Nature*, "Large language models encode clinical knowledge").

---

### Task 10 — Translating Spoken English into Spoken Portuguese in Real-Time

**Verdict: ✅ Currently capable**

Real-time speech-to-speech translation between English and Portuguese is a fully deployed, commercially available capability. Multiple systems achieve this:

- **Google Translate** and **Google Interpreter Mode**: Real-time spoken translation available on Android/iOS and Google Home devices.
- **Microsoft Azure Speech Translation**: Low-latency streaming translation supporting English-Portuguese with natural TTS output.
- **Meta SeamlessStreaming** (Barrault et al., 2023): A research system performing simultaneous speech-to-speech translation across 100+ languages with latency under 2 seconds.
- **KUDO**, **Interprefy**, and other platforms offer AI-assisted interpretation for conferences.

English and Portuguese are both high-resource languages with abundant parallel training data, making this translation pair particularly well-served. Translation quality for everyday conversation is generally high, though specialized technical, idiomatic, or dialectal content may pose challenges.

**Evidence:** Barrault et al. (2023, *arXiv*, "SeamlessM4T: Massively Multilingual & Multimodal Machine Translation"); Wu et al. (2016, "Google's Neural Machine Translation System").

---

### Task 11 — Performing a Complex Surgical Knee Operation

**Verdict: ❌ Not currently capable autonomously**

Robotic surgical systems are well-established in operating rooms worldwide. The **da Vinci Surgical System** (Intuitive Surgical) is used in over 1.2 million procedures annually for minimally invasive surgery. **MAKO SmartRobotics** (Stryker) is specifically designed for knee replacement surgery, guiding the surgeon's handpiece within a pre-planned boundary to improve implant placement accuracy (Kayani et al., 2018, *Bone & Joint Journal*). These systems demonstrably improve outcomes in knee arthroplasty compared to manual techniques.

However, these are **surgeon-controlled robotic systems**, not autonomous AI surgeons. The surgeon plans the procedure, makes all critical decisions, and controls the robot; the system enforces boundaries and provides haptic feedback. Fully autonomous robotic surgery—where an AI independently performs an entire procedure without human control—has been demonstrated only in extremely constrained experimental settings (e.g., STAR robot for intestinal anastomosis in pigs; Saeidi et al., 2022, *Science Robotics*), and never for complex human knee surgery in clinical practice.

Key barriers include: intraoperative adaptation to unexpected anatomy, sterile field maintenance, managing bleeding and complications, anesthesia coordination, and enormous liability/regulatory hurdles.

**Evidence:** Kayani et al. (2018, *Bone & Joint Journal*) "Robotic total knee arthroplasty"; Saeidi et al. (2022, *Science Robotics*) "Autonomous robotic laparoscopic surgery"; FDA regulations on autonomous surgical devices.

---

## Summary Table

| Task | Capable? | Confidence |
|------|----------|------------|
| 1. Playing beach volleyball | ❌ No | High |
| 2. Driving to a game store in Phoenix | ✅ Yes | High (within Waymo ODD) |
| 3. Driving in Hollywood, CA | ✅ Yes | High (within Waymo ODD) |
| 4. Buying groceries at a physical market | ❌ No | High |
| 5. Buying groceries on a cell phone | ✅ Yes | High |
| 6. Playing chess competitively | ✅ Yes | Very High |
| 7. Discovering and proving new math theorems | 🟡 Emerging | Medium |
| 8. Writing a comedy movie | 🟡 Partial | Medium |
| 9. Giving competent prescriptions | 🟡 Partial | Medium |
| 10. Translating English to Portuguese in real-time | ✅ Yes | Very High |
| 11. Performing complex knee surgery | ❌ No (autonomously) | High |

---

## References

- Barrault, L., et al. (2023). *SeamlessM4T: Massively Multilingual & Multimodal Machine Translation*. arXiv:2308.11596.
- Brohan, A., et al. (2023). *RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control*. arXiv:2307.15818.
- Buolamwini, J., & Gebru, T. (2018). *Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification*. FAccT 2018.
- Correll, N., et al. (2016). *Analysis and Observations from the First Amazon Picking Challenge*. *IEEE TASE*.
- Davies, A., et al. (2021). Advancing mathematics by guiding human intuition with AI. *Nature*, 600, 70–74.
- Jumper, J., et al. (2021). Highly accurate protein structure prediction with AlphaFold. *Nature*, 596, 583–589.
- Kayani, B., et al. (2018). Robotic total knee arthroplasty. *Bone & Joint Journal*, 100-B(12), 1566–1575.
- Kober, J., Bagnell, J. A., & Peters, J. (2013). Reinforcement learning in robotics: A survey. *IJRR*, 32(11), 1238–1274.
- LeCun, Y. (2022). *A Path Towards Autonomous Machine Intelligence*. OpenReview.
- Marcus, G., & Davis, E. (2019). *Rebooting AI*. Pantheon Books.
- Mirowski, P., et al. (2023). *Co-Writing Screenplays and Theatre Scripts with a Language Model*. arXiv:2209.14958.
- Nori, H., et al. (2023). *Capabilities of GPT-4 on Medical Challenge Problems*. Microsoft Research arXiv:2303.13375.
- Romera-Paredes, B., et al. (2023). Mathematical discoveries from program search with large language models. *Nature*, 625, 468–475.
- Rudin, C. (2019). Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead. *Nature Machine Intelligence*, 1, 206–215.
- SAE International. (2021). *Taxonomy and Definitions for Terms Related to Driving Automation Systems* (J3016).
- Saeidi, H., et al. (2022). Autonomous robotic laparoscopic surgery for intestinal anastomosis. *Science Robotics*, 7(62).
- Silver, D., et al. (2018). A general reinforcement learning algorithm that masters chess, shogi and Go through self-play. *Science*, 362(6419), 1140–1144.
- Singhal, K., et al. (2023). Large language models encode clinical knowledge. *Nature*, 620, 172–180.
- Strubell, E., Ganesh, A., & McCallum, A. (2019). Energy and Policy Considerations for Deep Learning in NLP. *ACL 2019*.
- Trinh, T. H., et al. (2024). Solving olympiad geometry without human demonstrations. *Nature*, 625, 476–482.
- Vaswani, A., et al. (2017). Attention is all you need. *NeurIPS 2017*.
- Waymo. (2022). *Waymo One Expands Fully Autonomous Rides in Phoenix*. Waymo Blog.
- Waymo. (2024). *Waymo One Launches in Los Angeles*. Waymo Blog.
- Wei, J., et al. (2022). Emergent abilities of large language models. *TMLR*.
- Wu, Y., et al. (2016). *Google's Neural Machine Translation System: Bridging the Gap between Human and Machine Translation*. arXiv:1609.08144.
- Yao, S., et al. (2022). *WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents*. NeurIPS 2022.
