## Format for the answers

# The interval:

```html
<EQN $PAD = 'calc'; $CASGRADER = 'mathematica'; $KEY_IMAGE_DISPLAY = '(-\infty, 0]'; ''>WAInterval["(", -Infinity, 0, "]"] {tab} optInterval = {SIMPLIFY -> False, TOLERANCE -> "0", ENDPOINTS -> True}; <g:optInterval>
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
