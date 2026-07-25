# How to Use AI Chatbots Wisely in Education

## Background

Today, there are two competing views of AI chatbots in education:

- AI chatbots can replace teachers and are the future of education.
- AI chatbots allow students to skip the learning process and are destroying education.

Both positions are clearly extreme, yet each is valid from its own perspective.
The tension exists because AI is a tool with no inherent position or methodology.
Because AI tools are so efficient, different ways of using them produce noticeably different outcomes almost immediately.

In education, students are constantly looking for answers to different kinds of questions.
But simply “getting the answer” is never meaningful in itself.
After all, educational questions are carefully designed sandbox problems.
What matters is how students grow while searching for the answer:
Did they internalize knowledge, skills, or wisdom through thinking?
Did the process make them more mentally agile, enthusiastic, resilient, or humble?
For this reason, getting an answer directly from AI defeats the purpose of education.
But AI can do far more than complete students’ homework and assignments for them. It can play many different roles, several of which can support student growth.

This lesson plan explores constructive ways to use AI chatbots in education.
Its goal is to help students respond proactively rather than passively as the broader shift toward AI becomes unavoidable—and even learn to benefit from it.

## Example Conversation

> What is the largest prime number below 100?

The largest prime number below 100 is 97.

98 is divisible by 2, 99 is divisible by 3, and 97 is not divisible by any of 2, 3, 5, or 7. Therefore, 97 is prime.

> Please explain what a prime number is and the mathematical process used in the question above. I am an elementary school student and do not understand.

**What is a prime number?**

A prime number is a number greater than 1 that can be divided evenly **only by 1 and itself**.

“Divided evenly” means that nothing is left over after division.

Here are a couple of examples:

- The number **7**: Imagine sharing seven candies equally. You can divide them evenly among one person (seven candies each) or seven people (one candy each). If you try to divide them among two or three people, some will be left over. Therefore, 7 is prime.
- The number **6**: Six candies can be divided evenly among one, two, three, or six people (three candies each for two people or two candies each for three people). Because 6 can be divided by 2 and 3 in addition to 1 and itself, it is **not** prime.

**How to solve the question above**

The question asks for the largest prime number below 100. Since we want the “largest,” we can start at 100 and check the numbers one by one as we count down:

- **99**: Can it be divided by smaller numbers? Yes. 99 = 9 × 11, so it is divisible by 3, 9, and 11. ❌ Not prime
- **98**: 98 is even, so it is divisible by 2 (98 = 2 × 49). ❌ Not prime
- **97**: Try dividing it by smaller numbers:
  - By 2? No, because 97 is odd.
  - By 3? No, because 9 + 7 = 16, which is not a multiple of 3.
  - By 5? No, because its last digit is neither 0 nor 5.
  - By 7? No, because 7 × 13 = 91 and 7 × 14 = 98, neither of which equals 97.

No smaller whole number divides 97 evenly. It is divisible only by 1 and itself. ✅ **Therefore, 97 is prime and is the largest prime number below 100.**

> Why not start at 1 and count upward?

You absolutely **can** start at 1 and count upward, and you will eventually find 97. Both methods are correct; the only difference is how long they take.

The key is that the question asks for the **largest** prime number.

If you start at 1, you will encounter 2, 3, 5, 7, 11, 13, and many more prime numbers along the way. You cannot know which one is the largest until you have checked every number close to 100 to make sure there is nothing larger. That means checking many numbers.

If you start at 100 and count downward, the first prime number you encounter must be the largest. Once you have checked that 98 and 99 are not prime, you can stop as soon as you reach 97 and say, “That’s it!”

Here is an analogy:

Imagine that a group of children is standing in a line from shortest to tallest, and you need to find the **tallest** child. You could start with the shortest child and check everyone in order, but that would take a while. It would be faster to go directly to the tallest end of the line and work backward.

So it is not that you *cannot* start at 1. Starting at 100 and counting down is simply **more efficient**. 😊

> Could you turn this mathematical process into a Python program so that I can answer questions about the largest prime number below any given number?

Of course. Here is a simple, easy-to-understand program.

Its approach is exactly what we just discussed: **begin with the number you provide, count downward, and stop at the first prime number you find.**

