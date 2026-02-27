# Best-Parts Map

| Layer | Best LLM for This Layer | What to Extract (copy the key paragraph/section) |
|-------|------------------------|--------------------------------------------------|
| Layer 1: Data Foundation        |  gemmini        |     The system ingests three distinct data streams: static restaurant metadata (menu, price, location), dynamic event logs (clicks, views, order history), and real-time signals (GPS coordinates, current weather, and local traffic).        |
| Layer 2: Statistics & Analysis  |   claude       |     ranking model: Bayesian-smoothed ratings (to stop a restaurant with 3 reviews from outranking one with 3,000        |
| Layer 3: ML Models              |   gemini       |        The core engine uses a Two-Tower neural network architecture or Gradient Boosted Decision Trees (GBDT) to rank thousands of candidates. The "Query Tower" encodes user state (past orders, time of day), while the "Candidate Tower" encodes restaurant state, producing a similarity score in a shared vector space.     |
| Layer 4: LLM / Generative AI   |    chatgpt      |     Controlling hallucinations and ensuring factual accuracy (menus, pricing). Maintaining latency constraints.        |
| Layer 5: Deployment & Infra     |    chatgpt      |     Maintaining low latency during peak traffic (meal times). Ensuring model rollback safety and versioning.        |
| Layer 6: System Design & Scale  |    chatgpt      |        Balancing freshness vs scalability. Designing multi-stage ranking to reduce computational cost.     |
| Overall Analysis / Hardest Problem |   gemini    |      f you were rebuilding this from scratch, the first thing you'd need to get right is..." > The Feature Store.       |
| Writing Style / Structure       |   chatgpt       |       If rebuilding from scratch: The first thing you'd need to get right is: High-quality event tracking and feature pipeline design. If your behavioral data is flawed, every downstream ML layer becomes unreliable.      |
