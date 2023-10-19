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
<EQN $PAD='calc';$CASGRADER='mathematica';$KEY_DISPLAY='commalist';''>{<EQN $a>} {tab} GradeList[Hold[key], Hold[{response}], CONTENTS -> number, FORM -> unordered] && Length[key] == Length[{response}]
```