```python
# Check whether a number n is prime
def is_prime(n):
    if n < 2:              # Numbers below 2 are not prime
        return False
    for i in range(2, n):  # Try dividing n by every number from 2 to n-1
        if n % i == 0:     # If it divides evenly, n has another factor
            return False   # Therefore, n is not prime
    return True            # If none divide evenly, n is prime

# Find the largest prime number below limit
def largest_prime_below(limit):
    for num in range(limit - 1, 1, -1):  # Count down from limit-1
        if is_prime(num):                 # Stop at the first prime
            return num                    # Return it

# Use the function
print(largest_prime_below(100))   # Prints 97
```

Here are a few details:

- The `%` in `n % i` is the remainder operator. For example, `98 % 2` gives 0, so 98 is divisible by 2. `97 % 2` gives 1, so it does not divide evenly. This is how the program checks divisibility.
- The `-1` in `range(limit - 1, 1, -1)` means **count downward**, matching our approach of counting down from 100.
- To check a different number, replace `100` on the final line with any number. For example, `largest_prime_below(50)` returns 47.

If you have trouble running it or want me to explain how to use it on a computer, just ask.

> Does this problem offer any lessons beyond mathematics?

Yes. I think this small problem contains several interesting lessons.

**1. Sometimes working backward from the goal is smarter than starting at the beginning.**

We want to find the largest prime number, so we begin at 100 and count down, stopping as soon as we find one. This approach is often useful in life as well. If you know exactly what you want, you may not need to explore everything from the beginning. Starting from the goal and working backward can be faster.

**2. Large problems can be broken into smaller problems.**

Determining whether 97 is prime may seem difficult, but we can break it into small questions: Is it divisible by 2? By 3? And so on. A difficult problem becomes easier when handled one small piece at a time. Whenever something feels too difficult to begin, try dividing it into smaller parts.

**3. Knowing when you have enough information to stop is also a skill.**

Once we find 97, we stop immediately instead of wasting effort checking smaller numbers. Knowing when you have reached the answer can save a great deal of work.

**4. Tools can repeat tedious work for us.**

Once we have written the program, we no longer need to check every number ourselves whenever we face the same kind of problem. People teach a smart process to a machine, and the machine handles the repetitive work. This is one of the most useful aspects of programming.

I think it is worthwhile when a small question about prime numbers can also teach us these ideas.

> Does this problem connect to more advanced science and engineering?

Yes, and the connections run surprisingly deep. Here are a few of the most interesting ones.

**1. Prime numbers protect the world’s secrets—cryptography**

This is one of the most remarkable uses of prime numbers. When you browse the internet, when a family member transfers money on a phone, or when you enter a password, a kind of “lock woven from prime numbers” helps protect the information behind the scenes.

The underlying idea is clever: multiplying two very large prime numbers is easy, but starting with their product and determining the original two primes is extremely difficult. Even a supercomputer could require a very long time. Because attackers cannot easily break the lock, the information remains safe. Much of internet security rests on the difficulty of factoring numbers into primes.

**2. Nature also “uses” prime numbers—the secret of cicadas**

Some cicadas in North America spend most of their lives underground and emerge only once every **13 years** or **17 years**. Scientists have observed that both 13 and 17 are prime numbers, and that may not be a coincidence. A prime-number life cycle may help cicadas avoid regularly coinciding with the life cycles of predators. A small insect can therefore have a surprising connection to prime numbers.

**3. “How can we calculate faster?” is a major field of study—computer science**

Remember how counting down from 100 saved us work? In science and engineering, finding a way to complete a calculation in the fewest possible steps is an extremely important and valuable problem. To determine whether a number with hundreds of digits is prime, researchers have invented methods billions of times faster than our simple program. The study of computational efficiency supports the entire modern computing world.

What I find most remarkable is this: **Prime numbers may look like a quiet, simple idea from a mathematics textbook, yet they are working behind the scenes in the internet, nature, and supercomputers. The simplest and most fundamental ideas often have the widest and deepest uses.**

> Please provide sources for the answers above.

That is a good request—checking sources reflects a serious approach to learning. I will look for reliable support for the claims above. I found a reliable source for the cryptography claim; next I will investigate the cicadas. There is strong support for that claim as well. Finally, I will check the claim about fast methods for testing large prime numbers.

I have finished checking. The earlier claims are supported by reliable sources, which I have organized into three topics below.

**1. Prime numbers and cryptography (RSA)**

