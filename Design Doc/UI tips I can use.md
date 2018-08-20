# UI tips I can use

## Consider changing text weight and color before size

Sometimes making text larger does make sense, but try to resist the urge to make it the first thing you try for any
element that isn't display text.

Two common color scales ("blackness" refers to color density):

1. One black color and one gray color
2. One black color, one gray color, and one lighter gray color

Likewise, you'll rarely need more than two weights:

1. Normal weight (either 400 or 500)
2. Bolder weight (either 600 or 700)

You generally want to avoid weights under 300 unless they're being used for large display text

## Avoid using borders

Subtlety is king, and few structural elements are as in-your-face as borders. Instead, consider making different
sections different colors or increasing the spacing between them.

## Figure out your action hierarchies

For any given site, there will always be a primary action. Then there will be some set of secondary action(s), followed
by tertiary action(s). Figure these out and structure the site to make completing the important actions as easy as
possible.

Refactoring UI says this of the actions:

* **Primary actions should be obvious.** Solid, high contrast background colors work great here.
* **Secondary actions should be clear but not prominent.** Outline styles or lower contrast background colors are great options.
* **Tertiary actions should be discoverable but unobtrusive.** Styling these actions like links is usually the best approach.

Also, different actions can become primary/secondary/tertiary based on context. For example, deleting something might be
a tertiary action normally, but when a user clicks the button for it, there's a good chance they're focused on it over
anything else at that point. Once that happens, deletion becomes a primary action, which should be communicated
accordingly.

## Don't sacrifice function for form

You want both, but at the end of the day, a functional but ugly app is magnitudes more useful than a beautiful but
broken or rudimentary one. Always consider accessability. In a lot of cases, you really can't afford to decrease the
text contrast too much (60% black on 100% white is about the highest you should let yourself get away with). Also,
people **really** don't like it when you remove borders from form inputs.

## Increasing contrast of white text

You probably shouldn't be doing this on solid color backgrounds, but giving white text a drop shadow helps it stand out
against backgrounds – especially if the background itself it pretty light.

## Pure gray text tends to look off when put on a colored background

Give it a little color by saturating it based off the background color.

## You don't have to stick with the defaults for how inputs look

I know you can get really crazy with how you style radio buttons. Presumably, you can do this with most forms. As long
as the inputs communicate how they work, I don't see any problem with overhauling how the default interfaces look. You
don't have to be beholden to the boring parts of the internet, even if they've been around for two decades.

## Overprinting can look pretty slick

Just have large side content (like images) exceed the bounds of an element and set `overflow` to `hidden`. Doing this
can also help elements feel proportional, surprisingly enough.

## Choose the right "spacing" multiples

CSS doesn't support leading, which does make things a bit trickier. But basing all your spacing off of some value like
`6px` that's not too big (not also not too small like `2px` is, as that doesn't define strong enough guidelines) helps
establish vertical rhythm. Honestly, I feel like the best thing to do is to define things in terms of the body text's
leading (or the closest thing to it), even if that value ends up getting subdivided later.

## Overlapping and interlocking elements make designs feel more cohesive

Websites have access to plenty of properties that can simulate depth, and placing some elements over each other can not
only tie them more closely together but even encourage the user to scroll further down.

## If the images you're designing for presents too many colors, change them

If you have no choice but to place images with a disparate set of colors next to each other, make them uniform. You can
make their colors uniform. One strategy that Refactoring UI uses a lot (maybe abuses) is making the images grayscale
(this can be done with `filter: grayscale(100%)`), making the background some other color, and then setting the image's
`mix-blend-mode` to `multiply`.
