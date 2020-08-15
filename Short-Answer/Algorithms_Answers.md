#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n). This while loop will run n times, since a + n^2 cancels out the n^3 condition
    in the while loop.


b) O(nlogn). The for loop is executed n times, and the while loop will only last
    logn times due to the condition of j, and j doubling itself with each loop.


c) O(n). This is a single recursive call.

## Exercise II

Using a binary search, I would start off at the middle floor, and throw an egg.
If it breaks, we would move down to the middle of the building from where we were,
and throw another egg. If the egg didn't break, we would move up to the middle between
us and the top of the building. We would repeat until we had only moved one floor.

The runtime of this would be O(logn), as each time we would be able to halve the floors
that we needed to check.

def egg_chuck([n]):
    mid = len(n)//2
    if n[mid] == 'Egg broken':
        egg_chuck(n[:mid])
    elif n[mid] == 'Egg not broken':
        egg_chuck(n[mid:])
