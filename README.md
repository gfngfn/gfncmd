<!-- -*- coding: utf-8 -*- -->

# `gfncmd.sty`

`gfncmd.sty` is a LaTeX package useful for making LaTeX codes more structurized and semantic
(yet its documentation is under construction).

# `gfnlf.sty`

`gfnlf.sty` is a LaTeX package for writing logical formulae in structurized syntax.
An example is here:

    \usepackage{amsmath}
    \usepackage{amssymb}
    \usepackage{gfncmd}
    \useRightarrowaslimpl
    \usepackage{gfnlf}
    \usesinglequantifier
      ...
    $\forallin{x|y|z}{P}{\lflimpl{\lfland{x \pord y}{y \pord z}}{x \pord z}}$

generates ∀x, y, z∈P (x ≦ y ∧ y ≦ z ⇒ x ≦ z) ,
where `\useRightarrowaslimpl` and `\usesinglequantifier` are notation options.
If you change options like

    \usepackage{amsmath}
    \usepackage{amssymb}
    \usepackage{gfncmd}
    \useinvertedCaslimpl
    \usepackage{gfnlf}
    \usedotpluralquantifier
    \makeleftparenmandatory{lflimpl}{lfland}
      ...
    $\forallin{x|y|z}{P}{\lflimpl{\lfland{x \pord y}{y \pord z}}{x \pord z}}$

then it generates ∀x∀y∀z∈P. ((x ≦ y ∧ y ≦ z) ⊃ x ≦ z).
