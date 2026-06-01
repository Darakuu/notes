# Game Theory Study Guide

## I. Core Concepts in Decision Theory

This section covers the foundational elements of individual decision-making under certainty, including preferences, utility functions, and their properties.

### A. Binary Relations and Preferences

- **Weak Preference ($\preceq$):** A fundamental binary relation in decision theory. $a \preceq b$ means "b is weakly preferred to a" (or "a is no better than b").
- **Reflexivity:** For any element $a$, $a \preceq a$. An item is always weakly preferred to itself.
- **Transitivity:** If $a \preceq b$ and $b \preceq c$, then $a \preceq c$. This ensures consistency in preferences.
- **Completeness:** For any pair $a, b$, either $a \preceq b$ or $b \preceq a$ (or both). This means all alternatives can be compared.
- **Strict Preference ($\prec$):** Derived from weak preference. $a \prec b$ if and only if $b \preceq a$ and it's not the case that $a \preceq b$. This implies $b$ is strictly preferred to $a$.
- **Asymmetry:** If $a \prec b$, then it's _not_ the case that $b \prec a$.
- **Transitivity:** If $a \prec b$ and $b \prec c$, then $a \prec c$.
- **Indifference ($\sim$):** Derived from weak preference. $a \sim b$ if and only if $a \preceq b$ and $b \preceq a$. This means an individual is equally satisfied with $a$ and $b$.
- **Equivalence Relation Properties:** Indifference is reflexive, symmetric, and transitive.
- **Reflexivity:** $a \sim a$.
- **Symmetry:** If $a \sim b$, then $b \sim a$.
- **Transitivity:** If $a \sim b$ and $b \sim c$, then $a \sim c$.
- **Antisymmetry:** A property of a binary relation $R$ where if $a R b$ and $b R a$, then $a=b$. The weak preference relation is antisymmetric if $a \preceq b$ and $b \preceq a$ imply $a=b$.
- **Decision Problem:** A pair $(A, \preceq)$, where $A$ is a set of alternatives and $\preceq$ is a weak preference relation on $A$.

### B. Utility Functions

- **Definition:** A function $u: A \to \mathbb{R}$ that represents a weak preference relation $\preceq$ if, for each pair $a, b \in A$, $a \preceq b$ if and only if $u(a) \geq u(b)$.
- **Equivalences:**$a \prec b \iff u(a) > u(b)$
- $a \sim b \iff u(a) = u(b)$
- **Existence of Utility Functions:Order Dense Set:** A set $B \subset A$ is order dense in $A$ if, for each pair $a_1, a_2 \in A$ with $a_2 \prec a_1$, there is $b \in B$ such that $a_2 \preceq b \preceq a_1$.
- **Gap:** A pair $(a_1, a_2)$ with $a_2 \prec a_1$ is a gap if, for each $b \in A$, either $b \preceq a_2$ or $a_1 \preceq b$. $a_1$ and $a_2$ are gap extremes.
- **Theorem 1.2.3 (Existence Condition for Antisymmetric Preferences):** If $(A, \preceq)$ is a decision problem where $\preceq$ is antisymmetric, then $\preceq$ can be represented by a utility function if and only if there is a countable set $B \subset A$ that is order dense in $A$.
- **Lexicographic Order (Example 1.2.2):** An example of a preference relation that cannot be represented by a utility function. It implies an "infinite" preference for the first differing component, which cannot be captured by real numbers.

### C. Linear Utility

- **Convex Decision Problem:** A decision problem $(X, \preceq)$ where $X$ is a convex subset of a finite dimensional real vector space.
- **Linear Utility Function:** A function $\bar{u}: X \to \mathbb{R}$ representing $\preceq$ such that it satisfies two conditions:
- $\bar{u}$ represents $\preceq$ (i.e., $x \preceq y \iff \bar{u}(x) \geq \bar{u}(y)$).
- For each $t \in [0, 1]$, $\bar{u}(tx + (1-t)y) = t\bar{u}(x) + (1-t)\bar{u}(y)$ (linearity/convexity property).
- **Properties of Preferences for Linear Utility:Independence:** For each triple $x, y, z \in X$ and $t \in (0, 1]$, $x \preceq y$ if and only if $tx + (1-t)z \preceq ty + (1-t)z$. This means preferences over mixtures are independent of the common component $z$.
- **Continuity:** For each triple $x, y, z \in X$ such that $x \prec y \prec z$, there is $t \in (0, 1)$ with $y \sim tx + (1-t)z$. This ensures no "jumps" in preferences.
- **Uniqueness of Linear Utility Functions:** If $\bar{u}$ is a linear utility function representing $\preceq$, then any other linear utility function $\hat{u}$ representing $\preceq$ is a positive affine transformation of $\bar{u}$ (i.e., $\hat{u}(x) = a\bar{u}(x) + b$ for $a > 0$).

