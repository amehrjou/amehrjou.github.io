---
title: "The Randomness of Meritocracy Under Overload"
date: 2025-08-26
permalink: /posts/2025/08/randomness-of-meritocracy
tags:
  - academia
  - psychology
  - statistics
  - systems
  - sociology
published: true
comments: true
image: /assets/images/random_meritocracy.png
summary: An exploration of how overloaded selection systems collapse into randomness, disguised by elaborate procedures that create the appearance of fairness while failing to improve predictive accuracy.
classes: wide
---



<div style="text-align: center; margin: 3em 0;">
  <p style="font-size: 1.2em; color: #666; font-style: italic; letter-spacing: 0.5px;">
    "We are prone to overestimate how much we understand about the world and to underestimate the role of chance."<br>
    Daniel Kahneman
  </p>
</div>

Lately, I've seen many complaints about AI conferences, overloaded review systems, shallow or inconsistent reviews, artificially tuned acceptance rates by ACs, and endless debates about fairness.

None of this surprises me. The issues stem from fundamental incentive problems baked into our publication system. While conferences attempt to patch the process through new constraints, penalties, and workflows, these surface-level fixes cannot repair a system that's fundamentally unstable. And this pattern extends far beyond publications, it's a universal feature of any selection system overwhelmed by external incentives that exceed its processing capacity.

The uncomfortable truth is that when a selection system is overloaded and its evaluations are not strongly predictive of what we truly value (research quality, innovation, long-term impact), the outcomes approach randomness. Decisions start to look like lotteries, even if they're dressed up in complex rules, multi-step workflows, and scoring systems.

## The Disguised Lottery

We can simply express the problem via probability theory. Let each candidate have a true score $Y$ (e.g., future research output, innovation, job performance). Our evaluation process produces an observed score

$$
S = f(Y) + \epsilon,
$$

where $f(Y)$ is the systematic part of evaluation and $\epsilon$ represents noise.

Three conditions matter:

1. **Power:** The evaluation procedure (depth of reviews, quality of interviews, robustness of scoring) must have sufficient **statistical power** to reliably distinguish candidates. Low-power tests inflate error rates and reduce meaningful differentiation.
2. **Signal:** The variance explained by $f(Y)$ must dominate the variance of $\epsilon$.
   $$
   \text{Signal-to-Noise Ratio (SNR)} = \frac{\mathrm{Var}[f(Y)]}{\mathrm{Var}[\epsilon]} \gg 1
   $$
3. **Alignment:** The correlation between $S$ and the true outcome $Y$ must be strong.
   $$
   \rho(S, Y) \approx 1
   $$

If any of these fail: low power, low SNR, or weak alignment, rankings **collapse into noise**. The probability that the top-ranked candidate truly outperforms a random candidate (from the pool of reasonable candidates) approaches 0.5, no better than a coin toss.

It's not an unknown effect and has been shown by several studies in different fields. For example, Chernev, Böckenholt, and Goodman (2015) show that in choice overload, decision accuracy degrades as noise grows. However, apart from this mathematically obvious fact, there is a psychological and sociological factor to it.

## Why Society Resists Admitting the Randomness

Admitting randomness undermines the story of fairness and meritocracy. Instead, we build elaborate scoring systems that **feel structured but lack statistical reliability**. This resistance stems from deep psychological and institutional forces that have been well-documented across multiple disciplines.

Theodore Porter's *Trust in Numbers* (1995) shows how institutions adopt numerical methods not because they enhance accuracy, but because they appear objective and legitimize decisions. Kahneman, Sibony, and Sunstein's *Noise* (2021) demonstrates our tendency to seek patterns and causal narratives rather than accept randomness. When faced with unpredictable outcomes, institutions layer procedures and scoring rubrics to appear consistent and fair, even when statistical evidence shows the results are effectively random.

Research on procedural justice and system justification theory reveals that people care deeply about the fairness of the process, often more than the outcome itself. Even symbolic gestures: having a "voice," transparency, structured evaluation, can satisfy concerns about fairness and reinforce trust in the system without necessarily improving predictive accuracy. The paradox is that these mechanisms protect the system's credibility while doing little to improve its statistical reliability. We end up with increasingly elaborate procedures that feel more legitimate but produce outcomes that are statistically indistinguishable from random selection.

## Familiar Systems That Feel Meritocratic

The mathematical framework I've outlined applies to numerous selection systems that we intuitively believe are meritocratic. Consider PhD admissions: when the correlation between admission criteria and future research success approaches zero ($\rho(S, Y) \approx 0$), admitted students become statistically indistinguishable from randomly selected ones. The elaborate application processes, recommendation letters, and standardized tests create the illusion of precision, but if they fail to predict what truly matters: research creativity, persistence, and long-term contribution, then the entire system operates as a sophisticated lottery.

Paper review systems face similar challenges. When reviewer scores are inconsistent or reviews become shallow due to overload (low statistical power), the signal-to-noise ratio plummets. What emerges is not a reliable ranking of research quality, but rather a noisy ordering that could easily be generated by random assignment. The multi-stage review process, with area chairs and program committees, creates procedural complexity that masks the underlying statistical instability.

Hiring processes, particularly in competitive fields, often fall into the same trap. Without validated predictors or structured, high-quality interviews that actually correlate with job performance, selecting "top talent" becomes no more reliable than drawing names from a hat. Yet organizations invest heavily in elaborate interview processes, case studies, and assessment centers that feel rigorous but lack the statistical power to meaningfully distinguish candidates beyond random chance.

## The Feedback Loop Comes to the Rescue

The good news is that overloaded systems may recover naturally. A useful analogy comes from economics: financial markets often swing between bubbles and corrections. When speculation detaches asset prices from fundamentals, markets appear chaotic. But over time, negative feedback (e.g., losses, capital flight) forces a correction and restores some level of alignment between value and price.

Selection systems behave similarly. Over time, those who assign values (academic positions, industrial hiring, etc.) recognize that their "choices" are indistinguishable from random. But not all entities recognize this at the same pace. Those with higher tolerance for noise, often actors without direct skin in the game, are the last to act. Smaller startups already put less weight on publications. Larger corporations, with more inertia, take longer to adapt. Publicly funded academia, often shielded from immediate consequences, may be the last to react.

As participants move away from this low-SNR environment, submission pressure decreases, the burden lifts, reviews deepen (only truly motivated submitters and reviewers remain), and the signal-to-noise ratio improves.

These systems oscillate: they swing between phases of functioning and breakdown. Unless we rethink the incentives, not just the mechanisms, we will keep repeating the cycle with slightly fancier patches.

---

**References:**

- Chernev, A., Böckenholt, U., & Goodman, J. (2015). [Choice Overload: A Conceptual Review and Meta-Analysis](https://www.researchgate.net/publication/265170803_Choice_Overload_A_Conceptual_Review_and_Meta-Analysis). *Journal of Consumer Psychology, 25*(2), 333–358.
- Kahneman, D., Sibony, O., & Sunstein, C. R. (2021). *Noise: A Flaw in Human Judgment*. Little, Brown Spark.
- Porter, T. M. (1995). *Trust in Numbers: The Pursuit of Objectivity in Science and Public Life*. Princeton University Press.
