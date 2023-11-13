## Format for the answers

# The interval:

```html
<EQN $PAD = 'calc'; $CASGRADER = 'mathematica'; $KEY_IMAGE_DISPLAY = '(-\infty, 0]'; ''>WAInterval["(", -Infinity, 0, "]"] {tab} optInterval = {SIMPLIFY -> False, TOLERANCE -> "0", ENDPOINTS -> True}; <g:optInterval>
```

# Union of intervals:
```HTML
<EQN>$PAD='calc'; $CASGRADER='mathematica'; $KEY_IMAGE_DISPLAY='(-\infty, $a), ($b, \infty)'; ''</EQN>WAUnion[WAInterval["(",-Infinity,<EQN $a>,")"], WAInterval["(",<EQN $b>,Infinity,")"]] {tab} optInterval = {SIMPLIFY -> False, TOLERANCE -> "0", ENDPOINTS -> False}; <g:optInterval>
```


# The list (un-ordered):

```html
<EQN $PAD='calc'; $CASGRADER='mathematica'; $KEY_DISPLAY='commalist';''>{Exp[1/<EQN $a>]} {tab} GradeList[Hold[key], Hold[{response}], FORM->unordered]
```

Or

```html
<EQN $PAD='calc';$CASGRADER='mathematica';$KEY_DISPLAY='commalist';''>{<EQN $a>, <EQN $b>} {tab} GradeList[Hold[key], Hold[{response}], CONTENTS -> number, FORM -> unordered] && Length[key] == Length[{response}]
```

# The point has specific order:
```
<EQN $PAD = 'calc'; $CASGRADER = 'mathematica'; $KEY_DISPLAY = 'commalist'; ''>{<EQN $a>Sqrt[3]/3, <EQN -5*$a**4 + 9*$d>/9} {tab} GradeList[Hold[key], Hold[{response}], CONTENTS -> number, FORM -> ordered, TOLERANCE->0] && Length[key] == Length[{response}]
```

# Multiple choice with figures:

```html
<table class="indent plotmc">
        <tr>
            <td> <_> </td>
            <td> <_> </td>
        </tr>
        <tr>
            <td> <_> </td>
            <td> <_> </td>
        </tr>
    </table>
```
We need to use `<SECTION nobr>` in the question source and `<SECTION><EQN $SET_EACH_POSITION = 1;''>` in the answer box.


# Integral as limit with options

```PERL
  $function  = ' res = ReleaseHold[Rationalize[Hold[response]]]; var = VARIABLE /. optSeries; range = RANGE /. optSeries; center = CENTER /. optSeries; maxdeg = Exponent[key, var]; iterVar = range[[1]]; isEqual = FullSimplify[PowerExpand[Sum[key, Evaluate[range]] - Sum[res, Evaluate[range]]] == 0]; isCentered = If[center === any, True, If[range[[2]] == range[[3]], Apply[And, FullSimplify[Coefficient[key, (var - center), #] - Coefficient[res, (var - center), #] == 0] & /@ Range[0, maxdeg]], Apply[And, FullSimplify[PowerExpand[# == 0], Assumptions -> {Element[iterVar, Integers], iterVar > range[[2]]}] & /@ {res /. Flatten[{ToRules[Apply[Or, Cases[Reduce[key == 0 && Element[iterVar, Integers] && iterVar > range[[2]], var, Reals], _Equal, {0, Infinity}]]]}]}]]]; isEqual && isCentered';
```

where the answer needs to check

```html
<EQN $PAD = 'calc'; $CASGRADER = 'mathematica'; $KEY_IMAGE_DISPLAY='\left(\left($a + \frac{${diff}i}{n}\right)^2 + \sqrt{1 + 2\left($a + \frac{$diff i}{n}\right)}\right)\frac{$diff}{n}'; ''> n:((<EQN $a> + (<EQN $diff>*Sqrt[-1])/n)^2+ Sqrt[1 + 2*(<EQN $a> + (<EQN $diff>*Sqrt[-1])/n)])*(<EQN $diff>/n) {tab} optSeries = {RANGE -> {n, 1, 100}, CENTER -> any, VARIABLE -> i}; <EQN $function>
```
