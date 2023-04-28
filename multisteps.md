# The template to create a multi-step question

## The preample:

```HTML
<link rel="stylesheet" type="text/css" href="/csstyle/style.css"/>
<em>
  This question has several parts that must be completed sequentially.
  You can skip any part of the question to continue the next step.
  However, you will not receive any points for the skipped part,
  and you will not be able to come back to resubmit the answer for the skipped part.
</em>
```

## The premise of all steps:
Notes: We can ignore this part while working on editing mode. Once we are done, we can add this later.

```HTML
<tutorial order='ascending' button='Start'>
<premise title='Limits by Rationalizing'>
<link rel="stylesheet" type="text/css" href="/csstyle/style.css"/>
<div class="wa1par">
Statment of the problem:
  <div class = 'indent'>
    <watex>
    \[
      \lim_{x \rightarrow <s:infinity>}{x^2}
    \]
    </watex>
  </div>
</div>
</premise>
```

## We now start with the first step:

```HTML
<step skip_text = 'Skip' button = 'Click here to begin!' >
<div class="wa1par">
  Do you remember how to calculate a limit at infinity?
</div>
<div class="wa1ans">
  <watex>
    \[
      \lim_{x \rightarrow <s:infinity>}{x^2} = <_>.
    \]
  </watex>
</div>
</step>
```

## The following steps are similar:

```HTML
<step skip_text = 'Skip' >
<div class="wa1par">
  From the previous step, we have something...
  <div class="indent">
    <watex>
    \[
    x^2+y^2=1.
    \]
    </watex>
  </div>
  Now, we can continue...
</div>
<div class="wa1ans">
  <div class="indent">
    <watex>
    \[
    <s:alpha> + <s:beta> = <_>.
    \]
    </watex>
  </div>
</div>
</step>
```

## The conclusion and closing tutorial tag:

```HTML
<conclusion>
        You have completed the problem.
</conclusion>
</tutorial>
```