This claim is accurate. RSA is one of the most widely used public-key cryptosystems. Its security relies on an asymmetry: multiplying two large prime numbers is easy, while factoring the result is extremely difficult. The computational difficulty of factoring the product of two large primes supports secure communication, digital signatures, authentication, and other forms of modern digital security. One additional detail: a 2048-bit key is currently considered a minimum acceptable standard, which means the prime numbers used in practice are vastly larger than those in our example.
Sources: Splunk’s introduction to the RSA algorithm, Entro’s security glossary, and the Prime Pages at t5k.org.

**2. Prime numbers and cicadas (13- and 17-year cycles)**

This connection is real and is a classic example in science. A life cycle with a prime-number length—13 or 17 years—may prevent predators from evolving life cycles that are exact factors of the cicadas’ cycle. This matches the earlier explanation: for example, cicadas on a 12-year cycle could regularly coincide with predators on two-, three-, four-, or six-year cycles. Entomologists Monte Lloyd and Henry Dybas formally proposed this predator-avoidance idea in a 1966 paper. Evolutionary biologist Stephen Jay Gould later helped popularize it in a 1977 article.
Sources: Nature Education’s Scitable resource and a SpaceDaily report.

**3. Prime numbers and “calculating quickly” (computer science)**

This claim is also accurate. A trial-division approach like the one in our program becomes impractically slow for very large numbers. Although many probabilistic algorithms already existed, in 2002, Manindra Agrawal, Neeraj Kayal, and Nitin Saxena introduced what became known as the AKS algorithm—the first deterministic algorithm that could determine whether a number was prime or composite in polynomial time. To be precise, however, AKS is a landmark in computational number theory but is not very practical. It becomes faster than commonly used methods only at input sizes beyond present computational capabilities. In practice, faster methods such as Miller–Rabin are more commonly used.
Sources: The AKS paper on arXiv and the Wolfram MathWorld entry.

One honest caveat: most of the sources above are educational websites or encyclopedic references. They are suitable for an elementary-school explanation but are themselves secondary sources. For formal academic work, it is better to find the original research, such as the 1966 paper by Lloyd and Dybas and the 2002 AKS paper. Those are the most authoritative sources.

> Please give me another question of about the same difficulty. Do not make it too different.

Here is one:

**What is the largest prime number below 50?**

The approach is exactly the same as before, except that 100 has been replaced with 50. Try checking the numbers one at a time as you count down from 50.

I will not reveal the answer yet. Tell me what you think, and we will check it together. 😊

> 49

Almost—just check 49 once more.

49 is divisible by 7: **7 × 7 = 49**. Because it can be divided by 7 in addition to 1 and itself, 49 is **not** prime.

Here is a small hint: The number below 49 is 48, which is even and therefore divisible by 2. The next number is 47. Would you like to check whether 47 is divisible by 2, 3, or 5?

## Lesson Plan

**Course title:** Using AI Wisely: From “Getting Answers” to “Learning to Think”  
**Audience:** Upper elementary through middle school students  
**Length:** Half-day or full-day lecture and workshop, delivered in person or online  
**Core idea:** AI is not a machine that thinks for you; it is a partner that helps you think better.

---

**Part 1 · Cognitive Offloading (An Example of What Not to Do)**

Demonstration: Ask AI only for an answer (“What is the largest prime number below 100?”).  
Key point: Taking the answer directly does not merely skip one calculation; it skips the foundation of understanding. For students who are still building that foundation, this is a red line.

**Part 2 · Treat AI as a Teacher**

Demonstration: Ask follow-up questions such as “What is a prime number?” and “Why not start at 1 and count upward?”  
Key point: Turn AI from an “answer machine” into an “explainer,” using questions to drive understanding.

**Part 3 · Turn the Learning into a Reusable Tool**

Demonstration: Ask AI to write a small program that tests prime numbers.  
Key point: Transform a one-time thinking process into a tool that can be reused later.

**Part 4 · Inspiration and Extension**

Demonstration: Ask “What lessons does this offer beyond mathematics?” and “How does this connect to science and engineering?” Explore topics such as RSA and cicada life cycles.  
Key point: Use AI to broaden students’ horizons. It is okay if they do not understand everything; the goal is to spark curiosity, not achieve complete mastery.  
Teacher note: Before going deeper, tell students that they are only expected to listen for something interesting. Afterward, return to a simple question to prevent cognitive overload.

**Part 5 · Verify the Sources**

Demonstration: Ask AI to provide sources and discover together that many are secondary popular-science sources—and that AI may even cite something incorrectly.  
Key point: AI can be wrong. Do not trust it blindly. Verify information independently and trace claims back to original sources whenever possible. This is the most important skill in using AI.

