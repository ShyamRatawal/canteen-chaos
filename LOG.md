# Debug log

Your notes. One entry per bug you fixed, using the template below.

This file is read as carefully as your code. A correct fix you cannot
explain counts for little; a bug you could not fix but investigated
honestly still counts for something.







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





### CC-05 — "The category bar scrolls away on my phone"

**What I tried:** Reproduced the issue by scrolling through the menu on a small screen. Tried changing the category bars CSS to position: sticky and top: 0, but it did not work.

**Where I got to:** Confirmed that the category and filter bar scrolls away instead of remaining visible at the top. I suspect the sticky positioning or surrounding layout may be involved, but I could not confirm the root cause.

**What I would try next:** i would inspect the parent containers, their positioning and overflow properties to understand why the sticky behavior is not working.



### CC-10 — "The price sort is reversed"

**What I tried:** Reproduced the issue by selecting the price sorting option and observing that dishes appeared in the opposite order. Inspected the event listener for #sortSelect, which updates the selected sorting option and calls loadMenu().

**Where I got to:** Identified the sorting dropdown event listener but could not confirm the exact cause. I suspect the price comparison logic may be sorting in the wrong direction.

**What I would try next:** Trace how the selected sort option is processed inside loadMenu() and inspect the .sort() comparator to check whether ascending and descending price orders are reversed.
