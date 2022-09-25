---
title: "Kaslaanka Theme Demo"
author: "John Doe"
date: "2021-12-21T12:00:00"
brief: "Hello World! this is just a brief of what the article is about."

tags:
    - HelloWorld
    - Demo
    - Markdown-Show

meta_img: images/example.jpg
---

[Kaslaanka](https://github.com/M1cR0xf7/Kaslaanka) is a ~~Bootstrap~~ based minimalist theme for Hugo

<div class="figure">

![](https://images.unsplash.com/photo-1639077567163-f5bcf1c94d06)

<p class="caption">
Photo by <a href="https://unsplash.com/@eberhardgross?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">eberhard 🖐 grossgasteiger</a>
on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
</p>

</div>

## Typography

Follows the ~~Bootstrap~~ based typography.

# h1 Heading

## h2 Heading

### h3 Heading

#### h4 Heading

##### h5 Heading

###### h6 Heading

---

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Deleted text~~

> Block quotes are
> written like so.
>
> They can span multiple paragraphs,
> if you like.

Some text, and some `code` and then a nice plain [link with title](/ "title text!").

and then

+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    * Ac tristique libero volutpat at
+ Very easy!

vs.

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

## Code

Inline `code` example

### Python

```python
"""
This is a pure Python implementation of the quick sort algorithm
For doctests run following command:
python -m doctest -v radix_sort.py
or
python3 -m doctest -v radix_sort.py
For manual testing run:
python radix_sort.py
"""
from __future__ import annotations


def radix_sort(list_of_ints: list[int]) -> list[int]:
    """
    Examples:
    >>> radix_sort([0, 5, 3, 2, 2])
    [0, 2, 2, 3, 5]

    >>> radix_sort(list(range(15))) == sorted(range(15))
    True
    >>> radix_sort(list(range(14,-1,-1))) == sorted(range(15))
    True
    >>> radix_sort([1,100,10,1000]) == sorted([1,100,10,1000])
    True
    """
    RADIX = 10
    placement = 1
    max_digit = max(list_of_ints)
    while placement <= max_digit:
        # declare and initialize empty buckets
        buckets: list[list] = [list() for _ in range(RADIX)]
        # split list_of_ints between the buckets
        for i in list_of_ints:
            tmp = int((i / placement) % RADIX)
            buckets[tmp].append(i)
        # put each buckets' contents into list_of_ints
        a = 0
        for b in range(RADIX):
            for i in buckets[b]:
                list_of_ints[a] = i
                a += 1
        # move to next
        placement *= RADIX
    return list_of_ints


if __name__ == "__main__":
    import doctest

    doctest.testmod()
```

### C 0xc0de!

```C
// https://www.ioccc.org/2020/carlini/hint.text

#include <stdio.h>

#define N(a)       "%"#a"$hhn"
#define O(a,b)     "%10$"#a"d"N(b)
#define U          "%10$.*37$d"
#define G(a)       "%"#a"$s"
#define H(a,b)     G(a)G(b)
#define T(a)       a a
#define s(a)       T(a)T(a)
#define A(a)       s(a)T(a)a
#define n(a)       A(a)a
#define D(a)       n(a)A(a)
#define C(a)       D(a)a
#define R          C(C(N(12)G(12)))
#define o(a,b,c)   C(H(a,a))D(G(a))C(H(b,b)G(b))n(G(b))O(32,c)R
#define SS         O(78,55)R "\n\033[2J\n%26$s";
#define E(a,b,c,d) H(a,b)G(c)O(253,11)R G(11)O(255,11)R H(11,d)N(d)O(253,35)R
#define S(a,b)     O(254,11)H(a,b)N(68)R G(68)O(255,68)N(12)H(12,68)G(67)N(67)

char* fmt = O(10,39)N(40)N(41)N(42)N(43)N(66)N(69)N(24)O(22,65)O(5,70)O(8,44)N(
            45)N(46)N    (47)N(48)N(    49)N( 50)N(     51)N(52)N(53    )O( 28,
            54)O(5,        55) O(2,    56)O(3,57)O(      4,58 )O(13,    73)O(4,
            71 )N(   72)O   (20,59    )N(60)N(61)N(       62)N (63)N    (64)R R
            E(1,2,   3,13   )E(4,    5,6,13)E(7,8,9        ,13)E(1,4    ,7,13)E
            (2,5,8,        13)E(    3,6,9,13)E(1,5,         9,13)E(3    ,5,7,13
            )E(14,15,    16,23)    E(17,18,19,23)E(          20, 21,    22,23)E
            (14,17,20,23)E(15,    18,21,23)E(16,19,    22     ,23)E(    14, 18,
            22,23)E(16,18,20,    23)R U O(255 ,38)R    G (     38)O(    255,36)
            R H(13,23)O(255,    11)R H(11,36) O(254    ,36)     R G(    36 ) O(
            255,36)R S(1,14    )S(2,15)S(3, 16)S(4,    17 )S     (5,    18)S(6,
            19)S(7,20)S(8,    21)S(9    ,22)H(13,23    )H(36,     67    )N(11)R
            G(11)""O(255,    25 )R        s(C(G(11)    ))n (G(          11) )G(
            11)N(54)R C(    "aa")   s(A(   G(25)))T    (G(25))N         (69)R o
            (14,1,26)o(    15, 2,   27)o   (16,3,28    )o( 17,4,        29)o(18
            ,5,30)o(19    ,6,31)o(        20,7,32)o    (21,8,33)o       (22 ,9,
            34)n(C(U)    )N( 68)R H(    36,13)G(23)    N(11)R C(D(      G(11)))
            D(G(11))G(68)N(68)R G(68)O(49,35)R H(13,23)G(67)N(11)R C(H(11,11)G(
            11))A(G(11))C(H(36,36)G(36))s(G(36))O(32,58)R C(D(G(36)))A(G(36))SS

#define arg d+6,d+8,d+10,d+12,d+14,d+16,d+18,d+20,d+22,0,d+46,d+52,d+48,d+24,d\
            +26,d+28,d+30,d+32,d+34,d+36,d+38,d+40,d+50,(scanf(d+126,d+4),d+(6\
            -2)+18*(1-d[2]%2)+d[4]*2),d,d+66,d+68,d+70, d+78,d+80,d+82,d+90,d+\
            92,d+94,d+97,d+54,d[2],d+2,d+71,d+77,d+83,d+89,d+95,d+72,d+73,d+74\
            ,d+75,d+76,d+84,d+85,d+86,d+87,d+88,d+100,d+101,d+96,d+102,d+99,d+\
            67,d+69,d+79,d+81,d+91,d+93,d+98,d+103,d+58,d+60,d+98,d+126,d+127,\
            d+128,d+129

char d[538] = {1,0,10,0,10};

int main() {
    while(*d) printf(fmt, arg);
}
```

`<pre>` Hello World `</pre>`
<pre>
  ___ ___         .__  .__            __      __            .__       .___
 /   |   \   ____ |  | |  |   ____   /  \    /  \___________|  |    __| _/
/    ~    \_/ __ \|  | |  |  /  _ \  \   \/\/   /  _ \_  __ \  |   / __ |
\    Y    /\  ___/|  |_|  |_(  <_> )  \        (  <_> )  | \/  |__/ /_/ |
 \___|_  /  \___  >____/____/\____/    \__/\  / \____/|__|  |____/\____ |
       \/       \/                          \/                         \/
</pre>


## Buttons

<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-outline btn-outline-success">Success</button>
<button type="button" class="btn btn-outline btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline btn-outline-info">Info</button>
<button type="button" class="btn btn-outline btn-outline-light">Light</button>
<button type="button" class="btn btn-outline btn-outline-dark">Dark</button>

## Alerts

<!-- <div class="alert alert-primary" role="alert"> -->
<!-- This is a primary alert—check it out! -->
<!-- </div> -->
<!-- <div class="alert alert-secondary" role="alert"> -->
<!-- This is a secondary alert—check it out! -->
<!-- </div> -->
<div class="alert alert-success" role="alert">
This is a success alert—check it out!
</div>
<div class="alert alert-danger" role="alert">
This is a danger alert—check it out!
</div>
<div class="alert alert-warning" role="alert">
This is a warning alert—check it out!
</div>
<div class="alert alert-info" role="alert">
This is a info alert—check it out!
</div>
<div class="alert alert-dark" role="alert">
This is a dark alert—check it out!
</div>
<div class="alert alert-outline" role="alert">
This is a light alert—check it out!
</div>

## Tables

<table class="table table-hover">
<thead>
<tr>
<th scope="col">#</th>
<th scope="col">First</th>
<th scope="col">Last</th>
<th scope="col">Handle</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row">1</th>
<td>AAAAAAAA</td>
<td>BBBBBBBB</td>
<td>@aaa</td>
</tr>
<tr>
<th scope="row">2</th>
<td>OOOOOOO</td>
<td>WWWWWWW</td>
<td>@uuuuuuu</td>
</tr>
<tr>
<th scope="row">3</th>
<td colspan="2">ppppppp</td>
<td>@twitter</td>
</tr>
</tbody>
</table>


<!-- i will not support forms right now -->
<!-- i don't think i need it at the time -->

<!-- ## Forms -->

<!-- <form> -->
<!-- <div class="form-group"> -->
<!-- <label for="exampleFormControlInput1">Email address</label> -->
<!-- <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com"> -->
<!-- </div> -->
<!-- <div class="form-group"> -->
<!-- <label for="exampleFormControlSelect1">Example select</label> -->
<!-- <select class="form-control" id="exampleFormControlSelect1"> -->
<!-- <option>1</option> -->
<!-- <option>2</option> -->
<!-- <option>3</option> -->
<!-- <option>4</option> -->
<!-- <option>5</option> -->
<!-- </select> -->
<!-- </div> -->
<!-- <div class="form-group"> -->
<!-- <label for="exampleFormControlSelect2">Example multiple select</label> -->
<!-- <select multiple class="form-control" id="exampleFormControlSelect2"> -->
<!-- <option>1</option> -->
<!-- <option>2</option> -->
<!-- <option>3</option> -->
<!-- <option>4</option> -->
<!-- <option>5</option> -->
<!-- </select> -->
<!-- </div> -->
<!-- <div class="form-group"> -->
<!-- <label for="exampleFormControlTextarea1">Example textarea</label> -->
<!-- <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea> -->
<!-- </div> -->
<!-- </form> -->

<hr>

**<span class="first-letter">L</span>orem ipsum** dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore _magna aliqua_. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

In modus congue feugait eos. In nec nonumy volutpat corrumpit, sea assentior quaerendum no, cum affert scripta ea. No nihil voluptaria pro. [Erat democritum mei no](https://example.com), homero quodsi aliquando id mel, ridens civibus molestiae et nam.

Ea eam postea facilisi. Nullam forensibus consequuntur usu ea, no ius consul delectus periculis. Eam veri numquam an. Et partiendo gubergren eam. Quod iudicabit has ex, eam diam facilisi eu, elitr aliquip no eum.