**Part 6 · Check My Growth**

Demonstration: Have AI provide a new question, let the student answer (“49”), and then receive feedback and correct the mistake.  
Key point: Use AI to check whether the student has genuinely learned the concept.

---

**Workshop (adjust the length for a half-day or full-day course)**

Give each student a short problem. The rule is that students may not ask directly for the answer; they must question AI step by step, as shown in the demonstration.

The final submission is not an answer but a “learning journey” containing three things: a record of follow-up questions, a small AI-generated tool, and an independent check of one of the AI’s sources.

## Sample Workshop Questions

Each of the following questions is about as deep as the prime-number problem, and each can be explored through understanding, tool-building, extension, and verification.

**1. How many numbers below 100 are divisible by 3?**

The basic approach is similar to the prime-number problem. Students can count the numbers one by one or discover the pattern in `100 ÷ 3`.  
Extensions: Build a program that counts multiples within any range; explore the divisibility rule for 3—a number is divisible by 3 if the sum of its digits is divisible by 3—and investigate why it works.

**2. A number leaves a remainder of 2 when divided by 3 and a remainder of 3 when divided by 5. What is the smallest possible number?**

This requires trial and error as well as reasoning, adding one more layer beyond straightforward calculation.  
Extensions: This is an early form of the ancient “Han Xin Counts the Soldiers” problem and the Chinese remainder theorem. It can lead to cryptography and calendars, or students can write a small program to solve it automatically.

**3. What is the sum of all the numbers from 1 to 100?**

This classic problem can be solved by adding every number or by discovering the clever idea of pairing the first and last numbers: 1 + 100, 2 + 99, and so on.  
Extensions: In the “AI as teacher” approach, have AI guide students to discover the pairing pattern instead of giving them the formula. The story of the young Gauss also offers an encouraging connection.

**4. How tall would a sheet of paper become if it could be folded 30 times?**

The answer is surprising—it would exceed 100 kilometers—and can create a strong sense of wonder.  
Extensions: This question naturally leads to exponential growth and its connections to viral spread, compound interest, and Moore’s law. It is also ideal for verification: Have students question whether the result is really possible and independently check the paper thickness and calculation.

**5. Can you use four 4s to make every whole number from 1 to 10?** For example, `4 ÷ 4 = 1` and `4 ÷ 4 + 4 ÷ 4 = 2`.

This is the most open-ended question and has many possible solutions, encouraging experimentation.  
Extensions: It works well with both the “AI as teacher” and tool-building approaches. Students can ask, “AI gave me one solution—can I find another?” This discourages blind acceptance of a single answer.

Questions 3 and 4 are best suited to the “inspiration and extension” section because they create a strong sense of surprise. Questions 1, 2, and 5 work especially well as hands-on workshop activities because each has a clear questioning path and can lead to a small program.

## Other Constructive Ways to Use AI

Students can try one or two of these approaches during the workshop.

**1. The Feynman Method: I Explain It to AI**

Reverse the roles. Instead of asking AI to explain something to the student, have the student explain what they have just learned and ask AI to identify mistakes or unclear points. This may be the strongest workflow of all because it requires students to **produce** an explanation rather than passively receive one. If they cannot explain something clearly, they probably do not fully understand it.

**2. The Socratic Method: Ask Questions Only—Do Not Give Me the Answer**

Tell AI explicitly: “From now on, ask me questions only. Do not tell me the answer.” AI becomes a guide. This method is especially easy to teach because students can begin using it with a single prompt.

**3. Predict First, Then Check**

Write down an answer or prediction **before** asking AI, then compare the two. The order matters: Commit to an idea first, and verify it afterward. Even if the prediction is wrong, thinking has already taken place, and students will remember “where my reasoning went wrong” more clearly than simply receiving the correct answer.

**4. Diagnose the Sticking Point: Ask Only “Where Did I Get Stuck?”**

Give AI the student’s work but instruct it to **identify only the step where the reasoning went wrong**, without providing the correct answer. The student receives a location to investigate and must repair the solution independently. This preserves the most valuable part of learning: climbing out of the hole yourself.

**5. Please Challenge My Argument**

Present an opinion or method and ask AI to find flaws and counterexamples. This develops resilient thinking rather than seeking agreement. It is especially useful for middle school students and helps counter the belief that “if AI says it, it must be right.”
