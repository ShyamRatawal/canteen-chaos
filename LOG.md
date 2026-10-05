# Debug log

Your notes. One entry per bug you fixed, using the template below.

This file is read as carefully as your code. A correct fix you cannot
explain counts for little; a bug you could not fix but investigated
honestly still counts for something.

Delete the example before you submit.



## Example — delete this

### CC-99 — "The cart total is wrong"

**Reproduced:** Added 2 dosas at Rs. 60 each. The cart showed
Rs. 119.99999 instead of Rs. 130. Happened every time, on any dish with
a price ending in .50.

**Cause:** The total was being added up with plain floating point and
never rounded, so 0.1 + 0.2 style errors showed up on screen. The
rounding helper existed but this one place was not using it.

**Fix:** Ran the total through the existing rounding helper instead of
adding a new one, so every price on screen goes through the same path.

**Checked:** Cart, checkout and the order screen all show Rs. 130 now.
Prices without decimals still show without a trailing .00.

**Time:** about 40 minutes, most of it working out that the cart and the
order screen round in different places.



## CC-0X — "<the complaint, in short>"

**Reproduced:**

**Cause:**

**Fix:**

**Checked:**

**Time:**



## Could not fix

For anything you investigated but did not solve. Say what you tried and
where you got to. This is worth marks — leaving it blank when you got
stuck is not.

### CC-0X — "<the complaint>"

**What I tried:**

**Where I got to:**

**What I would try next:**


## Extra credit

Anything not on the bug log: a problem you found yourself, a test you
wrote, or a fix you are unsure about. Same format, plus one line on how
you noticed it.




### CC-01 : "The search suggestions are behind everything"

**Reproduced:** Searched for some coffee and weren't able to see the suggestions as it was behind the cat tabs. 

**Cause:** the stacking order for div was the issue. cat tabs was overlapping the suggestions because of a higher z index.

**Fix:** In the cat tabs changing the value to 0 works. But why 0? there were one button and one div tag stacked on top and by changing the stacking relationship the cursor now reaches the button. also by changing the z index to 0 the cat tabs reach the bottom of the stacking order.

**Checked:** By ordering the coffee. Now the unwanted stacking is gone.

**Time:** took like an hour as I'm learning new topics throughout the process.




### CC-02: "Can't read anything in dark mode"

**Reproduced:** Toggled the dark and light mode and faced the same issue

**Cause:** the .name-btn was inheriting color from a div tag .dish-body the color there was fixed instead of a var which changed with the theme.

**Fix:** By changing the color in dish-body from a fixed color to a variable color which is already present in the root theme to match the colors. When the theme is light the .dish-body gets the value from the root and when its dark it gets the value from the dark theme code block

**Checked:** Now when dark mode is on the text is visible and when light mode is on the text is still visible

**Time:** Took me like 40 mins to learn some new CSS and inheritance of different code blocks 
