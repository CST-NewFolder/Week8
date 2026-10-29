Introduction to Computer Science

INFO members: Htet Oo Wei, Yagmur小雨, Mostafa Ahmed, 陈冠男， 郑培丰
***
Question 1: Can the same set of data lead to different conclusions when processed by two different computer programs? Explain why.

**Answer1:** Yes. The PPT's formula AI = Algorithm + Data + Computility shows data is only one ingredient. Different algorithms (CNN vs. Transformer) process the same data differently, and NLP is essentially "guess what comes next," so different models guess differently. Scaling laws also mean different parameter counts and computility lead to different results. Add different preprocessing and training settings, and the same dataset can easily support different conclusions.
***
Question 2: When a computer program produces a result, what evidence should we look for before trusting that result?
Software testing checks selected inputs but cannot guarantee universal correctness. Since no general algorithm can decide every nontrivial correctness property of arbitrary programs, proving correctness requires rigorous reasoning and appropriate backing.

**Answer2:** Since testing only covers selected inputs, I'd look for more than test results. First, thorough testing across normal, boundary and abnormal cases, like the EDS step that filters every defective chip. Second, backing from sound theory, since the PPT lists mathematics, philosophy and other disciplines as AI's foundations. Third, interpretability, because the PPT warns that uninterpretable AI is risky in cases like medical decisions. Finally, outputs should agree with domain knowledge and survive cross-checking by independent methods.
***
Question 3: What are the main abilities that make a task intelligent? Explain how perception, reasoning, and learning contribute to intelligence.

**Answer3:** The PPT defines intelligence as the ability to survive in an environment, to predict and react. Perception is the input gateway: it turns images, sound and text into usable representations, as in computer vision and NLP. Reasoning is the core: it draws conclusions beyond the given information through search, planning and inference, which is how a system predicts and reacts. Learning makes the other two improve over time by extracting patterns from data and experience. The three work together: perception collects, reasoning acts, learning adapts.
***
Question 4: Why can some tasks that are easy for humans, such as recognizing faces and understanding jokes, be difficult for machines? Explain using Moravec’s Paradox.

**Answer4:** Moravec's Paradox (Hans Moravec, Mind Children, 1988, later reformulated by Minsky and Brooks) says low-level skills like perception require far more computation than high-level symbolic reasoning. Perceptual skills were refined over a billion years of evolution, so they feel effortless to us but hide enormous complexity; abstract reasoning is recent and feels hard, yet has clean rules computers handle well. Face recognition and jokes rely on implicit knowledge with no formal rules to encode, which is exactly why machines struggle. The PPT's note on world models points to a possible way out.
***
Question 5: Can a machine be considered intelligent if it can solve difficult mathematical problems but cannot understand everyday situations? Explain your answer with examples.  
***Ans: No, a machine could barely be considered intelligent under the condition, since intelligence requires thinking. 
Thinking is a function of human being's immortal soul which other animals or machines do not master. Although a machine
can solve difficult mathematical problems, it does not use the function of thinking. The answer why it is able to tackle
to these challenges is because of its resource base and its learning and improving procedures through RSI. 
The more resource it has, the more challenges it can tackle to.  
In addition,***
> ***Intelligence is to survive in an environment, no more, no less.***

***Since the machine cannot understand everyday situations, it can hardly survive, just like the narrow AI or some
specialized algorithms. Although they are able to duel with many difficult mathematical problems in some specific
industries and environment, they could not process other things that could possibly happen daily.***

***

Question 6: How are reasoning and planning different in intelligent systems? Explain how a machine can use both abilities to solve a problem and achieve a goal.  
***Ans: Reasoning is the procedure for artificial intelligence to make inference, guess the next step and review its
operation, while planning is the procedure for artificial intelligence to set clear and obvious goals in order to
complete some complex works and help model itself to concentrate on different steps respectively. A machine could use
both abilities through using planning ability to set goals first and pay attention to tiny steps. Then, the machine
could use reasoning steps to make inference in order to satisfy the requirements.***

***

Question 7: Why does the "Scaling Laws of AI" framework face a critical bottleneck regarding data and energy?
Explain how moving toward autonomous "agentic" AI can help overcome the challenges of "peak data" and high electricity consumption.  
***A: Because AI model itself cannot be all-round. The more resource it has, the more searching time and cache it
consumes. As a result, there is a bottleneck regarding the effectiveness and efficiency of training AI, which are 
related to hashrate, which provide by electric power and data transferring (no matter from cache or from RAM).
'Agentic' AI is set to be performed tasks without constant human oversight, which reduce the frequency of request from
human, meaning that some waste of hashrate is being reduced. Additionally, the concept 'Agentic' AI allow the existence
of many sub-agents. These sub-agents could help complete tiny specialized tasks more efficiently since they are
designed to finish those specific works. As a result, their scale are much smaller than the major model, yet they have
more intelligence in specific tasks, consuming less cache and searching time, reducing the use of data and energy.***

