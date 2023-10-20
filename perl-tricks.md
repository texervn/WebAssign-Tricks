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




# Perl array:

```Perl
$i = randnum(0,1,1);
@fn = ('\\arcsin', '\\arctan');
@solns = ('<eqn $ab>/Sqrt[1 - (<eqn $a>x)^2]', '<eqn $ab>/(1 + (<eqn $a>x)^2)');
$fx = $fn[$i];
$ans = $solns[$i];
```