## WebAssign question template

```PERL
<eqn>
$a = randnum(1, 10, 1);
$b = randnum(1, 10, 2);
''
</eqn>
```

Question body:
```HTML
<link rel="stylesheet" type="text/css" href="/csstyle/style.css" />

<div class="wa1par">
Find the sum of the following numbers:
<watex>
\[
${a} + ${b} = <_>.
\]
</watex>
</div>

```

Answer paragraph:

```HTML
<div class="wa1ans">
    <div class="indent">
        <watex>\[sin^{-1}\left($a\right) = <_>\]</watex>
    </div>
</div>
```

Answer format:
```HTML
<EQN $PAD='calc'; $CASGRADER='mathematica';>x: <eqn $a + $b> {tab} <g:Exact>
```