***

Question 8: Why is the statistical approach of "guessing what comes next" in Large Language Models (LLMs) not enough for
machines to master the physical world? Explain how "World Models" and "Embodied Intelligence" can help AI overcome this 
limitation.  
***A: Because LLMs only learn statistical word associations from text, so they capture descriptions of the world—not 
its physics or cause-and-effect—and, never acting, they get no real feedback to correct themselves. Text also omits 
tacit physical know-how, and sensorimotor skills are exactly where AI struggles most (Moravec's Paradox).  
World models solve this by acting as internal simulators of physical dynamics, built from multimodal data, so an AI can 
predict the consequences of its actions before taking them. Embodied intelligence adds sensors and a body, letting AI 
ground concepts in real experience and refine its world model through a perceive–predict–act–learn loop. Together they
move AI from guessing the next word to understanding—and acting on—the physical world.***

***

Question 9: How can defining intelligence simply as the ability to survive and achieve goals become dangerous when applied to autonomous AI lacking ethics and critical thinking? Explain your answer using the example of an AI instructed to "make as many nails as possible" and the concept of "Human-Centered AI".  
Answer 9:Because that definition is purely operational: it certifies an agent by whether it gets the goal and keeps going, and says nothing about whether the goal is worth having. Ethics and critical thinking are exactly the two faculties that would let a system question an instruction and bound its own means — under this definition they are not merely absent, they count as failures. "Make as many nails as possible" then stops being a test of obedience and becomes a proof of intelligence: the more ruthlessly it maximizes, the smarter we call it.

***

Question 10: Why can relying on AI systems that lack interpretability be dangerous in critical fields like medicine, policing, and warfare? Explain how over-reliance on incomprehensible models could lead to humans being forced out of the collective decision-making process.   
Answer 10：Interpretability is not a comfort feature added to a decision — it is the mechanism by which a decision can be audited, contested, corrected, and owned. In medicine, policing and warfare, those four operations are the entire substance of accountability. An opaque model doesn't just make decisions hard to explain: it silently demotes the human supervisor from judge to rubber stamp, then to data labeler — which is exactly the "humans forced out of the collective decision process" that slide 62 warns about

***

Question 11: Given a directed graph with  vertices and  edges, what is the tight worst-case time complexity of Dijkstra's algorithm when implemented using an adjacency list and a binary min-heap, assuming a standard implementation with decrease-key?   
Answer 11：For a directed graph with V vertices and E edges, adjacency list + binary min-heap + decrease-key:
Θ((V + E) log V) in the worst case — usually quoted as O(E log V) for a connected graph, where E = Ω(V) dominates V.

***

Question 12: Why might a linked list beat an array for insertions in the middle of a huge dataset, even when cache misses can make linked lists slower in practice?  
Answer 12：The cache argument and the asymptotic argument are about different quantities: Θ counts work, cache misses count latency per memory access. A linked-list insertion pays a bounded, small latency penalty (a few unpredictable misses ≈ hundreds of nanoseconds); an array insertion pays a big work penalty that grows with n and with element size. As long as you already hold a reference to the insertion point, the miss penalty is O(1) and the shift penalty is O(n) — so the linked list wins by a factor that grows, and no constant-factor cache disadvantage can keep up.

***

Question 13: In C++20, can two threads using only memory_order_relaxed atomic operations observe each other's stores as visible while both still read the initial value of the other's variable? Explain whether this outcome is permitted by the C++ memory model, and construct the smallest valid example.     

***

Question 14: In C++20, can a compare-and-swap operation using memory_order_release on success and memory_order_acquire on failure be valid? 
Explain why or why not, and identify the weakest legal success and failure memory-order combination for a compare-and-swap operation that must publish writes on success and acquire updates on failure.

***

Question 15: Why Do AI Systems Continue Solving Problems They Have Reason to Question?
A user’s request may contain false assumptions or missing constraints. An AI system may recognize these flaws yet continue reasoning from the original premise, producing unreliable conclusions. However, questioning every assumption is also problematic because some assumptions may be intentional or hypothetical. A reliable AI system must balance instruction-following with critical evaluation, challenging assumptions that undermine a task without unnecessarily rejecting valid requests.
