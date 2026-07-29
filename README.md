# Near-Optimal Online Recalibration for Log Loss

## Abstract

Online recalibration replaces an arbitrary forecast sequence by predictions that are calibrated and nearly as accurate. Recent work attains the optimal $T=\Theta(\varepsilon^{-3})$ horizon for globally Lipschitz proper losses, but logarithmic loss is unbounded at probabilities zero and one. Naive clipping makes the existing bound polynomially worse. We give the first near-optimal recalibration guarantee for Bernoulli log loss without any restriction on the input forecasts. Our algorithm achieves expected ordinary $\ell_1$ calibration at most $\varepsilon$ and expected excess log loss at most $\varepsilon^2$ after $O(\varepsilon^{-3}\log(1/\varepsilon))$ rounds. A matching $\Omega(\varepsilon^{-3})$ lower bound leaves only one logarithmic factor. The key is a nonuniform mixture oracle controlled by adjacent KL tangent gaps, rather than by a global Lipschitz constant. A grid uniform in the Bernoulli information coordinate $\arcsin\sqrt p$ has $O(\varepsilon^{-1})$ points, probability mesh $O(\varepsilon)$, and labelwise tangent gap $O(\varepsilon^2)$ even at the boundary. Normalizing the loss objective and initializing the imbalanced meta learner at that objective prevents the growing clipped loss range from being paid twice. Experiments on controlled streams and a shifted CIFAR-10 binary stream evaluate the finite-time calibration and loss frontier. A fixed practical step choice reduces exact calibration error by $92.8\%$ on the shifted image stream while improving log loss. The result closes the unbounded-log-loss gap for arbitrary-hint online recalibration while making explicit which information-geometric ingredients are inherited from earlier log-loss discretization.

## Main results

**Theorem.** There are universal constants $C,c>0$ such that the following holds. For any $\varepsilon\in(0,c)$, any horizon \begin{equation} T\geq C\frac{\log(1/\varepsilon)}{\varepsilon^3}, \end{equation} and every non-anticipating hint-label sequence, \method produces predictions satisfying Equations~(\ref{eq:target-cal}) and (\ref{eq:target-loss}).

**Theorem.** For all sufficiently small $\varepsilon$, any online learner that guarantees expected $O(\varepsilon)$ ordinary $\ell_1$ calibration and expected $O(\varepsilon^2)$ excess Bernoulli log loss on every sequence requires \begin{equation} T=\Omega(\varepsilon^{-3}). \end{equation} This holds even when every hint lies in $[1/4,3/4]$.

## Keywords

online recalibration, logarithmic loss, calibration, proper scoring rules, minimax rate, sequential prediction

## Files

- `fancyhdr.sty`
- `iclr2027_conference.bst`
- `iclr2027_conference.sty`
- `main.bbl`
- `main.pdf`
- `main.tex`
- `math_commands.tex`
- `natbib.sty`
- `references.bib`
- `supplement.zip`
