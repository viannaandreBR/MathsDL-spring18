# MathsDL-spring18
Topics course Mathematics of Deep Learning, NYU, Spring 18. CSCI-GA 3033. 

## Logistics

* Tuesdays from 7.10pm-9pm. CIWW 102

* Tutoring Session with Parallel Curricula (**optional**): Fridays 11am-12:30pm CIWW 101. The first week **only** it is 10:30am-12pm.

* Piazza: [sign-up here](https://piazza.com/nyu/spring2018/csciga3033)

* Office Hours: Tuesdays 9:30am-11:00am

## Instructors

__Lecture Instructor__: Joan Bruna (bruna@cims.nyu.edu)

__Tutor (Parallel Curricula)__: Cinjon Resnick (cinjon@nyu.edu)


## Syllabus

This Graduate-level topics course aims at offering a glimpse into the emerging mathematical questions around Deep Learning. In particular, we will focus on the different geometrical aspects surounding these models, from input geometric stability priors to the geometry of optimization, generalisation and learning. We will cover both the background and the current open problems. 

Besides the lectures, we will also run a parallel curricula (optional), which, starting from a landmark recent DL paper (AlphaGo), will trace back the fundamentals of Dynammic Programming, Policy Learning and Monte-Carlo Tree Search through the literature and lab materials. 

### Detailed Syllabus 

*  Introduction: the Curse of Dimensionality

* Part I: Geometry of Data
  * Euclidean Geometry: transportation metrics, CNNs , scattering. 
  * Non-Euclidean Geometry: Hausdorff-Gromov distances, Graph Neural Networks. 
  * Unsupervised Learning under Geometric Priors (Implicit vs explicit models, microcanonical, transportation metrics).
  * Applications and Open Problems: adversarial examples, graph inference, inverse problems.

* Part II: Geometry of Optimization and Generalization
  * Stochastic Optimization (Robbins & Munro, Convergence of SGD) 
  * Stochastic Differential Equations (Fokker-Plank, Gradient Flow, Langevin Dynamics, links with SGD; open problems) 
  * Information Geometry and Optimal Transport (Amari, Fisher-Rao metric, Wasserstein) 
  * Reproducing Kernel Hilbert Spaces 
  * Landscape of Deep Learning Optimization (Tensor/Matrix factorization, Deep Nets; open problems). 
  * Generalization in Deep Learning. 


## Pre-requisites

Multivariate Calculus, Linear Algebra, Probability and Statistics at solid undergraduate level.

Notions of Harmonic Analysis, Differential Geometry and Stochastic Calculus are nice-to-have, but not essential.

## Grading

The course will be graded with a final project -- consisting in an in-depth survey of a topic related to the syllabus,
plus a participation grade. The detailed abstract of the project will be graded at the mid-term. 

## Lectures

| Week        | Lecture Date           | Topic       |  References                     |
| ---------------|----------------| ------------|---------------------------|
| 1 | 1/23  | **Lec1** Introduction: The Curse of Dimensionality in ML [Slides](https://github.com/joanbruna/MathsDL-spring18/blob/master/lectures/lecture1.pdf) |  [References](doc/refs.md#lec1)  |
| 2 | 1/30  | **Lec2** Euclidean Geometric Stability. [Slides](https://github.com/joanbruna/MathsDL-spring18/blob/master/lectures/lecture2.pdf) |  [References](doc/refs.md#lec2)  |
| 3 | 2/6  | **Guest Lecture: Leon Bottou (Facebook/NYU)** [Slides](https://github.com/joanbruna/MathsDL-spring18/blob/master/lectures/bottou-02.06.2018.pdf)  |  [References](doc/refs.md#lec3)  |
| 4 | 2/13  | **Lec3** Scattering Transforms and CNNs [Slides](https://github.com/joanbruna/MathsDL-spring18/blob/master/lectures/lecture3.pdf) |  [References](doc/refs.md#lec3)  |
| 5 | 2/20  | **Lec4** Non-Euclidean Geometric Stability. Gromov-Hausdorff distances. Graph Neural Nets |  [References](doc/refs.md#lec3)  |
| 6 | 2/27  | **Lec5** Unsupervised Learning under Geometric Priors. Implicit vs Explicit models. Optimal Transport models. Microcanonical Models. Open Problems  |  [References](doc/refs.md#lec5)  |
| 7 | 3/6  | **Lec6** Stochastic Optimization. Convergence properties (or lack thereof).   |  [References](doc/refs.md#lec6)  |
| 8 | 3/13  | **Spring Break**  |  [References](doc/refs.md#lec8)  |
| 9 | 3/20  | **Lec7** Discrete vs Continuous Time Optimization. Fokker-Plank. Langevin Dynamics.  |  [References](doc/refs.md#lec7)  |
| 10 | 3/27  | **Lec8** Landscape of Deep Learning Optimization. Tensor factorization |  [References](doc/refs.md#lec8)  |
| 11 | 4/3  | **Lec9** Landscape of Deep Learning Optimization (cont'd). |  [References](doc/refs.md#lec9)  |
| 12 | 4/10  | **Lec10** Information Geometry. |  [References](doc/refs.md#lec10)  |
| 13 | 4/17  | **Lec11** Reproducing Kernel Hilbert Spaces |  [References](doc/refs.md#lec11)  |
| 14 | 4/24  | **Lec12** Optimal Transport in ML. Adversarial Training |  [References](doc/refs.md#lec12)  |
| 15 | 5/1  | **Lec13** Generalization. Review of Rademacher complexity. Stability. |  [References](doc/refs.md#lec13)  |



### Lab sessions / Parallel Curricula

## AlphaGoZero living document: https://goo.gl/iFZ4XD

* Class 4: MCTS & UCT
  * Motivation: Monte Carlo Tree Search (MCTS) forms the backbone of AlphaGoZero. It’s what lets it reliably explore and then hone in on the best policy. UCT (UCB for Trees) builds on top of what we’ve been learning and, paired with MCTS, is integral to the training process.
  * Required Reading:
    * [Sutton](http://incompleteideas.net/book/bookdraft2017nov5.pdf): Section 8.11
    * [Browne](https://gnunet.org/sites/default/files/Browne%20et%20al%20-%20A%20survey%20of%20MCTS%20methods.pdf): Sections 2.2, 2.4, 3.1-3.5, 8.2-8.4.
    * [Silver Thesis](http://papersdb.cs.ualberta.ca/~papersdb/uploaded_files/1029/paper_thesis.pdf): Sections 1.4.2 and 3.
  * Optional Reading:
    * [Jess Hamrick on Browne](http://jhamrick.github.io/quals/planning%20and%20decision%20making/2015/12/16/Browne2012.html).
    * [Original MCTS Paper](https://hal.archives-ouvertes.fr/file/index/docid/116992/filename/CG2006.pdf).
    * [Original UCT Paper](http://ggp.stanford.edu/readings/uct.pdf).
    * Browne: 
      * 4.8: MCTS applied to Stochastic or Imperfect Information Games.
      * 7.2, 7.3, 7.5, 7.7: Applications of MCTS.
  * Questions:
    * Can you detail each of the four parts of the MCTS algorithm?
    * What characteristics make MCTS a good choice?
    * What are examples of domain knowledge default policies in Go?
    * Why is UCT optimal? Can you prove that the failure probability at the root converges to zero at a polynomial rate in the number of games simulated?

* Class 3: Policy and Value Functions
  * Motivation: The Policy and Value Functions are at the core of Reinforcement Learning. The Policy function is the set of probabilities you give to each possible move. The Value function is your estimate of how good is the current state. In AlphaGoZero, a single network calculates both a value and a policy, then later updates its weights based off of the difference between those figures and the empirical results.
  * Required Reading (note: Sutton from here out refers to the [final version](http://incompleteideas.net/book/bookdraft2017nov5.pdf). Make sure it says COMPLETE DRAFT):
    * Value Function:
      * Sutton 3.5, 3.6, 3.7
      * Sutton: 9.1, 9.2, 9.3 (important!)
    * Policy Function:
      * Sutton: 4.1, 4.2, 4.3
      * Sutton: 13.1, 13.2 (important!), 13.3, 13.4
  * Optional Reading:
    * Sergey Levine: [Berkeley Fall'17: Policy Gradients](https://www.youtube.com/watch?v=tWNpiNzWuO8&feature=youtu.be) →  This is really good.
    * Sergey Levine: [Berkeley Fall'17: Value Functions](https://www.youtube.com/watch?v=k1vNh4rNYec&feature=youtu.be) → This is really good.
    * [Karpathy does Pong](http://karpathy.github.io/2016/05/31/rl/).
    * [David Silver on PG](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/pg.pdf).
    * [David Silver on Value](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/FA.pdf).
  * Questions:
    * Why does policy gradient have such high variance?
    * What is the difference between off-policy and on-policy?
    * Sutton:
      * 3.13: What is the Bellman equation for action values, that is, for qπ? ...
      * 3.14: In the gridworld example … are the signs of these rewards important, or only the intervals between them? Prove ...
      * 3.15: Now consider adding a constant c to all the rewards in an episodic task … would this have any effect, or would it leave the task unchanged as in the continuing task above? Why or why not? Give an example. 
      * 3.20: Give the Bellman equation for q∗ for the recycling robot. 
      * 4.3: What are the equations analogous to (4.3), (4.4), and (4.5) for the action-value function qπ and its successive approximation by a sequence of functions q0, q1, q2, . . . ? 
      * 4.6 (important!): How would policy iteration be defined for action values? Give a complete algorithm for computing q∗, analogous to that on page 65 for computing v∗. Please pay special attention to this exercise, because the ideas involved will be used throughout the rest of the book. 
      * 13.2 (important!): Prove (13.7) using the definitions and elementary calculus.
    
* Class 2: Multi-Armed Bandits and Upper Confidence Bounds
  * Motivation: Bandits and UCB are key components of how MCTS was originally formalized. The node selection during the search is achieved through the UCB approach, which is analogues to how its performed in a multi-armed bandit scenario.
  * Required Reading: 
    * Sutton: Sections 2.1 - 2.6 (Find on newclasses.nyu.edu in the class materials)
    * [Jeremy Kun: Optimizing in the Face of Uncertainty](https://jeremykun.com/2013/10/28/optimism-in-the-face-of-uncertainty-the-ucb1-algorithm/)
  * Optional Reading:
    * [Original UCB1 Paper](https://homes.di.unimi.it/~cesabian/Pubblicazioni/ml-02.pdf)
    * [UW Lecture Notes](https://courses.cs.washington.edu/courses/cse599s/14sp/scribes/lecture15/lecture15_draft.pdf)
  * Questions:
    * Sutton Exercises 2.1, 2.2, 2.4, 2.5
    * Sutton: What are the pros and cons of the optimistic initial values method?
    * Kun: In the proof for the expected cumulative regret of UCB1, why is delta(T) a trivial regret bound if the deltas are all the same?
    * Kun: Do you understand the argument for why the regret bound is O(sqrt(KTlog(T)))?
    * Can you reproduce the UCB1 algorithm?

* Class 1: Minimax and Alpha Beta Pruning
  * Motivation: These original core ideas did so much for the study of games. They spurred the field forward starting in the 50s and still to this day have mindshare in how to build a computer engine that beats games, including in popular chess engines like Stockfish.
  * Required Reading: 
    * [Cornell Recitation on Minimax & AB Pruning](https://www.cs.cornell.edu/courses/cs312/2002sp/lectures/rec21.htm)
    * [Knuth](https://pdfs.semanticscholar.org/dce2/6118156e5bc287bca2465a62e75af39c7e85.pdf): 6 (Theorems 1&2, Corollaries 1&3).
  * Optional Reading:
    * [CMU's MFAI Lecture 1](https://www.cs.cmu.edu/~arielpro/mfai_papers/lecture1.pdf).
    * Knuth: 1-3.    
    * [Chess Programming on Minimax](https://chessprogramming.wikispaces.com/Minimax)
    * [Chess Programming on AB Pruning](https://chessprogramming.wikispaces.com/Alpha-Beta)
  * Questions:
    * (Knuth) Show that AlphaBetaMin(p, alpha, beta) = -AlphaBetaMax(p, -beta, -alpha). (p. 300)
    * (Knuth) For Theorem 1.(1), why are the successor positions of type 2? (p. 305)
    * (Knuth) For Theorem 1.(2), why is it that p’s successor position is of type 3 if p is not terminal?
    * (Knuth) For Theorem 1.(3), why is it that p’s successor positions are of type 2 if p is not terminal?
    * (Knuth) Show that the subparts of Theorem 2, are correct.


