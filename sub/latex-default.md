# Default settings of packages

## `amsthm`

```tex
\newtheoremstyle{plain}
  {\topsep}     % ABOVESPACE
  {\topsep}     % BELOWSPACE
  {\itshape}    % BODYFONT
  {0pt}         % INDENT (empty value is the same as 0pt)
  {\bfseries}   % HEADFONT
  {.}           % HEADPUNCT
  {5pt plus 1pt minus 1pt} % HEADSPACE
  {}            % CUSTOM-HEAD-SPEC

\newtheoremstyle{definition}
  {\topsep}     % ABOVESPACE
  {\topsep}     % BELOWSPACE
  {\normalfont} % BODYFONT
  {0pt}         % INDENT (empty value is the same as 0pt)
  {\bfseries}   % HEADFONT
  {.}           % HEADPUNCT
  {5pt plus 1pt minus 1pt} % HEADSPACE
  {}            % CUSTOM-HEAD-SPEC

\newtheoremstyle{remark}
  {.5\topsep}   % ABOVESPACE
  {.5\topsep}   % BELOWSPACE
  {\normalfont} % BODYFONT
  {0pt}         % INDENT (empty value is the same as 0pt)
  {\itshape}    % HEADFONT
  {.}           % HEADPUNCT
  {5pt plus 1pt minus 1pt} % HEADSPACE
  {}            % CUSTOM-HEAD-SPEC
```
Source: https://tex.stackexchange.com/a/17555/

## `geometry`

```tex
\geometry{
                      % paper size is unchanged
  scale=0.7,          % body size is 70% of paper size
                      % one-sided documents
  hmarginratio=1:1,   %   left margin : right margin = 1:1
                      % two-sided documents
  % hmarginratio=2:3, %   left margin : right margin = 2:3
  vmarginratio=2:3,   % top margin : bottom margin = 2:3
  ignoreall           % the header, footer, marginal notes are excluded
                      %   when calculating the size of body
}
```
Source: `texdoc geometry`, sec. 6.4


## `subcaption`

```tex
\captionsetup[sub]{
  margin      = 0pt,
  size        = smaller,
  labelformat = parens,
  labelsep    = space,
  skip        = 6pt,
  list        = false,
  hypcap      = false
}
```
Source: `texdoc subcaption`, sec. 1


## `hlist`

```tex
\sethlist{
  pre skip       = \medskipamount,
  post skip      = \medskipamount,
  left margin    = 0pt,
  col sep        = 2.5em,
  item offset    = 1.75em,
  label sep      = 0.25em,
  label width    = *,
  label align    = left,
  show label     = true,
  pre label      = \bfserise,   % "\bf" if loaded as tex package
  label          = \arabic{hlisti}.,
  post label     = {},
  item sep       = 0pt,
  list parindent = 0pt,
  pre item       = {},
  post item      = {},
  resume         = false,
  autoindent     = false,
  show frame     = false
}
```
Source: `kpsewhich hlist.tex`, lines begin with `\setKVdefault[\hlstname]`
