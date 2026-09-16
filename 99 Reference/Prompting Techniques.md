# Practical Manual for Prompting ChatGPT Effectively

## 1. The Core Principle

Good prompting is not primarily about writing extremely long instructions.

It is about giving the model enough information to correctly determine:

**What am I doing? → What do I need from you? → At what level? → In what form? → Under what constraints?**

The conversation above repeatedly failed because one or more of these were left implicit.

---

# 2. The Five Things a Good Prompt Should Establish

### 1. Context — What are we working on?

> “I am designing a fictional biological framework for Naruto.”

### 2. Objective — What do you want me to do?

> “Help me identify the intermediate concepts.”

### 3. Scope — What part are we working on?

> “Only Bloodline Inheritance, not the entire chakra system.”

### 4. Level — How detailed should the answer be?

> “Give me high-level categories, not mechanisms.”

### 5. Output constraints — What should the answer look like?

> “Give me 5–7 items with a one-line explanation each.”

This is the basic prompting structure.

---

# 3. The Biggest Prompting Mistake in the Example

You asked:

> “Help me Identify the intermediate concepts for a bloodline inheritance to work.”

You knew what **“intermediate”** meant in your head.

I did not.

I interpreted it as permission to produce fairly detailed biological mechanisms.

### Better prompt

> “I am building a Bloodline Inheritance framework. I already know I need concepts such as conditions for occurrence, development, and activation. Help me identify the **intermediate-level categories** that sit between the overall concept and detailed mechanisms. Keep them broad enough to later contain several subtopics. Do not give me detailed biology yet.”

The important improvement is not verbosity.

It is **defining the level of abstraction**.

---

# 4. Always Specify the Job You Want Done

Compare:

> “epigenetic inheritance?”

This can mean:

- Define it.
    
- Explain it simply.
    
- Compare it to Bloodline Inheritance.
    
- Tell me whether my model is epigenetic.
    
- Help me use it as fictional inspiration.
    

Your intention became apparent only through several turns.

A better prompt would be:

> “Explain epigenetic inheritance in simple terms, then tell me whether it provides a useful analogy for my Bloodline Inheritance model.”

---

# 5. Tell the Model What You Already Know

One of the most useful prompting techniques is **state management**.

Instead of making the model reconstruct your thinking:

> “I already distinguish Development, Strengthening, and Activation. I want to know whether Strengthening deserves to remain a separate intermediate category.”

This prevents the model from repeatedly proposing concepts you have already settled.

---

# 6. Explicitly Separate Exploration From Finalization

There are two very different activities.

### Exploration

> “Give me several possible ways to structure this.”

### Evaluation

> “Compare these structures and identify their differences.”

### Refinement

> “Modify my existing structure without replacing it.”

### Finalization

> “Produce the final hierarchy.”

Tell the model which activity you're performing.

Otherwise, it may assume you want a finished answer when you are actually brainstorming.

---

# 7. Use Constraints to Control the Model

Constraints are among the most effective prompting tools.

For example:

> “Only give me high-level concepts.”

> “No examples.”

> “Don't introduce terminology yet.”

> “Don't use real-world categories unless they help explain the concept.”

> “Maximum 7 items.”

> “One sentence per item.”

These are not unnecessary restrictions. They reduce ambiguity.

---

# 8. Learn to Correct the Model Precisely

Your corrections such as:

> “dude do not go so deep”

were understandable, but they leave the model to infer **what “too deep” means**.

A stronger correction identifies the exact failure:

> “You're giving me mechanisms. I need categories that can contain those mechanisms. Move one abstraction level upward.”

That teaches the model exactly how to adjust.

Another example:

Instead of:

> “This is a sub issue description not a definition.”

Use:

> “I am writing a GitHub sub-issue description. Rewrite my notes as a statement describing what this issue will investigate. Do not define the concept itself.”

---

# 9. Use “Negative Instructions” Carefully

Tell ChatGPT what **not** to do when it is likely to make a recurring mistake.

For example:

> “Do not answer with established scientific terminology yet.”

> “Do not expand the categories into subcategories.”

> “Do not reinterpret my fictional model as a standard biological taxonomy.”

Negative instructions are particularly useful after you've observed a failure pattern.

---

# 10. Give the Model a Reference Point

When discussing an evolving framework, show its current state.

For example:

> “Current structure:  
> Origin  
> Heritability  
> Establishment  
> Development
> 
> I am trying to determine what belongs after Development.”

This is far better than asking:

> “What concepts should Bloodline Inheritance have?”

