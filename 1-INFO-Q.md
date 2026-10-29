Introduction to Computer Science

INFO members: Htet Oo Wei, Yagmur小雨, Mostafa Ahmed, 陈冠男， 郑培丰

Question 1: Can the same set of data lead to different conclusions when processed by two different computer programs? Explain why.

**answer1:** Yes. The same data can easily lead to different conclusions if two programs handle it differently, and the PPT's own formula explains why: AI = Algorithm + Data + Computility. Data is only one of the three ingredients, so identical data says nothing about the other two.

The algorithm part is the most obvious. A CNN and a Transformer are built around completely different assumptions about what matters in the input. Even within NLP, which the PPT describes as basically a game of "guess what comes next," two programs trained on the same corpus can learn different guessing habits. The attention mechanism weights different parts of the context, so the same sentence can produce different continuations.

Then there is scale. The scaling laws in the PPT say performance depends on data size, parameter count and compute together. Two programs using the same dataset but with different parameter counts or different computility will simply not reach the same level, and their conclusions will drift apart.

There are also smaller, less glamorous causes. Preprocessing is never identical: one program might clean outliers aggressively while another keeps them. Training settings like random initialization and optimization choices mean even the same architecture can converge to different models. So no, "same data" does not mean "same answer," and honestly it would be surprising if it did.
***
Question 2: When a computer program produces a result, what evidence should we look for before trusting that result?
Software testing checks selected inputs but cannot guarantee universal correctness. Since no general algorithm can decide every nontrivial correctness property of arbitrary programs, proving correctness requires rigorous reasoning and appropriate backing.

**answer2:** Testing can only cover the inputs someone thought to try, so before trusting a result I would want several kinds of evidence, not just "it passed the tests."

First, the testing itself should be thorough: normal cases, boundary cases, and deliberately broken inputs. The PPT makes a nice parallel from chip manufacturing. The EDS step exists purely to sort out defective chips before packaging, and yield only means something because every chip goes through it. Software deserves the same suspicion: results on standard benchmarks and on real, typical cases should be checked, not just a handful of hand-picked examples.

Second, there should be a theoretical reason to expect the program to work. The PPT lists the foundations of AI as philosophy, mathematics, economics, neural science, psychology, sociology, computer science and engineering, cybernetics, and language and linguistics. The point I take from that list is that a trustworthy system rests on established theory and reasoning, not only on "it seemed to work when we tried it."

Third, I want to be able to see why the program produced its output. The PPT singles out lack of interpretability as a major weakness of today's large language models, and warns that uninterpretable AI can have serious consequences in cases like medical decisions. A result that comes out of a black box is hard to trust even when it looks right, because there is no way to tell whether it is right for the right reasons.

Finally, the output should survive cross-checking: does it agree with what the domain already knows, and can an independent method reproduce it? An AI suggesting a diagnosis still has to make sense against clinical knowledge. If a result only one program can produce and nobody can verify it another way, that is a reason to hold onto it loosely.

Question 3: What are the main abilities that make a task intelligent? Explain how perception, reasoning, and learning contribute to intelligence.
***
**answer3:** The PPT gives a refreshingly blunt definition: intelligence is the ability to survive in an environment, no more, no less, plus the ability to predict and react accordingly. If that is the goal, the abilities that make a task intelligent are perception, reasoning, and learning, and each does a different job.

Perception is how information gets in. It turns raw signals like images, sound and text into representations the system can actually work with, and it covers the AI areas the PPT lists as computer vision and voice/NLP. Without it there is nothing to think about: a system that cannot read its surroundings cannot predict anything in them, let alone survive.

Reasoning is what happens to that information. It means drawing conclusions that go beyond what was directly given, which is why the PPT groups search and planning together with logic and inference as core research directions. Reasoning is the "predict and react" part of the definition made concrete. When a system faces a situation it has never seen, reasoning, not memory, is what carries it through.

Learning is what makes the other two get better over time. Instead of being programmed for every situation, a learning system extracts patterns from data and experience, which is what machine learning and data mining are about in the PPT's list. This is the adaptiveness part: an intelligent system improves without being rewritten.

