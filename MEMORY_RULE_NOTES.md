# SFVFS Crown Fractal — a finite history rule

This documents the experimental [Memory Stem Explorer](memory.html), a companion to the [fixed-rule Crown Fractal](index.html) and [shared-seat holonomy explorer](holonomy.html). It is a specified visualization experiment, not a new Lean theorem, RH proof, or prime/quantum model.

## Station labels and state

Three perpendicular great circles have 12 incidence labels each: `xy:B12, xy:B1, …, xy:B11`, and likewise for `yz` and `zx`. Their 36 labels occupy 30 distinct unit directions `s(ℓ)∈ℝ³`. Six axis endpoints are shared hubs. A label is therefore a **route into a station**; two different labels can choose the same immediate position while leaving different ring history.

Let `q=sin(π/12)≈0.2588190451`. Each node has a center `c`, scale `L`, incoming ring `r` (or none at the root), current station, and a bounded charge `m∈{0,1,2}`. The root has `c=0`, `L=1`, `r=none`, `m=0`, and the shared clock at B12. The charge is an intentionally minimal proposed B13-like record: a finite summary, not an archive of the whole address.

For a selected incidence label `ℓ` with direction `s=s(ℓ)`, the child **reads its parent's charge first**:

`g(m)=1+0.10m`, `c'=c+L·g(m)·s`, `L'=L·q·g(m)`.

In local coordinates this is the similarity `f_(s,m)(x)=g(m)s+qg(m)x`. Its rule depends on the state carried by the parent, unlike the fixed control `f_s(x)=s+qx`.

Only after making the child does it **write** the next charge. A ring switch is counted when the chosen ring differs from the incoming ring and the move leaves a shared hub. If there is such a switch, `m'=2`; otherwise, if the chosen station is a hub, `m'=1`; otherwise `m'=max(0,m−1)`. The child stores the selected ring and station for the following move. A nonhub route with `m=0` continues as an exact fixed-rule negative control. The update formula accepts all 36 labels; the explorer's visible forest samples **neighboring graph walks** to keep rendering finite. This policy changes geometry, not the mathematical label alphabet.

The displayed A and X crowns remain opposite on all three axes. They share the global 12-seat clock. For clock cursor `b` and charge `read` used in this child's geometry, the local A angle is `t=π/2−2π(b mod 12)/12−read·π/18`; the X angle is `t+π`. Each read charge adds a 10° local phase offset while all axes keep the same global clock speed. That offset is a chosen display and state rule, not a consequence of zeta zeros or the established B-constraint certificate.

## The shared-hub witness

Compare two label paths under the same clock:

`A = (xy:B12, xy:B1, xy:B2)`

`B = (zx:B3, xy:B1, xy:B2)`.

The first labels both denote `+x`. At depth one both centers are `+x`, scales are `q`, and charges written are `1`. At depth two the identical `xy:B1` choice reads `m=1` in both histories: their centers and scales still match (`L₂=1.1q²≈0.07368603`). But the B-labeled history switches from `zx` to `xy` while leaving `+x`, writing `m=2`; A remains in `xy` and decays to `m=0`. The same `xy:B2` choice next reads different charges, so the depth-three centers separate by `0.2L₂≈0.0147372056` and the child scales differ by `0.2qL₂≈0.0038142695`. The letters A/B here label **comparison paths**, not the antipodal A/X bodies in the artwork.

Holding the label paths fixed while disabling reads of `m` makes both address centers coincide through these three steps. The **write-only** control still records the same charge packets but forces `read=0` in center, scale and crown-phase calculations; **off** forces `read=0` and suppresses writes. The active versus write-only comparison is the causal ablation: the separation comes from reading history, not from a changed seat sequence or different global clock phase. The two paths have distinct **labels**, even while their selected 3D station directions coincide on the first step.

For the six displayed moves, A/B charges read are `0/0, 1/1, 0/2, 0/1, 1/1, 0/0`. The fourth choice `xy:B3` reaches the shared `+y` hub and writes a new packet `1` on both paths. Both charges have returned to zero by the sixth move, yet the centers and scales altered earlier remain different (center separation about `0.0214825149` at move six). This is a precise instance of **finite observable memory leaving a lasting geometric trace** in the selected recursion; it does not imply an unbounded internal register.

## Why the construction remains bounded

The effective contraction ratio is at most `1.2q≈0.3105828542<1`. A state-independent conservative bound for the absolute center is

`|c_n|≤1.2·Σ_(j=0)^(n−1)(1.2q)^j < 1.2/(1−1.2q)≈1.7406`.

With the specified `m=0` root, the first displacement is exactly one, yielding the sharper bound `|c_n|≤1/(1−1.2q)≈1.4505`. This only bounds centers and does not prove uniqueness of state-dependent addresses. **Within any one parent**, all 36 child labels read the same `m`; adjacent sibling circles still touch because their center spacing is `2Lqg(m)` and each radius is `Lqg(m)`. Across different parent histories, the scale need not be the original fixed `q`, and global equal-size/tangency claims do not follow. Rendering an exponentially branching tree requires an explicit sampling or visibility cap; displayed samples are not exhaustive enumeration.

## B-constraint lineage and mathematical status

The [Volume 1 common-carrier checkpoint](https://github.com/marccraigartist/SFVFS-Liminus/blob/main/docs/VOLUME1_COMMON_CARRIER_GREEN.md) names B1 Selection, B2 Forgetting, B8 Awareness, B9 Release, and B12 finite/infinite linked continuation. In this experiment those names motivate selecting a label, noticing a shared hub, releasing an event into a **later** child read, and allowing charge to decay. Returning to B12 can therefore return to the same phase with a different finite state. This is an analogy and a chosen test policy, not a claim that the geometric multiplier `1+0.10m` satisfies the formal B predicates or follows from Lean.

The [current SFVFS-Liminus status](https://github.com/marccraigartist/SFVFS-Liminus/blob/main/docs/CURRENT_STATUS.md) explicitly describes B13 central memory and nested routing as proposed extensions whose storage/retrieval are not established by its certificate. B13 is used here as a proposed **history register**, neither a thirteenth ring seat nor a fourth spatial axis. This prototype's one-move read delay is not the full canonical B8→B9→B12→B3 timing; that would require a separate staged model and test.

History-sensitive IFS are an established mathematical family. [Mauldin and Williams (1988)](https://sites.math.unt.edu/~mauldin/papers/no67.pdf) studied graph-directed similarity constructions; [Barnsley, Elton and Hardin (1989)](https://link.springer.com/chapter/10.1007/978-1-4899-6886-9_1) studied recurrent IFS; and [Prusinkiewicz and Hammel (1991)](https://algorithmicbotany.org/papers/automata-language-and-iterated-function-systems.pdf) explicitly used automata to constrain IFS transformation sequences. With finite ring, station and charge state, this model can be represented as a static graph-directed system on an enlarged state space. Its SFVFS-specific incidence aliases, chosen feedback rule and visual behavior are the experiment; adding finite memory is not itself a new fractal class. No prime, zeta-zero, RH or P-versus-NP conclusion follows from this geometry.
