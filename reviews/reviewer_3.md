	This paper studies verification of nonlinear neural
feedback systems with a fixed neural-network controller.
The proposed method, FABRIC, combines forward reachability
from the initial set with backward reachable-set
computation from the goal or unsafe set, followed by
containment or disjointness checks to certify reach and
avoid properties. The backward component adapts DRIP-style
domain refinement to nonlinear dynamics using polyhedral
enclosures, computes outer approximations of may-reachable
backward sets, and introduces practical methods for
constructing certified inner approximations of
must-reachable backward sets. The main contribution is best
understood as a practical bidirectional verification
pipeline for closed-loop neural systems with nonlinear
dynamics, rather than a new controller-synthesis or general
reachability framework.

Strengths:
- May/must BRSs well laid out
- Polyhedral enclosures for nonlinear dynamics for backward
domain refinement shows the authors can take existing work
and extend it
- Full comparison against baselines, and unicycle
highlights strengths of backward computation

Main weaknesses:
- Paper lays out poorly what is novel and what is inherited
/ adapted from prior (own and community) work
- No sensitivity analysis on chosen hyperparameters + no
clear explanation on why only 6% backwards & mostly forward
is much better than 100% forward
Technical clarity issues:
- Equation 7 should be arbitrary k (not just 2) as it seems
like the methods use arbitrary k
- M0, ..., Mn listed as vague constraints, not very
mathematically rigorous


Minor issues:
- Table 3 has no metrics defined for them.
- Dynamics need to be defined more explicitlym as we assume
its a control that is fully additive
- I find that in the introduction the work doesn't fully
lay out where backward and forward work well and how they
are complementary 