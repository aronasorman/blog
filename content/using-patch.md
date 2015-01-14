+++
date = "2015-01-13T08:35:28-08:00"
draft = true
title = "using patch"

+++

# The problem of slow tests

One thing that has been irking me since the start of my work in
[KA Lite](https://github.com/learningequality/ka-lite.git) is how slow
tests have been running. We use the free tier of Travis and often a
full run of the test suite can take upwards of 20-30 minutes, from
first push to the main repo up until the email from Travis. Part of
that is due to the queue in Travis' free tier, but a huge chunk of
that is simply our test suite.

The KA Lite codebase started out having no tests, and the easiest way
to add them is to use browser tests to test out the functionality of
completed features. Running browser tests however, takes a very long
time. For a person trying to introduce a testing culture into the
organization, this is one my main blockers.

Recently I've been working on a Django command that had to download a
moderately sized json file from the internet. The download took ~10
seconds on a good run, which, if we had to do on our test suite would
add even more time to an already long test run.

So at first, while writing the test I've tried caching the download in
the command itself:

In management/commands/parse_json.py:
```
    assessment_items_url = "https://s3.amazonaws.com/uploads.hipchat.com/86198%2F624195%2FtYo7Ez0tt3e1qQW%2Fassessmentitems.json"

    # cache the assessmentitems
    assessment_items_cache_path = os.path.join(settings.PROJECT_PATH, "assessmentitems.cache.json")
    if os.path.isfile(assessment_items_cache_path):
        assessment_items = json.load(open(assessment_items_cache_path))
    else:
        assessment_items = json.loads(requests.get(assessment_items_url).content)
        json.dump(assessment_items, open(assessment_items_cache_path, "w"))
```
