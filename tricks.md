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
    <div class="wa1par">
        <strong>The following formulas may be used to complete the question</strong>
        <div class="wa1given">
            <latex>
                $$\frac{d}{dx}\left(\sin^{-1}(x)\right)= \frac{1}{\sqrt{1-x^2}}$$</latex>
</div>
        <div class="wa1given">
            <latex>
                $$\frac{d}{dx}\left(\tan^{-1}(x)\right)= \frac{1}{1+x^2}$$</latex>
</div>
        <div class="wa1given">
            <latex>
$$\frac{d}{dx}\left(\sec^{-1}(x)\right) = \frac{1}{x\sqrt{x^2-1}}.$$
</latex>
        </div>
    </div>
</div>


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
