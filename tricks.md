## Using Loops for creating problems

# While Loop:

```Perl
<eqn>
$k = randnum(4,6,1);
my $counter = 1;
$prod = "";
while ($counter < $k) {
$prod = $prod . "(n + $counter)";
$counter++;
}
''
</eqn>
```


# Part inside question

```html

<link rel="stylesheet" type="text/css" href="/csstyle/style.css"/>


<div class="subblock">
    <div class="sublabel">
        (a)
    </div>
    <div class="subpart">
 <div class="wa1par">
        Find the derivative of the function.
        <div class='indent'>
            <watex> y = ${b}<s:thinsp>${fx}(${a}x) </watex>
        </div>
    </div>
</div>
</div>
<div class="wa1ans">
    <div class="indent">
        <watex>\[y' = <_>\]</watex>
    </div>
</div>
```

# Perl array:

```Perl
$i = randnum(0,1,1);
@fn = ('\\arcsin', '\\arctan');
@solns = ('<eqn $ab>/Sqrt[1 - (<eqn $a>x)^2]', '<eqn $ab>/(1 + (<eqn $a>x)^2)');
$fx = $fn[$i];
$ans = $solns[$i];
```
