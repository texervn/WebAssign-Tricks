## Useful tricks for HTML

# Font size for math formula:

```html
<div class="indent" style="font-size:150%;">
<watex>\[F(x) = e^{${a}x \sin(${b}x)}\] </watex>
</div>
```

# Box around the text:

```html
<span style="border:solid 1px; padding: 10px;"><watex>\[\frac{<s:pi>}{2}, \frac{<s:pi>}{2} + 3 \sin(\frac{<s:pi>}{2})\]</watex></span>
</div>
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
