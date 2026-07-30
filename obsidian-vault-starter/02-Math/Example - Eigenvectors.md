---
tags: [concept, linear-algebra]
subject: linear-algebra
status: solid
created: 2026-07-30
---

# Eigenvectors

## One-line definition (in your own words, no copy-paste from the book)
A vector that a matrix only stretches or shrinks, never rotates off its own line.

## Feynman explanation
> Explain this to a smart 12-year-old. No jargon, no notes open. If you can't, you don't understand it yet.

Imagine a matrix as a machine that grabs every arrow in space and moves it somewhere else. Almost every arrow gets moved *and* rotated to point a new direction. But a few special arrows only get longer or shorter — they keep pointing exactly the same way. Those special directions are the eigenvectors, and how much longer/shorter they get is the eigenvalue.

## The picture
> The geometric/visual intuition — sketch it in Excalidraw or embed a photo of a hand-drawn diagram.

![[]]
*(Open Excalidraw here and draw: a unit circle, the matrix's action turning it into an ellipse, and the two axes of the ellipse as the eigenvector directions — this is the 3Blue1Brown picture, redraw it yourself from memory.)*

## Formal statement / derivation
For a square matrix $A$, a nonzero vector $v$ is an eigenvector with eigenvalue $\lambda$ if:
$$Av = \lambda v$$
Equivalently, $(A - \lambda I)v = 0$ has a nonzero solution, which requires $\det(A - \lambda I) = 0$ — the characteristic equation.

## Handwritten work
![[]]
*(Work a 2x2 example by hand — pick a shear matrix, solve the characteristic polynomial, find both eigenvectors, then check $Av = \lambda v$ numerically in Python.)*

## Anki flashcard(s)
> Requires the Obsidian_to_Anki plugin + Anki desktop + AnkiConnect. Run "Obsidian_to_Anki: Scan Notes" to push these into your Anki deck.

START
Basic
Front: What equation defines an eigenvector/eigenvalue pair?
Back: $Av = \lambda v$ — $v$ is only scaled, not rotated, by $A$.
Tags: concept::linear-algebra

Basic
Front: How do you find the eigenvalues of a matrix $A$?
Back: Solve $\det(A - \lambda I) = 0$ (the characteristic equation).
Tags: concept::linear-algebra
END

## Connections
- Diagonalization (Stage 1 "prove it" milestone) uses eigenvectors as the change-of-basis columns.
- Principal component analysis (Stage 4) is eigenvectors of a covariance matrix.
- Stability analysis in nonlinear dynamics (Stage 3, Khalil) linearizes a system and checks the eigenvalues of the Jacobian.

## Open questions
- Why do complex eigenvalues always come in conjugate pairs for real matrices? (Revisit after Stage 3 complex analysis.)

## Source(s)
- Strang, *Introduction to Linear Algebra*, ch. 6.
- 3Blue1Brown, *Essence of Linear Algebra*, ep. 14.
