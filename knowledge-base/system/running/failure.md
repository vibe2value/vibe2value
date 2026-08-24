[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Running](README.md) / Failure

# Failure

> Status: the method below is written. PROJECT_NAME's answer is not filled in yet.

**Question this file answers:** How does a failure surface and with what context attached?

In a system built from separate parts, failures are not rare events. They are a normal part of how it runs. What a part does when it cannot finish is a design decision rather than something to leave to chance. The two obvious answers are both wrong. Hiding it lets a wrong or empty answer reach the end with nobody knowing there is anything to question. Stopping everything throws away all the work the other parts did correctly.

The rule underneath is narrow. Recover what can be recovered quietly. Report the rest. Even then, report with the full record rather than empty handed, because a handoff with no context makes the next person start from nothing.

## What to write down

### Where a failure shows up

Name the places. A log, an alert, a status field, a line in the output someone actually reads. A failure with nowhere to appear gets found by a user.

### What travels with it

A report worth acting on says three things: what was being attempted, anything that was managed before it stopped and what to try instead.

### How the status travels separately from the result

The payload and the status are two different facts. Whether the operation succeeded has to come back in its own channel rather than being inferred from the answer looking empty. An empty result can be the honest answer to a question with nothing to find. A result that arrives can still be partial or stale.

### Which kinds of failure this project distinguishes

The kind decides the next move, so the kinds have to be named. A rate limit means wait and retry. A bad credential means fix it rather than retry. The service being down means go somewhere else. List the ones PROJECT_NAME actually sees.

### How a gap is marked when results are combined

A tidy summary can hide that part of the evidence never arrived. Say which parts are well supported and which are thin because something was missing, so looks-good is never mistaken for is-good.

## The check

**Pass:** you can point at where each kind of failure appears and say what a person or an AI is handed to work from when it does.

**Fail:** any failure whose only symptom is that the answer looks wrong.

## PROJECT_NAME's answer

Fill this in.
