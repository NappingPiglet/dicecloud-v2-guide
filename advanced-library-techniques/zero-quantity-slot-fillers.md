# Zero-Quantity Slot Fillers

The simplest way to allow the selection of an arbitrary number of fillers for a slot is to set the slot's expected quantity to 0. This creates a dilemma, however, since the slot will now always appear on the summary card, even if there are no more potential options left to select - do this too much, and your Character tab can get pretty messy in a hurry.

One way to get around this is to use a "Hide slot" filler containing an attribute with a value of 1, which is then referenced by the slot's condition field. This allows the user to select as many fillers as they wish, then select "Hide slot" to remove it from the display. However, this comes with its own drawback; a falsey condition will hide the slot entirely, even from the detailed Build view! Now you can't unhide the slot without digging into the tree to manually remove the "Hide slot" filler.

Luckily, there is a very simple solution:

* Set your slot's quantity to 1.
* Set the quantity of each slot _filler_ to 0.
* Set the quantity of the "Hide slot" filler to 1.
* Enable "Hide when full" on your slot. 

While this may seem backwards and unintuitive at first, it allows for the exact desired behavior. By setting the quantity of each filler to 0, they do not count against the expected quantity limit of the slot they fill; thus, an arbitrary number of fillers can be selected, and the "Hide slot" filler - the only one with a quantity of 1 - will actually fill the slot and hide it from the summary card, while still leaving it accessible from the detailed view.

This trick can even be applied to slots that weren't intentionally designed to use zero-quantity fillers. While the cases in which you might want to insert something additional into a slot alongside an actual intended value are rare, using a ZQF allows you to achieve just that; for example, you can use a ZQF to allow multiple bases in the auto-generated slot.

{% hint style="warning" %}
Since the add button for a full slot disappears, it is impossible to add a ZQF to a slot that is already full, even though it would fit by quantity. This means ZQFs must always be added before any filler that would completely fill the slot.
{% endhint %}