The three are hard to separate in practice. Perception feeds reasoning, reasoning acts on the world, learning updates both from the results. A system with only one of them looks less like intelligence and more like a very specialized tool.

Question 4: Why can some tasks that are easy for humans, such as recognizing faces and understanding jokes, be difficult for machines? Explain using Moravec’s Paradox.
***
**answer4:** Moravec's Paradox, which the PPT covers directly, is exactly about this reversal: the low-level skills that feel effortless to us, like perception and motor control, turn out to need far more computation than the high-level symbolic reasoning we consider difficult. Hans Moravec first stated the idea in his 1988 book Mind Children, and Minsky and Brooks later reformulated it.

The evolutionary explanation is the one the PPT gives, and I find it the most convincing. Perceptual and motor skills were refined over a billion years of evolution, so by the time we are born they are already built in and run without any conscious effort. Recognizing a face feels easy precisely because we never had to learn it deliberately. Abstract reasoning, by contrast, only emerged in the last hundred thousand years, so it still feels like work to us. Our sense of difficulty measures conscious effort, not computational cost, and that is why it misleads us.

This also explains why faces and jokes resist formalization. Both depend on enormous amounts of implicit knowledge: what a face looks like under any lighting or angle, or the context, timing and shared assumptions a joke needs to land. None of this comes with clean rules we could write down, because we never learned it from rules in the first place. Chess and arithmetic went the other way: fully specified rules, exactly the kind of problem computers were built for, which is why machines beat us there decades ago.

The PPT's list of current LLM limitations lines up with this reading: short of perceptive ability, no arms or legs, weak embodied experience. Interestingly, slide 58 points to world models as the possible way out, letting systems simulate their environment and predict consequences of actions instead of only manipulating text. If Moravec is right about where the difficulty lives, that is exactly the direction the field would have to go.

Question 5: Can a machine be considered intelligent if it can solve difficult mathematical problems but cannot understand everyday situations? Explain your answer with examples.
***
Question 6: How are reasoning and planning different in intelligent systems? Explain how a machine can use both abilities to solve a problem and achieve a goal.

Question 7: Why does the "Scaling Laws of AI" framework face a critical bottleneck regarding data and energy? Explain how moving toward autonomous "agentic" AI can help overcome the challenges of "peak data" and high electricity consumption.  

Question 8: Why is the statistical approach of "guessing what comes next" in Large Language Models (LLMs) not enough for machines to master the physical world? Explain how "World Models" and "Embodied Intelligence" can help AI overcome this limitation.  

Question 9: How can defining intelligence simply as the ability to survive and achieve goals become dangerous when applied to autonomous AI lacking ethics and critical thinking? Explain your answer using the example of an AI instructed to "make as many nails as possible" and the concept of "Human-Centered AI".  

Question 10: Why can relying on AI systems that lack interpretability be dangerous in critical fields like medicine, policing, and warfare? Explain how over-reliance on incomprehensible models could lead to humans being forced out of the collective decision-making process.  

Question 11: Given a directed graph with  vertices and  edges, what is the tight worst-case time complexity of Dijkstra's algorithm when implemented using an adjacency list and a binary min-heap, assuming a standard implementation with decrease-key?                 

Question 12: Why might a linked list beat an array for insertions in the middle of a huge dataset, even when cache misses can make linked lists slower in practice?      

Question 13: In C++20, can two threads using only memory_order_relaxed atomic operations observe each other's stores as visible while both still read the initial value of the other's variable? Explain whether this outcome is permitted by the C++ memory model, and construct the smallest valid example.     

Question 14: In C++20, can a compare-and-swap operation using memory_order_release on success and memory_order_acquire on failure be valid? 
Explain why or why not, and identify the weakest legal success and failure memory-order combination for a compare-and-swap operation that must publish writes on success and acquire updates on failure.

Question 15: Why Do AI Systems Continue Solving Problems They Have Reason to Question?
A user’s request may contain false assumptions or missing constraints. An AI system may recognize these flaws yet continue reasoning from the original premise, producing unreliable conclusions. However, questioning every assumption is also problematic because some assumptions may be intentional or hypothetical. A reliable AI system must balance instruction-following with critical evaluation, challenging assumptions that undermine a task without unnecessarily rejecting valid requests.
