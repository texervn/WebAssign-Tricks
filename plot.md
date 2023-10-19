## Plot the graph in WA

# Plot a right triangle

```html
<div class='figure'>
    <waplot axes='false' frame='false' view='-1, 6;-1,4'>
        <plot type='text' color='black' size='18' location='3,-0.3'>
            $b
        </plot>
        <plot type='text' color='black' size='18' location='5.2,1.5'>
            $a
        </plot>
        <plot type='text' color='black' size='22' location='0.8,0.3'>
            \[Alpha]
        </plot>
        <plot type='text' color='black' size='22' location='4.5,2.4'>
            \[Beta]
        </plot>
        <plot type='parametric' vars='t' range='Pi/2-ArcTan[3/5], Pi/2' thickness='thick' color='black'>
            {0.5*Sin[t], 0.5*Cos[t]}
        </plot>
        <plot type='parametric' vars='t' range='Pi, Pi+ArcTan[5/3]' thickness='thick' color='black'>
            {0.5*Sin[t] +5, 0.5*Cos[t]+3}
        </plot>
        <plot type='arrow' arrowheadsize='tiny' color='black' thickness='thick'>
            {{4.6,0.4},{4.6,-0.05}}
        </plot>
        <plot type='arrow' arrowheadsize='tiny' color='black' thickness='thick'>
            {{4.6,0.4},{5.05,0.4}}
        </plot>
        <plot type='1d' vars='x' color='blue' thickness='thick' range='0,5'>
            0
        </plot>
        <plot type='1d' vars='x' color='blue' thickness='thick' range='0,5'>
            3*x/5
        </plot>
        <plot type='implicit' vars='x,y' range='4.5,6;0,3' color='blue' thickness='thick'>
            x==5
        </plot>
    </waplot>
</div>

```
