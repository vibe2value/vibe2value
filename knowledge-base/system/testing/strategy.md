[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Testing](README.md) / Testing strategy

# Testing strategy

> Status: the method below is written. PROJECT_NAME's answer is not filled in yet.

**Question this file answers:** What do we test, at what level and what do we deliberately not test?

Two halves, the second of which usually goes unwritten. Saying what is not tested turns a gap into a decision. Left unsaid it stays a gap that everyone assumes someone else covered.

The test runner itself is recorded with the rest of the stack in [`../architecture/stack/`](../architecture/stack/README.md). This file is the approach rather than the tool.

## What to write down

### What is tested and at what level

Group by level rather than by file. What is checked in isolation, what is checked with the pieces joined up and what is checked end to end the way a user meets it. Say which single path is the one that is never allowed to go stale.

### What is deliberately not tested

Name it and give the reason. Performance because the load is not realistic yet. Styling because there is nothing stable to protect. Anything out of scope because it was never built. A reason makes it a decision that can be revisited rather than an oversight nobody owns.

### How each check can be made to fail

For every check, say what breaking it deliberately looks like. A check that cannot be made to go red is not a check. It is a green light wired to nothing. That is worse than having no check at all, because it turns something unknown into a false assurance.

The cheap version of this is a habit rather than a document: break the thing on purpose once, confirm the check goes red, then put it back.

### What is done about false positives

One noisy check makes people ignore all of them, accurate findings included. Trust like that is slow to earn back. Say how a noisy category gets handled: switched off and fixed properly rather than left spraying noise, plus what each finding reports about why it fired, so noise can be grouped and suppressed rather than endured.

### What is done about a check that comes back short

The opposite failure and the harder one to see. A check that finds four things where there were forty does not look broken, it looks like an answer, so the looking stops. Say what would be invisible to each check and where a second reading from a different direction comes from.

### When the checks run

On a change, before a promotion between environments, on a schedule. Tie this to [`../environments/deploy.md`](../environments/deploy.md) so it is clear which checks can stop a release.

## The check

**Pass:** for every check you can say how to make it go red. What is not tested is written down as a choice with a reason.

**Fail:** a check nobody has ever seen fail, or an answer that amounts to "we test everything".

## PROJECT_NAME's answer

Fill this in.
