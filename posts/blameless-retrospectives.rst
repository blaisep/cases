.. title: Blameless Retrospectives
.. slug: blameless-retrospectives
.. date: 2025-02-24 01:00:21 UTC
.. tags: Prose, DevOps, Lean Production
.. category: 
.. link: 
.. description: Towards psychological safety
.. type: text



Refactor the code review
========================

When a Code review is a dialog between humans about their opinions of the code, it threatens psychological safety. The value scales inversely with the number of lines of code.

A better approach is to crank up the (static and dynamic) analysis tools and discuss the results. This way the review becomes an exchange of observations about the linting rule and a comparison of metrics with pervious versions of the work.

This approach aligns with "red-green-refactor", where we use a suite of acceptance tests to determine that our changes do not break behavior. This strategy also facilitates distributed reviews, improving shared understanding.


In a similar way, incident analysis and retrospectives are less threatening if the discussion is around comparing metrics rather than human actions.

**Bad:**
During the incident, the ops team had to wait 30 mins to get a response from the on-call engineer. We must crucify Blaise.

**Better:**
Prior to the incident, the running min/max/avg on-call response was 2/34/12 minutes. We can reduce the deviation by the call routing and escalation criteria.

**Bad:**
Blaise merged a commit last night that included a misspelled hostname. The resulted in dns timeouts in production, impacting customer experience. Blaise will be reassigned to new-hire training.

**Better:**
Prior to last night's change p99 dns lookups resolved in less than 100ms