The first asks for **local refinement** rather than reconstruction.

---

# 11. Ask One Cognitive Task at a Time

Your conversation sometimes moved through:

**definition → biology → analogy → fictional interpretation → taxonomy → terminology**

That is intellectually reasonable, but each is a different task.

A strong workflow is:

**Understand → Compare → Design → Structure → Name → Formalize**

For example:

> “First, help me understand the biological concept. Don't apply it to Naruto yet.”

Then:

> “Now compare that concept with my Sharingan model.”

Then:

> “Now help me incorporate the useful parts into our fictional framework.”

This dramatically reduces conceptual drift.

---

# 12. Prompting for Terminology

When searching for a name, specify what kind of word you need.

You eventually asked:

> “I want a adjective the collates chakra and its related stuff into a umbrella... system? concept?”

That contains two different questions:

**Grammatical form:** adjective or noun?  
**Semantic scope:** what exactly must it encompass?

A stronger prompt:

> “I need an **umbrella noun** for the entire domain encompassing chakra production, storage, circulation, pathways, transformation, manipulation, and Bloodline Inheritance. I am naming the domain itself, not describing an individual ability. Give me 5 terminology options and explain the semantic difference between them.”

Now the model has a constrained lexical task.

---

# 13. Ask for Reasoning Through Comparisons, Not Just Answers

Instead of:

> “Is Chakra Mechanics correct?”

Use:

> “Compare ‘Chakra Mechanics’, ‘Chakra System’, and ‘Chakra Framework’ based on scope, meaning, and how naturally each works as the name of a fictional domain.”

This makes the model expose the relevant distinctions rather than simply producing a verdict.

---

# 14. A Useful Prompt Template

For serious conceptual work, this template is usually sufficient:

> **Context:** [What I am working on]
> 
> **Current model:** [What I have already established]
> 
> **Task:** [Exactly what I want you to do]
> 
> **Level:** [High-level / intermediate / detailed]
> 
> **Scope:** [What is included/excluded]
> 
> **Constraints:** [Length, format, things not to introduce]
> 
> **Goal:** [What I intend to use the result for]

You do not need to fill every field every time.

---

# 15. Diagnose the Problem Before Rewriting the Prompt

When ChatGPT gives a bad answer, ask:

**Did it misunderstand the context?**

→ Add context.

**Did it misunderstand the task?**

→ State the operation explicitly.

**Did it answer at the wrong depth?**

→ Specify abstraction level.

**Did it produce the wrong type of thing?**

→ Specify the output type.

**Did it overwrite my ideas?**

→ State what is already fixed.

**Did it introduce irrelevant knowledge?**

→ Define scope/exclusions.

This is the fastest way to improve a prompt.

---

# 16. Your Most Important Lesson From This Conversation

Your natural prompting style is often:

> **“Here is what I'm thinking. Help me with it.”**

That works surprisingly well for conversation, but it leaves many parameters implicit.

Your biggest improvement would be learning to convert:

> **implicit intent**

into:

> **explicit task + level + scope + constraints.**

You do **not** need to become excessively verbose.

A 25-word prompt with the right constraints can be much better than a 300-word prompt describing everything you've ever thought about the subject.

---

# 17. Example: Your Original vs Improved Prompt

### Original

> “what among the effects discussed is a new faculty??”

### Improved

> “Within our current Sharingan model, classify the effects we discussed into **new faculties versus enhanced existing faculties**. Use only the effects already mentioned. Don't introduce additional Sharingan abilities.”

This removes three ambiguities:

**classification criterion + dataset + scope.**

---

# 18. A More Advanced Technique: Specify the Relationship

When constructing frameworks, often the important question isn't:

> “What concepts exist?”

but:

> “How do these concepts relate?”

For example:

> “I have Origin, Heritability, Development, Strengthening, Activation, and Transmission. Determine whether these form a chronological sequence, a dependency structure, or whether some should instead be overarching constraints.”

This is a much more powerful conceptual-design prompt.

---

# 19. Your Prompting Checklist

Before sending a serious question, mentally check:

**What am I building?**  
**What exactly do I want done?**  
**What do I already know?**  
**What abstraction level do I want?**  
**What should the answer contain?**  
**What should it not contain?**

Those six questions will prevent most of the problems visible in the example conversation.

# 20. The Goal

Do not aim to write “perfect prompts.”

Aim to become good at **communicating the hidden parameters of your thought process**.

The better you become at identifying:

**context → task → scope → abstraction → constraints → desired output**

the more consistently ChatGPT will produce what you actually intended.