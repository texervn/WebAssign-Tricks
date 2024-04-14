# Using Loops for creating problems

## While Loop:

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




## Perl array:

```Perl
$i = randnum(0,1,1);
@fn = ('\\arcsin', '\\arctan');
@solns = ('<eqn $ab>/Sqrt[1 - (<eqn $a>x)^2]', '<eqn $ab>/(1 + (<eqn $a>x)^2)');
$fx = $fn[$i];
$ans = $solns[$i];
```


## Bonus points:

```html
<eqn ($RESPONSE_NUM < 2) ? $POINTS * 1.05 : (2 < $RESPONSE_NUM) ? $POINTS * 0.7 : $POINTS>
```

## Mapping

```PERL
$dx = 0.1;
@x = map($dx*$_,0..$n);

@fx = map(fx($x[$_]),0..$n);

#slice and concat arrays:
$k=2;
@rdx = (@fxl[0..$k], @fx[$k+1..2*$k], @fx[2*$k+1..$n]);
$r_sum = sum(@fx[0..$n-1])*$dx;

sub fx {
my $x = $_[0];
return $x**2;
};
```

## Pass array ref as arguments (good tips)

```PERL

$wa_plot = gen_waplot(\@x, \@fx);

sub gen_waplot {
    my ($xs, $ys) = @_;

    my $waplot_str = "";

    for my $i (0..$n-1) {
        $yi = @$ys[$i];
        $xi = @$xs[$i];
        $xj = @$xs[$i+1];
        if ($yi != 0) {
        $waplot_str .= "<plot type='region' range='$xi,$xj; 0,$yi' vars='x, y' color='lightblue'> x > $xi && x < $xj</plot>";}
    }
    $waplot_str .= "<plot type='implicit' range='0,$a; $y_min,$y_max' vars='x,y' color='blue' thickness='thick'>y==f(x)</plot>";

    return $waplot_str;
}
```


## Function to split commas for numbers.

```PERL
	sub format_number {
		my $number = shift;
		$number =~ s/(?<=\d)(?=(?:\d{3})+$)/,/g;
		return $number;
	}
```

Or we can use the following simple function in Webassign: `commas`


