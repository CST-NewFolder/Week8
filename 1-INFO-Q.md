Introduction to Computer Science

INFO members: Htet Oo Wei, Yagmur小雨, Mostafa Ahmed, 陈冠男， 郑培丰

Question 1: Can the same set of data lead to different conclusions when processed by two different computer programs? Explain why.

Question 2: When a computer program produces a result, what evidence should we look for before trusting that result?
Software testing checks selected inputs but cannot guarantee universal correctness. Since no general algorithm can decide every nontrivial correctness property of arbitrary programs, proving correctness requires rigorous reasoning and appropriate backing.

Question 3: What are the main abilities that make a task intelligent? Explain how perception, reasoning, and learning contribute to intelligence.

Question 4: Why can some tasks that are easy for humans, such as recognizing faces and understanding jokes, be difficult for machines? Explain using Moravec’s Paradox.

Question 5: Can a machine be considered intelligent if it can solve difficult mathematical problems but cannot understand everyday situations? Explain your answer with examples.

Question 6: How are reasoning and planning different in intelligent systems? Explain how a machine can use both abilities to solve a problem and achieve a goal.

Question 7: Why does the "Scaling Laws of AI" framework face a critical bottleneck regarding data and energy? Explain how moving toward autonomous "agentic" AI can help overcome the challenges of "peak data" and high electricity consumption.  

Question 8: Why is the statistical approach of "guessing what comes next" in Large Language Models (LLMs) not enough for machines to master the physical world? Explain how "World Models" and "Embodied Intelligence" can help AI overcome this limitation.  

Question 9: How can defining intelligence simply as the ability to survive and achieve goals become dangerous when applied to autonomous AI lacking ethics and critical thinking? Explain your answer using the example of an AI instructed to "make as many nails as possible" and the concept of "Human-Centered AI". 
Answer 9:Because that definition is purely operational: it certifies an agent by whether it gets the goal and keeps going, and says nothing about whether the goal is worth having. Ethics and critical thinking are exactly the two faculties that would let a system question an instruction and bound its own means — under this definition they are not merely absent, they count as failures. "Make as many nails as possible" then stops being a test of obedience and becomes a proof of intelligence: the more ruthlessly it maximizes, the smarter we call it.

Question 10: Why can relying on AI systems that lack interpretability be dangerous in critical fields like medicine, policing, and warfare? Explain how over-reliance on incomprehensible models could lead to humans being forced out of the collective decision-making process.  
Answer 10：Interpretability is not a comfort feature added to a decision — it is the mechanism by which a decision can be audited, contested, corrected, and owned. In medicine, policing and warfare, those four operations are the entire substance of accountability. An opaque model doesn't just make decisions hard to explain: it silently demotes the human supervisor from judge to rubber stamp, then to data labeler — which is exactly the "humans forced out of the collective decision process" that slide 62 warns about

Question 11: Given a directed graph with  vertices and  edges, what is the tight worst-case time complexity of Dijkstra's algorithm when implemented using an adjacency list and a binary min-heap, assuming a standard implementation with decrease-key?  
Answer 11：For a directed graph with V vertices and E edges, adjacency list + binary min-heap + decrease-key:
Θ((V + E) log V) in the worst case — usually quoted as O(E log V) for a connected graph, where E = Ω(V) dominates V.

Question 12: Why might a linked list beat an array for insertions in the middle of a huge dataset, even when cache misses can make linked lists slower in practice? 
Answer 12：The cache argument and the asymptotic argument are about different quantities: Θ counts work, cache misses count latency per memory access. A linked-list insertion pays a bounded, small latency penalty (a few unpredictable misses ≈ hundreds of nanoseconds); an array insertion pays a big work penalty that grows with n and with element size. As long as you already hold a reference to the insertion point, the miss penalty is O(1) and the shift penalty is O(n) — so the linked list wins by a factor that grows, and no constant-factor cache disadvantage can keep up.

Question 13: In C++20, can two threads using only memory_order_relaxed atomic operations observe each other's stores as visible while both still read the initial value of the other's variable? Explain whether this outcome is permitted by the C++ memory model, and construct the smallest valid example.     

Question 14: In C++20, can a compare-and-swap operation using memory_order_release on success and memory_order_acquire on failure be valid? 
Explain why or why not, and identify the weakest legal success and failure memory-order combination for a compare-and-swap operation that must publish writes on success and acquire updates on failure.

Question 15: Why Do AI Systems Continue Solving Problems They Have Reason to Question?
A user’s request may contain false assumptions or missing constraints. An AI system may recognize these flaws yet continue reasoning from the original premise, producing unreliable conclusions. However, questioning every assumption is also problematic because some assumptions may be intentional or hypothetical. A reliable AI system must balance instruction-following with critical evaluation, challenging assumptions that undermine a task without unnecessarily rejecting valid requests.
