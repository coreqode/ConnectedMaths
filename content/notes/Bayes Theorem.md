---
title: "Bayes Theorem"
---
-   Bayes' theorem is used to describe the probability of an event based on the prior knowledge of conditions that might be related to the event. For example, if the risk of developing health problems increases with age, Bayes' theorem allows the risk to an individual of a known age to be addressed more accurately. Bayes' theorem states that,
    
    $$P(A \mid B)=\frac{P(B \mid A) P(A)}{P(B)}$$
    
    $$Underlying Truth = \frac{Likelihood \times Belief(Prior Probability)}{Evidence} $$
    
    -   where \(A\) and \(B\) are the events and \(P(B) \neq 0\)
    -   \(P(A|B)\) is a Conditional Probability; the probability of event \(A\) occurring given that \(B\) is true. This is also called Posterior Probability of \(A\) given \(B\).
    -   \(P(B|A)\) is also a conditional probability; the probability of event \(B\) occurring given that \(A\) is true. It can also be interpreted as likelihood of \(A\) given fixed \(B\).
    -   \(P(A)\) and \(P(B)\) are the probabilities of observing \(A\) and \(B\) respectively, without any given conditions; they are also known as marginal probabilities.
-   Proof of Bayes' Theorem for discrete events.
    
    $$ P(A \mid B)=\frac{P(A \cap B)}{P(B)} \text {, if } P(B) \neq 0 $$
    
    where \(P(A \cap B)\) is the probability of both \(\mathrm{A}\) and \(\mathrm{B}\) being true. Similarly,  
    
    $$ P(B \mid A)=\frac{P(A \cap B)}{P(A)} \text {, if } P(A) \neq 0, $$
    
    Solving for \(P(A \cap B)\) and substituting into the above expression for \(P(A \mid B)\) yields Bayes' theorem:  
    
    $$ P(A \mid B)=\frac{P(B \mid A) P(A)}{P(B)}, \text { if } P(B) \neq 0 \text {. } $$
