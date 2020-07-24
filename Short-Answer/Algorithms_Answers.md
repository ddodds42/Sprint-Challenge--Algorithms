#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) Linear Runtime Complexity, O(n)


b) Log Linear Runtime Complexity, O(n Log(n))


c) Linear Runtime Complexity, O(n)

## Exercise II
This problem is optimized by a binary search solution.
It has a Logarithmic runtime complexity, O(Log(n)).
This Egg_dropper function presumably takes a list of stories marked either 0 or 1, 0 meaning "eggs do not break when dropped from this story" and 1 meaning the opposite. This means that f would be the lowes index position of the list containing a 1; that all 'stories' below f contain value 0, and all stories above f contain value 1.

Without further adieu than, here's the pseudocode!

Egg_drop_fxn (list_like_above):
    mark a head index value (bottom story in consideration) as the ground story (0) to start.
    mark a tail index value (top story in consideration) as the penthouse (len(list) - 1) to start.
    as long as the head and tail values haven't met (while loop):
        locate the median story (median between the head and tail values)
        if the median is 1 (broken egg) and the story beneath it (median - 1) is 0 (egg intact):
            that's the story we're looking for! Return that median story value
        if the median is 1 and the story beneath is 1 also:
            we're too high. shift the tail value to (median-1) and run the while loop again.
        if the median is 0 and the story above is 1:
            that next story is f! Return (median + 1)
        if the median is 0 and the story above is 0:
            we're too low. shift the head to (median+2) and repeat the loop.
    or just return NOT FOUND if the list is obstinent and has no 1's... which never happens with real eggs... but in fictional code it can I guess.
