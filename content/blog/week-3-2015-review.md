+++
date = "2015-01-19T23:17:41-08:00"
draft = true
title = "week 3 2015 review"

+++

# W3 2015 review

## General Events

- I finally achieved my short-term goal of biking all the way from
  home to work. It's been my fear ever since I've taken a two-month
  trip to the Philippines that I "haven't got it in me" anymore, so
  it's nice to know that I'm strong enough again to take that 16 mile
  long bike ride.

- Tried mountain climbing for the first time. The first time you start
  getting high up the wall is really scary. Despite knowing there's
  someone there to catch you, there's that fear that anytime you slip
  up you'll fall down 10-15 feet down below.

## Work Events

- Me and a couple of my co-workers hacked on some of our side projects
  on a weekend. I chose to port our Android APK build script to a
  Dockerfile, so that building the APK would be as simple as
  installing Docker for their platform, then running `make`.

## Learnings

- Still learning FreeBSD on my spare time. FreeBSD has some simple IDS
  tools builtin to it. One of the builtin tools is called [mtree](),
  a file integrity checker. (Expand on mtree)

- Python has some pretty good builtin tools for discovering and
  running tests. It has great functions for
  [discovering](https://docs.python.org/2/library/unittest.html#unittest.TestLoader.loadTestsFromNames)
  [tests](https://docs.python.org/2/library/unittest.html#unittest.TestLoader.discover),
  as well as
  [running](https://docs.python.org/2/library/unittest.html#unittest.TestLoader.discover)
  those tests.
