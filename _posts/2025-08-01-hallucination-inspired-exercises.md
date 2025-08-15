---
title:  "The Ghost in the Theorem: Confronting LLM Hallucination in the PhD Course"
categories:
  - Machine Learning
  - Research project
tags:
  - Teaching
  - PhD students
  - MSc students
  - Large Language Models
  - Hallucinations
  - research
---

Terence Tao: ["AI-generated proofs can look superficially flawless... but their errors are stupid."](https://youtu.be/HUkBz-cdB-k?si=LNUc8XX5NArudERg)

When the renowned mathematician Terence Tao said this, he perfectly captured the strange paradox of modern artificial intelligence. Today, large language models (LLMs) like ChatGPT are increasingly integrated into daily workflows, helping us write emails, summarize articles, and even code. Their power is undeniable. But as we start relying on them for more critical tasks, like mathematical reasoning, we have to ask: How do we handle their errors, especially when they are hidden under a cloak of confidence?

I wanted to bring this question into the classroom.

During the past spring semester, we conducted with students a small experiment in the PhD-level Machine Learning (ML) course I taught. The course is heavy on math, with homework assignments that require students to construct formal proofs. This provided an opportunity to investigate the capabilities of LLMs in formal reasoning. Given that few days ago frontier models achieved [high performance on International Mathematical Olympiad (IMO) questions](https://deepmind.google/discover/blog/advanced-version-of-gemini-with-deep-think-officially-achieves-gold-medal-standard-at-the-international-mathematical-olympiad/), we were curious: How would they fare with the kind of proofs of the course?

For a few selected problems, I prompted few publicly available, state-of-the-art LLMs to generate the proofs. The resulting text was embedded directly into the homework assignments without modification. Note that the frontier public APIs were used and the resulting text was the output with the 'reasoning' mode on and the first response of the LM. The students' task seemed simple: read the LM's proof, and if it was correct, they would get full credit. Simple, right?

Well, not quite. While some proofs were correct, others were elaborate traps. Students would follow the logic, which flowed with authoritative clarity, step by step... until they hit a wall. An equation or symbol would appear from nowhere. A crucial step in the logic would be a complete leap of faith. Suddenly, the assignment wasn't about passively checking an answer. It was an active exercise in debugging. It brought Terence Tao’s observation to life in our course: the LLM's mistakes weren't subtle miscalculations; they were fundamental errors of reasoning, presented as fact. These hallucinations, incorrect statements delivered with complete confidence, were not just a technical flaw.

Students had to pinpoint the exact moment the reasoning failed. The educational outcomes of the experiment were positive, with student interactions confirming the value of the exercise.

So, what does this experiment tell us about the future of education in the age of AI? First, it highlights an essential new skill: the ability to critically audit and debug AI-generated content. This goes beyond simple fact-checking. It's a form of digital literacy where students learn not just to consume information, but to question its logical structure. Instead of just learning the material, the students were learning how to think alongside—and at times, against—an AI partner. This skill is not just valuable for an ML class; it’s crucial for anyone who will use AI in their professional life, from lawyers reviewing AI-drafted contracts to doctors interpreting AI-driven diagnostics.

This also forces us to imagine how our roles as educators will evolve. Think about how calculators changed math class. They didn't make learning math obsolete; they freed us from mundane manual calculation and allowed us to focus on higher-level conceptual understanding. AI assistants could do the same for fields like mathematics. 

Until then, as we help our students become more critical thinkers, we must also ask: how do we build AI systems we can truly trust?

[Example](https://uwmadison.box.com/s/dhzga31c3wogbjwiadfuadk31kvuns4m) of the LLM proof.


If you have any further questions or feedback on the article, please feel free to get in touch. Here is the link with some of those exrercises as I reran them recently. 