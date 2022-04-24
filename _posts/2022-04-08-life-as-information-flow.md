---
title: 'What is Life? The emergence of the Top-Down Causal Structure'
date: 2022-04-24
permalink: /posts/2022/04/lifeastopdowncausation
tags:
  - life
  - physics
  - biology
  - mathematics
published: true
comments: true
image: /assets/images/what_is_life_schrodinger.jpeg
summary: Biology systems can be seen as information processing units as the whole organism and also as a collection of hierarchical information processing units. This perspective motivates the information-first approach toward explaining what is life, or more practically, what can be a computable metric to measure the life-ness of things. This article tries to take a computational stance in interpreting this perspective.
---

<!-- Add a single line of comment to prevent the blog post index page from including the following text. -->




<p align = "center">
<img src="/assets/images/bidirectional_causation.png" alt="bi-directional-causation" style="width:70%;"/>
</p>
<p align = "center" style="color:gray;">
Bi-directional causation
</p>



# TL;DR


von Neumann predicted the role of DNA by logical reasoning before the discovery of the structure of DNA. Among his uncountable scientific contributions is the invention of cellular automata in 1948 (without the aid of computers, only pen, and paper!) to elucidate the idea of self-replicating systems which is the key property of living organisms and formed the basis of his Univeral Constructor theory that can be seen as a logical approximate model for the living cells. In this article, I review some of the major ideas that are natural consequences of von Neumann's UC and how it relates to the life as we know it many of which are detailed by Sara Imari Walker based on the idea of top-down causation put forward by 



# The possibility of a Universal Constructor?
The Universal Constructor (UC) is an abstraction proposed by John von Neumann in ?? which can utilize resources in its environment to build any possible thing including itself. To elaborate more on the term "any" I have to bring up the concept of universality classes which are the subsets of a hypothetical universe in which a UC operates. As a non-rigorous example, in a universality class that consists of wooden material, a skillful wooden carpenter who is able to make every possible wooden thing is a UC. The carpenter is only the constructor and the instruction to make a certain thing must be given to him otherwise a self-referencing paradox arises when he wants to build himself. The paradox is resolved by separating the instructions (software) from the constructor (hardware) where the software is blindly copied (as a solid physical thing without considering its information content) upon replication. In the carpenter analogy, the recipe to build a chair is sometimes treated as a list of action items that explain in detail what to do to turn a piece of wood into a functional chair, and sometimes as a paper that has to be copied to be handed to the carpenter's child so he can continue his father's profession in making more chairs. But, who decides when that piece of paper has to be read like a bullet list of action items and when it has to be copied just as a piece of paper? von Neumann resolved this issue by introducing another logical component (a supervisory unit) that decides in which way the instruction paper has to be interpreted at a given time.

It was only due to von Neumann's genius that now we see these three components are omnipresent in almost all living things:
  * DNA: Algorithm
  * Ribosomes: Universal Constructor
  * DNA polymerases: Supervisory unit


# Trivial vs Non-trivial replicators

To an astute brain, this title quickly reminds Schrodinger's aperiodic crystals versus the periodic physical crystals. We can identify different replicators which can reproduce their likes but are not categorized as living organisms. To draw the boundary, we must take the laws of physics as given and say those replications that are purely driven by the laws of physics are rather trivial such as periodic crystals (e.g. NaCl or salt). Non-trivial replication is however governed by an abstract instruction set whose shortest description is comparable to the instruction set itself. In other words, non-trivial replicators cannot be compressed while the repetitive structure of trivial replicators allows for large compression gain. Notice that non-trivial replicators are also governed by the laws of physics but the replication itself is not a natural consequence of these laws, rather explicitly planned in the instruction set.

* Trivial replicators: 
  * Instruction set: Laws of physics
  * Only one mode of operation
  * $x_{t+1} = f(x_t)$; The update rule does not depend on the state.
* Non_trivial replicators:
  * Instruction set: Explicitely programmed (e.g. genome)
  * Infinite modes of opertations all within the physical constrains
  * $x_{t+1} = f_{x_t}(x_t)$: The update rule depends on the state.


# Hypothesis 1 on life's origin: Code becomes isolated from the Constructor

In light of the abovementioned dichotomy, it seems the sharp transition from non-living to living things occurs when the code becomes isolated from the constructors. There is indeed a chemical distinction in cells that support this hypothesis. The code (DNA) inhabits the worlds of nucleic acids while its products (proteins) live in the space of peptides. The communication is carried out by the bilingual molecules, i.e. messenger RNAs.

# Hypothesis 2 on life's origin: Top-down causation

This is an interesting hypothesis that needs further elaboration to become clear for a general audience. In abstract terms, top-down causation in this context means that the information (which is instantiated in a physical object e.g. DNA molecule) causes the organism and the organism itself causes the material in which the information is instantiated. Let's make it a little clear using a mental model.


<p align = "center">
<img src="/assets/images/man_inside_a_humanoid.jpeg" alt="man inside a humanoid" style="width:70%;"/>
</p>
<p align = "center" style="color:gray;">
A man controlling the humanoid as an example of bi-directional causation (Source: Hankook Mirae Technology)
</p>




Assume you are the operator of a large humanoid robot and you sit inside the robot and control its hands and legs by some connected pedals. Your hands are tied to the mechanical hands of the robot and cannot be released. You receive a visual signal from the outside world and operate the robot accordingly. You see a green wall in your way and assume it is a grasslike structure and decide to destroy it by the robot's hands to open your way. Unfortunately, the green wall is painted concrete and causes the breakage of your robotic arm. Your hand will also become disabled as it is connected to the robot's arm. Your brain had the prior information that greenness is a sign of lightness or softness which made you decide to go ahead and destroy the wall. This information causes your decision that consequently broke your robotic hand which reduced your action space in the future. You will no longer be able to use your hand which is tied to the broken robot's arm. Hence, the physical feedback from the higher level affected you as the hardware that carries the information and also the information itself while that physical feedback was caused by the information in the first place. Hence, your thought (information) had a pathway to affects its physical carrier (you) and limits its capacities. 



{% if page.comments %}
<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://http-distantvantagepoint-com.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}


