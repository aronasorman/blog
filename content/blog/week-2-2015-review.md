+++
date = "2015-01-14T05:01:56-08:00"
title = "week 2 2015 review"

+++

# W2 2015 review

## Work events

- Tons of new interns. 17 by the last count. I'm extremely skeptical
  of how they're gonna be handled, but this should be a learning
  experience both for them and us as well.
- I've realized that a big factor of my burnout during December was
  how little programming I actually accomplished each day. This
  stemmed from the frequent interruptions I got when I programmed. So
  we've made a commitment to try and group all the "meetings" into
  MWF, and leave TTh for "productive work" such as programming. See
  the [maker's schedule](http://www.paulgraham.com/makersschedule.html).


## Learnings

- I've been working on the
  [Matasano Crypto Challenge](http://cryptopals.com/). I'm in set 1
  challenge 6. Part of the challenge was to implement the Hamming
  Distance for two strings, and to implement that I had to learn how
  to count the "on" bits in a byte. I realized then that I had very
  little bit-flipping knowledge, so I looked up how to count bits, and
  encountered
  [Brian Kernighan's bit-counting algorithm](http://stackoverflow.com/questions/12380478/bits-counting-algorithm-brian-kernighan-in-an-integer-time-complexity).

- It was the first time I used Git's [reflog](http://git-scm.com/docs/git-reflog) feature in the
  wild. Glad to have finally used it by helping a co-worker restore
  their tree to a state before a fast-forward.

- I've started experimenting with FreeBSD on my downtime after work,
  by installing the
  [VMWare image](ftp://ftp.freebsd.org/pub/FreeBSD/releases/VM-IMAGES/10.1-RELEASE/amd64/Latest/)
  and reading the
  [FreeBSD handbook](https://www.freebsd.org/doc/handbook/). The
  handbook is a treasure trove of of Unix command line knowledge. Some
  things I learned just by reading it:

    - The executable permission for a directory means it can be `cd`'ed. Never knew about this 'til today.

    - Nor did I learn the full symbolic permissions syntax used by `chmod` 'til now.


  So far it's been experimentation with the VM for now, but one
  milestone I'm looking to reach is to be able to do some work-related
  programming in FreeBSD eventually, and at least be able to know the
  nuances of FreeBSD to be able to use it effectively as a server.
