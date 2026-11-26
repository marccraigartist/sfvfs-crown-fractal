# SFVFS Crown Fractal: loop and address notes

This note documents the companion [Shared-Seat Holonomy Explorer](holonomy.html) and the precise meaning of its three kinds of apparent “meeting.” It is a geometric experiment on Marc Craig's published [Crown Fractal](index.html), not an RH, prime, quantum, or P-versus-NP result.

## The graph

The parent gyroscope uses three perpendicular unit great circles, in the xy, yz and zx planes. Each has 12 seats at 30° intervals. Their 36 ring-seat *incidences* give 30 distinct 3D vertices: ±x, ±y and ±z each belong to two rings. These six vertices have degree 4; the other 24 have degree 2. Each ring contributes 12 edges, for 36 total. The connected graph is the octahedron's 1-skeleton with each of its 12 edges subdivided into three steps. Its cycle rank is `36−30+1=7`, and its embedding on the sphere bounds eight octant faces (`30−36+8=2`). A double-ring hub is not two distinct recursive-tree parents.

## Genuine spherical holonomy

Transport a tangent arrow along each 30° great-circle edge, using the shortest-geodesic rotation about the normalized cross product of its endpoints. Only when the route returns to its start does the signed angle between the original and returned arrow define loop holonomy. An open route has a transported arrow but no basepoint holonomy angle.

The positive octant boundary `+x→+y→+z→+x` takes 9 graph edges (three per quarter circle), bounds one-eighth of the unit sphere, and rotates the arrow by +90° under the explorer's orientation convention. Reverse traversal gives −90°. This is the classical sphere-area/holonomy relation, not a new theorem: Eguchi, Gilkey and Hanson work through **exactly this triangle** in [their 1980 differential-geometry review](https://empg.maths.ed.ac.uk/Activities/GT/EGH.pdf), pp. 276–278; see also [UCLA's differential geometry notes](https://www.math.ucla.edu/~sucharit/120A-notes.html).

Two **12-edge loops with the same start and end** make the distinction visible: a complete xy great circle has holonomy 0° modulo 360°, whereas `+x→+y→+z→−y→+x` encloses two octants and has 180° modulo 360°. Repeating a loop 12 or 144 times gives 144 or 1,728 steps. Its final angle may wrap to 0° even when the trajectory accumulated many nontrivial turns; report both the route history and angle modulo 360°.

Spherical tangent-plane holonomy at a fixed basepoint is an `SO(2)` rotation and is **commutative**. “Non-commutative” here applies separately to the affine recursion maps below.

## Recursive addresses and map order

Let `S` be the 30 unique unit seat vectors and `q=sin(π/12)`. The recursive similarities are `f_s(x)=s+q x`. A finite address `(s₀,…,s_(n−1))` has centre `P=Σ_(k=0)^(n−1) q^k s_k`. Order matters:

`f_s∘f_t(x) − f_t∘f_s(x) = (1−q)(s−t)`.

Two of the 36 **slot labels** at one of six shared hubs name the *same* `s` and therefore the same map. That is an exact label alias. Different graph walks can return to the same graph vertex. Neither phenomenon asserts that two distinct addresses over the 30 **unique** maps have the same recursive centre.

In fact, distinct equal-length finite addresses over these 30 maps have **different exact 3D centres**. Here is a short proof. All seat coordinates lie in `F=Q(√3)`, while `q=(√6−√2)/4` does not lie in `F` and `m=q²=(2−√3)/4` does. A finite equality of two centres splits into an even and odd parity sum `E+qO=0` with `E,O∈F³`, so `E=O=0`. Within either parity sum, the first unequal seat vectors have distance at least `δ=2sin(π/12)≈0.517638`; later terms in powers of `m` can cancel at most `2m/(1−m)≈0.143594`. Thus the first unequal digit cannot cancel. The same argument applies repeatedly to both parities. This proof concerns equal-length **finite** words; it does not assert a uniqueness theorem for all infinite addresses or unequal lengths.

## An exact shadow collision under the flat projection

The 2D screen projects along `(1,1,1)`. It can identify distinct 3D centres. In source station order, the unrestricted depth-three address words

`A=(1,0,9)`, `B=(18,0,3)`

satisfy `P(A)−P(B)=(√3/2)(1,1,1)`. Therefore their flat screen positions are **exactly identical**, although their 3D distance is `3/2`. The words are choices of IFS digits, **not** nearest-neighbour walks on the 36-edge graph. An independent exact symbolic enumeration of all `30³=27,000` depth-three words found 27,000 distinct 3D centres and 26,820 distinct projected signatures: 180 projected pairs of multiplicity two. These are six outer-digit collision pairs, each with any of 30 middle digits. The shared hubs do not cause this projection effect; the sample happens to use a hub as its middle digit.

Numerical screen-pixel closeness is a third, tolerance-dependent category; do not confuse it with this exact projection equality.

## Reading a long run

The 12/144/1,728 controls describe **graph-walk time** and accumulated transport events. They do not enumerate `30^n` recursive addresses. At depth 144 or 1,728 the factor `q^n` is far below ordinary floating-point spatial resolution, so an animation of long loops should show vertex visits, returns and transported-frame history instead of pretending to resolve separate deep centres. The same graph and holonomy rule repeats at each geometrically similar child scale.