## II. Strategic Games

This section focuses on games where players choose actions simultaneously, considering the actions of others.

### A. Basic Definitions

- **Strategic Game (Normal Form Game):** A tuple $(N, {A_i}_{i \in N}, {u_i}_{i \in N})$, where:
- $N$: Set of players.
- $A_i$: Set of actions (or strategies) for player $i$. $A = \prod_{i \in N} A_i$ is the set of action profiles.
- $u_i$: Payoff function for player $i$, mapping action profiles to real numbers ($u_i: A \to \mathbb{R}$).
- **Action Profile Notation:** $(a'_i, a_{-i})$ denotes an action profile where player $i$ chooses $a'_i$ and all other players $j \neq i$ choose their actions $a_j$ as specified in the original profile $a$.
- **Best Reply (Best Response):** For a given action profile $a_{-i}$ of other players, player $i$'s best reply $a'_i$ is an action that maximizes $u_i(a'i, a{-i})$. $BR_i(a_{-i}) := { \hat{a}_i : \forall \tilde{a}_i \in A_i, u_i(a_{-i}, \hat{a}_i) \geq u_i(a_{-i}, \tilde{a}_i) }$.
- **Dominance:Strictly Dominated Strategy:** A strategy $a_i$ is strictly dominated if there exists another strategy $a'_i$ such that $u_i(a'i, a{-i}) > u_i(a_i, a_{-i})$ for all $a_{-i} \in A_{-i}$. A rational player will never play a strictly dominated strategy.
- **Weakly Dominated Strategy:** A strategy $a_i$ is weakly dominated if there exists another strategy $a'_i$ such that $u_i(a'i, a{-i}) \geq u_i(a_i, a_{-i})$ for all $a_{-i} \in A_{-i}$, and $u_i(a'_i, a_{-i}) > u_i(a_i, a_{-i})$ for at least one $a_{-i} \in A_{-i}$.
- **Iterated Elimination of Strictly Dominated Strategies (IESDS):** A process of successively removing strictly dominated strategies from a game. If a game has a unique strategy profile that survives IESDS, it is often considered a strong prediction of behavior.

### B. Nash Equilibrium (NE)

- **Definition:** An action profile $a^* = (a^*_1, \dots, a^*_n)$ is a Nash Equilibrium if, for each player $i$, $a^*_i$ is a best reply to $a^*_{-i}$. That is, no player can unilaterally improve their payoff by changing their strategy, given the strategies of the other players.
- $u_i(a^*_i, a^*_{-i}) \geq u_i(a_i, a^*_{-i})$ for all $a_i \in A_i$ and all $i \in N$.
- **Existence of Nash Equilibrium:** Every finite game has at least one Nash Equilibrium in mixed strategies. (This requires a move to mixed strategies).
- **Cournot Equilibrium (Example):** A Nash equilibrium in a Cournot duopoly or oligopoly model, where firms choose quantities to maximize profit, given the quantities chosen by competitors. The unique Nash equilibrium for two duopolists is $( \frac{d-c}{3}, \frac{d-c}{3} )$.

### C. Mixed Strategies and Expected Payoffs

- **Mixed Strategy:** A probability distribution over a player's pure strategies. A mixed strategy for player $i$ is denoted by $s_i \in \Delta(A_i)$, where $\Delta(A_i)$ is the set of all probability distributions over $A_i$.
- **Expected Payoff:** Given a mixed strategy profile $s = (s_1, \dots, s_n)$, the expected payoff for player $i$ is $U_i(s) = \sum_{a \in A} (\prod_{j \in N} s_j(a_j)) u_i(a)$.
- **Nash Equilibrium in Mixed Strategies:** A mixed strategy profile $s^_$ is a Nash equilibrium if, for each player $i$, $U_i(s^i, s^*_{-i}) \geq U_i(s_i, s^*_{-i})$ for all $s_i \in \Delta(A_i)$.
- A player's mixed strategy is a best response if and only if every pure strategy assigned a positive probability in the mixed strategy is a best response to the other players' strategies.
- **Minimax Theorem (Matrix Games):** For any two-player zero-sum game, the value of the game for player 1 (maximin payoff) is equal to the value of the game for player 2 (minimax payoff). This implies the existence of a Nash equilibrium in mixed strategies.

### D. Refinements of Nash Equilibrium

- **Perfect Equilibrium (in finite games):** A Nash equilibrium $s$ of a finite game $G$ is perfect if there exist sequences ${\eta^k} \to 0$ and ${s^k} \to s$ such that for each $k$, $s^k$ is a Nash equilibrium of $(G, \eta^k)$, where $(G, \eta^k)$ is a perturbed game. In a perturbed game, every pure strategy must be played with at least a small positive probability $\eta_i^k(a_i)$. Perfect equilibria rule out equilibria that rely on "unreasonable" threats (i.e., weakly dominated strategies).
- Equivalently, a Nash equilibrium $s$ is perfect if and only if for every pure strategy $a_i$ that is played with positive probability in $s_i$, $a_i$ is a best reply to $s_{-i}$ and also a best reply to all strategies $s_{-i}$ "close" to $s_{-i}$ (where "close" means that strategies used with probability 0 in $s_{-i}$ might be used with small positive probability).

### E. Correlated Equilibrium

- **Definition:** A correlated equilibrium for a game $G$ is a pair $(I, \tau^*)$, where $I = (\Omega, \rho, {P_i}_{i \in N})$ is an information structure and $\tau^*$ is an $I$-consistent correlated strategy. It implies that players receive private signals from a common random variable, and their chosen actions are optimal given their signal and the belief that other players are also acting optimally according to their signals.
- **Relation to Nash Equilibrium:** Every (pure) Nash equilibrium induces a correlated equilibrium. Correlated equilibria can yield higher payoffs for all players than any Nash equilibrium (e.g., in the Battle of the Sexes).

## III. Extensive Games

This section explores games where players make choices sequentially over time, represented by a game tree.

### A. Basic Definitions

- **Extensive Game:** A game defined by a game tree, specifying:
- **Players:** Set of players $N$.
- **Terminal Histories:** Sequences of actions that end the game, leading to payoffs.
- **Player Function:** Maps non-terminal histories to the player whose turn it is.
- **Action Sets:** Set of actions available to a player at each non-terminal history.
- **Payoff Functions:** Assigns a payoff to each player for each terminal history.
- **Information Set:** A set of decision nodes for a player such that the player cannot distinguish between any two nodes in the set. This is crucial for games with imperfect information.
- **Perfect Information:** Each information set contains exactly one node.
- **Imperfect Information:** At least one information set contains more than one node.
- **Strategy in Extensive Games:** A complete plan of action that specifies a player's choice at every information set where they are active, even those not reached in play.
- **Subgame:** A part of an extensive game that starts at a single node (the root of the subgame), contains all subsequent nodes and branches, and is itself an extensive game.

### B. Solution Concepts

- **Nash Equilibrium in Extensive Games:** The definition of Nash equilibrium still applies, but considering strategies as complete plans of action. However, NE might include "non-credible threats" in extensive games.
- **Subgame Perfect Equilibrium (SPE):** A strategy profile is a subgame perfect equilibrium if it induces a Nash equilibrium in every subgame of the original game. SPE eliminates non-credible threats.
- **Backward Induction:** The primary method for finding SPE in finite games with perfect information. It involves starting at the terminal nodes and working backward, determining optimal actions at each decision node.

### C. Repeated Games

- **Infinitely Repeated Games:** A base game (stage game) is played infinitely many times. Payoffs are typically discounted sums of stage game payoffs.
- **Finite Repeated Games:** The stage game is played a fixed number of times.
- **Backward Induction:** In finite repeated games with unique Nash equilibria in the stage game, backward induction implies that the unique SPE involves playing the stage game NE in every period.
- **Strategies in Repeated Games:** Strategies are functions mapping histories (sequences of past actions) to actions.
- **Grim Trigger Strategy:** A common strategy in repeated games where players cooperate as long as everyone cooperates, but if any player deviates, all players revert to a Nash equilibrium of the stage game forever.
- **Folk Theorems:** A class of theorems that state that in infinitely repeated games (or sufficiently long finitely repeated games), any individually rational and feasible payoff profile can be sustained as a Nash equilibrium (or subgame perfect equilibrium) for sufficiently high discount factors.
- **Individually Rational Payoff:** A payoff for a player that is at least their minimax payoff.
- **Feasible Payoff:** A payoff that can be achieved by some combination of actions in the stage game.

## IV. Games with Incomplete Information (Bayesian Games)

This section deals with games where players have private information about certain aspects of the game, such as their own payoffs or types.

### A. Basic Definitions

- **Incomplete Information:** Occurs when at least one player does not know some relevant information about the game, such as other players' payoff functions or types.
- **Type:** A player's private information, often drawn from a set of possible types ($\Theta_i$). Each type corresponds to a different payoff function or characteristic for that player.
- **Prior Beliefs:** Common knowledge probability distribution over the possible types of all players.
- **Signals:** Information received by players that helps them update their beliefs about other players' types.
- **Bayesian Game:** A strategic game where players have types, beliefs about other players' types, and their payoffs depend on the action profile and the type profile.
- A Bayesian game is characterized by:
- The set of players $N$.
- A set of actions $A_i$ for each player $i$.
- A set of types $\Theta_i$ for each player $i$.
- A payoff function $u_i(a, \theta)$ for each player $i$, where $a$ is the action profile and $\theta$ is the type profile $(\theta_1, \dots, \theta_n)$.
- A prior probability distribution $p(\theta)$ over the type profiles.
- **Strategy in a Bayesian Game:** A function $\hat{a}_i: \Theta_i \to A_i$ that specifies an action for each of player $i$'s possible types.

### B. Bayesian Nash Equilibrium (BNE)

- **Definition:** A strategy profile $(\hat{a}^*_1, \dots, \hat{a}^*_n)$ is a Bayesian Nash Equilibrium if for each player $i$ and each type $\theta_i \in \Theta_i$, $\hat{a}^*i(\theta_i)$ maximizes player $i$'s expected payoff, given $\hat{a}^*{-i}$ and player $i$'s beliefs about $\theta_{-i}$.
- Expected payoff for player $i$ with type $\theta_i$ choosing $a_i$: $E_{\theta_{-i} | \theta_i} [u_i(a_i, \hat{a}^*_{-i}(\theta_{-i}), \theta_i, \theta_{-i})]$.
- **Juries Example (Illustration):** A Bayesian game where jurors have private signals (types) about a defendant's guilt and must decide to convict or acquit. BNE involves jurors voting optimally based on their signal and the probability of guilt, considering others' optimal voting strategies.

## V. Cooperative Games

This section shifts focus to situations where players can form coalitions and jointly commit to strategies to achieve common goals, with an emphasis on how gains are distributed among players.

### A. Coalitional Games (TU-Games)

- **Transferable Utility (TU) Game:** A pair $(N, v)$, where $N$ is the set of players and $v: 2^N \to \mathbb{R}$ is the characteristic function.
- **Characteristic Function ($v(S)$):** Represents the maximum total payoff that a coalition $S \subseteq N$ can guarantee for its members, regardless of the actions of players outside $S$.
- $v(\emptyset) = 0$.
- **Nontransferable Utility (NTU) Game:** A pair $(N, V)$, where $V(S)$ is a set of feasible payoff vectors for coalition $S$. Utility cannot be freely transferred between players.
- **Properties of $V(S)$:** Nonempty, closed, comprehensive, $V({i}) \ne \mathbb{R}$, and $V(S) \cap {y \in \mathbb{R}^S : \forall i \in S, y_i \ge v_i}$ is bounded.
- **Allocation:** A vector $x \in \mathbb{R}^N$ representing the payoffs to each player.
- **Feasible Allocation:** An allocation $x$ is feasible if there's a partition of $N$ into coalitions ${S_1, \dots, S_k}$ such that for each $S_l$, there exists a payoff vector $y \in V(S_l)$ where $y_i = x_i$ for all $i \in S_l$.
- **Imputation:** A feasible allocation $x \in \mathbb{R}^N$ that satisfies:
- **Individual Rationality:** For each player $i \in N$, $x_i \geq v({i})$. (No player gets less than what they can guarantee alone).
- **Group Rationality (Efficiency):** $\sum_{i \in N} x_i = v(N)$. (The grand coalition's total payoff is distributed).
- The set of all imputations is denoted $I(v)$.

### B. Solution Concepts for TU-Games

- **The Core ($C(v)$):** The set of imputations that cannot be blocked by any coalition. An imputation $x$ is in the core if for every coalition $S \subseteq N$, $\sum_{i \in S} x_i \geq v(S)$.
- **Properties:** A core allocation is undominated (no coalition can achieve more for all its members than they get in the core allocation). If the game is superadditive, the core equals the set of undominated imputations.
- **Existence:** The core may be empty.
- **The Shapley Value ($\Phi(v)$):** A unique allocation rule that assigns a payoff to each player based on their marginal contributions to all possible coalitions. It is derived from a set of axioms:
- **Efficiency (EFF):** Sum of players' Shapley values equals $v(N)$.
- **Symmetry (SYM):** Symmetric players (interchangeable roles) get the same payoff.
- **Null Player Property (NPP):** Null players (contribute nothing to any coalition) get 0.
- **Additivity (ADD):** The Shapley value of a sum of games is the sum of their Shapley values.
- **Formula:** $\Phi_i(v) = \sum_{S \subseteq N \setminus {i}} \frac{|S|!(n-|S|-1)!}{n!} [v(S \cup {i}) - v(S)]$.
- **The Nucleolus ($\eta(v)$):** A unique imputation that minimizes the maximum "excess" of any coalition, lexicographically. The excess of a coalition $S$ for a given imputation $x$ is $e(S, x) = v(S) - \sum_{i \in S} x_i$. It measures how much a coalition is "short-changed" by an imputation.
- **Existence and Uniqueness:** The nucleolus is always non-empty and contains a unique allocation if the set of imputations is non-empty.
- **Lexicographic Order:** Used to compare excess vectors. A vector $\theta(y)$ is lexicographically smaller than $\theta(x)$ if at the first component where they differ, $\theta(y)$ has a smaller value.
- **The Nash Bargaining Solution (NBS):** A solution concept for 2-player cooperative games with NTU, where players agree on a feasible payoff vector that maximizes the product of their utility gains from a disagreement point.
- **Axioms:** Efficiency (Pareto optimality), Symmetry, Independence of Irrelevant Alternatives (IIA), and Scale Invariance (or Covariance with affine transformations).
- **Negotiation Game ($G_{NA}$):** A non-cooperative game where players propose demands, and if the demands are feasible, they get their demands; otherwise, they get the disagreement point. The Nash bargaining solution can be seen as a unique B-essential equilibrium of this negotiation game.

## VI. Advanced Topics

### A. Sperner's Lemma and Fixed Point Theorems

- **Simplex:** A generalization of a triangle (2-simplex) or tetrahedron (3-simplex) to higher dimensions.
- **Dissection of a Simplex:** A collection of smaller simplices that partition the original simplex.
- **Sperner Labeling:** A labeling of the vertices of a dissection of a k-simplex such that vertices on a face of the original simplex are labeled with an extreme point of that face.
- **Sperner's Lemma:** States that for any Sperner labeling of a dissection of a k-simplex, there must be at least one "completely labeled" simplex (a simplex whose vertices have all the labels of the original simplex's extreme points).
- **Brouwer Fixed-Point Theorem:** A continuous function from a convex, compact subset of a Euclidean space to itself must have at least one fixed point (a point $x$ such that $f(x) = x$). Sperner's Lemma is often used in proofs of fixed-point theorems, which are fundamental to proving the existence of Nash equilibria.

### B. Separating Hyperplane Theorems

- **Hyperplane:** A generalization of a line (in 2D) or a plane (in 3D) to higher dimensions. It divides a space into two half-spaces.
- **Supporting Hyperplane:** A hyperplane that touches the boundary of a convex set and separates the set from its interior.
- **Separating Hyperplane:** A hyperplane that separates two disjoint sets.
- **Theorem 2.14.3 (Separating Hyperplane Theorem):** If S and $\hat{S}$ are two disjoint, nonempty, and convex subsets of $\mathbb{R}^n$, then there is a separating hyperplane for S and $\hat{S}$. These theorems are crucial for proving results in convex analysis and game theory, particularly in cooperative game theory and general equilibrium theory.

## Quiz

**Instructions:** Answer each question in 2-3 sentences.

1. Explain the relationship between weak preference ($\preceq$), strict preference ($\prec$), and indifference ($\sim$).
2. What is a utility function in decision theory, and what is its primary purpose?
3. Why can't the lexicographic order be represented by a utility function?
4. Define what makes a utility function "linear" in the context of a convex decision problem.
5. What is a Nash Equilibrium in a strategic game?
6. How does a perfect equilibrium refine the concept of a Nash equilibrium in finite games?
7. What is the main difference between a strategic game and an extensive game in terms of how choices are made?
8. Briefly describe the concept of backward induction and its application in extensive games.
9. What is a Bayesian Nash Equilibrium, and how does it account for incomplete information?
10. Define the Core of a cooperative game. What does it mean for an imputation to be in the Core?

## Answer Key

1. Weak preference $a \preceq b$ means "b is weakly preferred to a." Strict preference $a \prec b$ means $a \preceq b$ and it's not the case that $b \preceq a$. Indifference $a \sim b$ means both $a \preceq b$ and $b \preceq a$. These three relations are derived from the fundamental weak preference.
2. A utility function is a real-valued function that assigns numerical values to alternatives, reflecting an individual's preferences. Its primary purpose is to provide a numerical representation of an agent's ranking of alternatives, where higher values correspond to more preferred alternatives.
3. The lexicographic order cannot be represented by a utility function because it implies an "infinite" preference for the first differing component, which cannot be captured by real numbers. No real number can be "infinitely" larger than another to represent such a strict ordering at the first point of difference, regardless of subsequent components.
4. A utility function is "linear" in a convex decision problem if it represents the preferences (i.e., $x \preceq y \iff \bar{u}(x) \geq \bar{u}(y)$) and also satisfies linearity with respect to mixtures: $\bar{u}(tx + (1-t)y) = t\bar{u}(x) + (1-t)\bar{u}(y)$ for $t \in [0,1]$. This implies that the utility of a combination of alternatives is the weighted average of the utilities of those alternatives.
5. A Nash Equilibrium is an action profile where no player can unilaterally improve their payoff by changing their strategy, given the strategies of all other players. In essence, it's a stable state where each player's chosen action is their best response to the actions chosen by the others.
6. A perfect equilibrium refines Nash equilibrium by requiring that the equilibrium strategies remain optimal even in subgames that would not be reached if players adhere to the equilibrium path. It eliminates Nash equilibria that rely on "non-credible threats" – strategies that are not optimal for a player to carry out if they were ever called upon to do so.
7. In a strategic game, players choose their actions simultaneously without knowledge of the other players' choices. In contrast, an extensive game models sequential decision-making, where players choose actions over time, potentially with knowledge of previous actions, and the game progresses through a series of stages or nodes.
8. Backward induction is a method used to find subgame perfect equilibria in finite extensive games with perfect information. It involves starting from the end of the game (terminal nodes) and working backward, determining the optimal action for each player at every decision node by considering the subsequent optimal play.
9. A Bayesian Nash Equilibrium is a strategy profile in a Bayesian game where each player's strategy (a function mapping types to actions) maximizes their _expected_ payoff, given their own type and their beliefs about the other players' types and strategies. It accounts for incomplete information by incorporating players' probabilistic beliefs about private information into their decision-making.
10. The Core of a cooperative game is the set of all imputations (feasible and individually rational payoff distributions) that cannot be "blocked" by any coalition. For an imputation to be in the Core, no group of players, by forming a coalition, can achieve a higher total payoff for all its members than what they receive in that imputation.

## Essay Format Questions

1. Discuss the importance of the continuity and independence properties of preferences for the existence and uniqueness (up to affine transformations) of linear utility functions in convex decision problems. Use examples or counter-examples to illustrate cases where these properties might fail and their implications.
2. Compare and contrast Nash Equilibrium, Perfect Equilibrium, and Correlated Equilibrium. Explain how each concept addresses limitations of the previous one, providing specific examples (e.g., Battle of the Sexes, Prisoner's Dilemma) to illustrate their differences and applications.
3. Analyze the role of fixed-point theorems (like Brouwer's) and Sperner's Lemma in proving the existence of Nash equilibria in game theory. Explain the theoretical connection between these mathematical tools and the game-theoretic concept of equilibrium.
4. Explain the concept of "non-credible threats" in extensive games and how the Subgame Perfect Equilibrium (SPE) refinement addresses this issue. Provide a detailed example of an extensive game where a Nash Equilibrium is not subgame perfect, clearly demonstrating why.
5. Critically evaluate the different solution concepts for cooperative games discussed (Core, Shapley Value, Nucleolus, Nash Bargaining Solution). Discuss their axiomatic foundations, their strengths and weaknesses, and in what types of scenarios each might be most appropriate or insightful.

## Glossary of Key Terms

- **Action Profile ($a$):** A list of actions chosen by all players in a game, one for each player.
- **Additivity (ADD):** An axiom for allocation rules, stating that the value assigned to a game constructed by summing two original games is the sum of the values assigned to the original games.
- **Allocation ($x$):** A vector in $\mathbb{R}^N$ representing the payoffs to each player in a cooperative game.
- **Antisymmetric Relation:** A binary relation $R$ where if $a R b$ and $b R a$, then $a=b$.
- **Asymmetric Relation:** A binary relation $R$ where if $a R b$, then it's not the case that $b R a$.
- **Backward Induction:** A method for finding Subgame Perfect Equilibria in extensive games by working backward from the end of the game.
- **Bayesian Game:** A strategic game where players have private information (types) and beliefs about other players' types, and payoffs depend on actions and types.
- **Bayesian Nash Equilibrium (BNE):** A strategy profile in a Bayesian game where each player's strategy (a function mapping types to actions) maximizes their expected payoff, given their type and beliefs about others.
- **Best Reply (Best Response) ($BR_i(a_{-i})$):** An action that maximizes a player's payoff, given the actions of other players.
- **Binary Relation ($R$):** A property of a set $A$ that relates elements of $A$ in pairs (e.g., $a \preceq b$).
- **Brouwer Fixed-Point Theorem:** A mathematical theorem stating that any continuous function from a compact, convex set to itself has at least one fixed point. Used to prove existence of Nash equilibria.
- **Characteristic Function ($v(S)$):** In a TU-game, a function that assigns to each coalition $S$ the maximum payoff its members can guarantee.
- **Coalition ($S$):** A subset of players in a cooperative game who can coordinate their actions.
- **Completeness (of Preference Relation):** For any two alternatives $a, b$, either $a \preceq b$ or $b \preceq a$ (or both).
- **Continuity (of Preferences):** A property of preferences ensuring that if $x \prec y \prec z$, there is a mixture of $x$ and $z$ that is indifferent to $y$. Important for linear utility.
- **Convex Decision Problem:** A decision problem $(X, \preceq)$ where the set of alternatives $X$ is a convex subset of a real vector space.
- **Core ($C(v)$):** The set of imputations in a cooperative game that cannot be blocked by any coalition.
- **Correlated Equilibrium:** A solution concept where players receive signals from a common random variable and choose actions optimally, given their signals and beliefs about others.
- **Cournot Equilibrium:** A Nash equilibrium in a Cournot oligopoly model, where firms compete by choosing quantities.
- **Decision Problem ($(A, \preceq)$):** A set of alternatives $A$ coupled with a weak preference relation $\preceq$ on $A$.
- **Disagreement Point:** In bargaining theory, the outcome if players fail to reach an agreement.
- **Dominance (Strictly/Weakly):** A strategy is dominated if another strategy always yields a (strictly) better or equal payoff, and sometimes a strictly better payoff, regardless of other players' actions.
- **Efficiency (EFF):** An axiom for allocation rules, stating that the sum of the allocated payoffs equals the total value generated by the grand coalition.
- **Equivalence Relation:** A binary relation that is reflexive, symmetric, and transitive (e.g., indifference).
- **Excess ($e(S,x)$):** In a cooperative game, for a given imputation $x$, the difference between a coalition's value $v(S)$ and the sum of payoffs its members receive in $x$.
- **Expected Payoff:** The average payoff for a player in a game involving mixed strategies or uncertainty, weighted by probabilities.
- **Extensive Game:** A game represented by a tree, specifying sequential moves, information sets, and payoffs.
- **Feasible Allocation:** In an NTU-game, an allocation that can be achieved by partitioning players into coalitions and distributing their values.
- **Finite Repeated Games:** Games where a base game is played a fixed number of times.
- **Folk Theorems:** A class of theorems in repeated games that state that a wide range of payoff profiles can be sustained as equilibria if players are sufficiently patient.
- **Gap:** A pair of alternatives $(a_1, a_2)$ with $a_2 \prec a_1$ such that no other alternative lies strictly between them in terms of preference.
- **Grim Trigger Strategy:** A strategy in repeated games where players cooperate as long as everyone cooperates, but permanently revert to a non-cooperative action if any player deviates.
- **Hyperplane:** A geometric concept dividing a space into two half-spaces; a generalization of a line or plane.
- **Imperfect Information:** In an extensive game, when a player cannot distinguish between different nodes in an information set.
- **Imputation ($x$):** A feasible allocation in a cooperative game that satisfies individual rationality and group rationality (efficiency).
- **Independence (of Preferences):** A property of preferences stating that preferences over mixtures are independent of a common component. Important for linear utility.
- **Indifference ($\sim$):** A binary relation where a decision-maker is equally satisfied with two alternatives ($a \sim b \iff a \preceq b \text{ and } b \preceq a$).
- **Individual Rationality:** A condition for an allocation where each player receives at least what they could obtain by acting alone.
- **Infinitely Repeated Games:** Games where a base game is played an infinite number of times, typically with discounted payoffs.
- **Information Set:** A set of decision nodes for a player in an extensive game where the player cannot distinguish between any two nodes.
- **Iterated Elimination of Strictly Dominated Strategies (IESDS):** A process of successively removing strictly dominated strategies to simplify a game.
- **Lexicographic Order:** A strict ordering of vectors where the first differing component determines the order (e.g., $(2,3,1)$ is preferred to $(1,100,5)$).
- **Linear Utility Function ($\bar{u}$):** A utility function for convex decision problems that also satisfies a linearity property for mixtures.
- **Minimax Theorem:** For two-player zero-sum games, the value of the game for player 1 (maximin payoff) equals the value of the game for player 2 (minimax payoff).
- **Mixed Strategy ($s_i$):** A probability distribution over a player's pure strategies.
- **Nash Bargaining Solution (NBS):** A solution for 2-player cooperative games (often NTU) that maximizes the product of players' utility gains from a disagreement point.
- **Nash Equilibrium (NE):** An action profile where no player can unilaterally improve their payoff by changing their strategy, given the others' strategies.
- **Negotiation Game ($G_{NA}$):** A non-cooperative game where players propose demands to reach a cooperative outcome.
- **Nucleolus ($\eta(v)$):** A unique imputation in a cooperative game that minimizes the maximum excess of any coalition, lexicographically.
- **Null Player:** In a cooperative game, a player whose marginal contribution to any coalition is zero.
- **Null Player Property (NPP):** An axiom for allocation rules, stating that null players receive a payoff of zero.
- **Order Dense Set:** A set $B \subset A$ is order dense in $A$ if, for any two alternatives $a_1, a_2$ where $a_2 \prec a_1$, there is an alternative $b \in B$ such that $a_2 \preceq b \preceq a_1$.
- **Perfect Equilibrium:** A refinement of Nash equilibrium that requires strategies to be optimal even in perturbed versions of the game (or in subgames that are not reached).
- **Perfect Information:** In an extensive game, when each information set contains exactly one node (players know all previous moves).
- **Player Function:** In an extensive game, a function that specifies which player moves at each non-terminal history.
- **Prior Beliefs:** A probability distribution over the possible types of players, common knowledge among all players.
- **Reflexivity:** A property of a binary relation $R$ where $a R a$ for all $a$.
- **Separating Hyperplane Theorem:** A theorem stating that two disjoint, nonempty, convex sets in Euclidean space can be separated by a hyperplane.
- **Shapley Value ($\Phi(v)$):** A unique allocation rule for TU-games that distributes total payoffs based on players' average marginal contributions to all possible coalitions.
- **Simplex:** A generalization of a triangle or tetrahedron to higher dimensions.
- **Sperner Labeling:** A specific type of labeling for the vertices of a dissection of a simplex.
- **Sperner's Lemma:** States that any Sperner-labeled dissection of a simplex must contain at least one "completely labeled" sub-simplex.
- **Strict Preference ($\prec$):** A binary relation where one alternative is strictly preferred to another ($a \prec b \iff b \preceq a \text{ and not } a \sim b$).
- **Strategic Game (Normal Form Game):** A game defined by a set of players, actions for each player, and payoff functions that depend on the chosen action profile.
- **Strategy (in Extensive Games):** A complete plan of action for a player, specifying their move at every information set.
- **Subgame:** A part of an extensive game that starts at a single node and is itself an extensive game.
- **Subgame Perfect Equilibrium (SPE):** A strategy profile that constitutes a Nash Equilibrium in every subgame of the original game.
- **Supporting Hyperplane:** A hyperplane that touches the boundary of a convex set and separates the set from its interior.
- **Symmetry (SYM):** An axiom for allocation rules, stating that players with identical roles (interchangeable positions) receive the same payoff.
- **Terminal Histories:** Sequences of actions in an extensive game that end the game, leading to payoffs.
- **Transitivity:** A property of a binary relation $R$ where if $a R b$ and $b R c$, then $a R c$.
- **Transferable Utility (TU) Game:** A cooperative game where utility can be freely transferred among players (e.g., monetary payoffs).
- **Type ($\Theta_i$):** A player's private information in a Bayesian game, affecting their payoffs or beliefs.
- **Utility Function ($u$):** A function that assigns numerical values to alternatives, reflecting a decision-maker's preferences.
- **Weak Preference ($\preceq$):** A binary relation where one alternative is weakly preferred to another ($a \preceq b$ means "b is at least as good as a").
- **Weakly Dominated Strategy:** A strategy that is never strictly better than another, and sometimes worse, for all opponents' actions.