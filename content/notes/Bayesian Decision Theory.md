---
title: "Bayesian Decision Theory"
---
-   It is a fundamental statistical approach to the problem of pattern classification. It predicts the outcome not only based on previous observations but also by taking into account the current situation. It uses Bayes Theorem heavily.
    
    -   Bayes' theorem is used to describe the probability of an event based on the prior knowledge of conditions that might be related to the event. For example, if the risk of developing health problems increases with age, Bayes' theorem allows the risk to an individual of a known age to be addressed more accurately. Bayes' theorem states that,
        
        $$P(A \mid B)=\frac{P(B \mid A) P(A)}{P(B)}$$
        
        $$Underlying Truth = \frac{Likelihood \times Belief(Prior Probability)}{Evidence} $$
        
        -   where \(A\) and \(B\) are the events and \(P(B) \neq 0\)
        -   \(P(A|B)\) is a Conditional Probability; the probability of event \(A\) occurring given that \(B\) is true. This is also called Posterior Probability of \(A\) given \(B\).
        -   \(P(B|A)\) is also a conditional probability; the probability of event \(B\) occurring given that \(A\) is true. It can also be interpreted as likelihood of \(A\) given fixed \(B\).
        -   \(P(A)\) and \(P(B)\) are the probabilities of observing \(A\) and \(B\) respectively, without any given conditions; they are also known as marginal probabilities.
    
-   Working of Bayesian Decision Theory:
    -   Let's say we have features from a vector \(x \in R^d\). A finite set of \(c\) categories \(w_1, w_2, ..., w_c\). So using Bayes' rule,
        
        $$ P\left(\omega_j / \mathbf{x}\right)=\frac{p\left(\mathbf{x} / \omega_j\right) P\left(\omega_j\right)}{p(\mathbf{x})} $$
        
        where \(p(\mathbf{x})=\sum_{j=1}^c p\left(\mathbf{x} / \omega_j\right) P\left(\omega_j\right)\)  
        
    -   A finite set of \(I\) actions \(\alpha_1, \alpha_{2, \ldots}, \alpha_I\). A loss function \(\lambda\left(\alpha_i / \omega_j\right)\). The cost associated with taking action \(\alpha_i\) when the correct classification category is \(\omega_j\)
    -   Suppose we observe \(x\) and take action \(\alpha_i\), and the cost associated with action \(\alpha_i\) with \(\omega_j\) being the correct category is \(\lambda (\alpha_i / \omega_j)\).
    -   The **conditional risk** (or **expected risk**) with taking action \(\alpha_i\) is:
        
        $$R\left(a_i / \mathbf{x}\right)=\sum_{j=1}^c \lambda\left(a_i / \omega_j\right) P\left(\omega_j / \mathbf{x}\right)$$
        
    -   Suppose \(\alpha(x)\) is a general decision rule that determines which action \(\alpha_1, \alpha_2, ... , \alpha_I\) to take for every x; then the overall risk is defined as:
        
        $$ R=\int R(a(\mathbf{x}) / \mathbf{x}) p(\mathbf{x}) d \mathbf{x} $$
        
    -   For each sample, the **Bayes Decision Rule** minimizes \(R\) by:
        -   Computing \(R(\alpha_i / x)\) for every \(\alpha_i\) given an \(x\).
        -   Choosing the action \(\alpha_i\) with the minimum \(R(\alpha_i/x)\).
        -   The resulting minimum overall risk is called **Bayes Risk** and is the best performance that can be achieved:
            
            $$R^* = min(R)$$
            
-   Why is Bayes' Classifier is the best classifier?