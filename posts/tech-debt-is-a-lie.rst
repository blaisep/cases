.. title: tech debt is a lie
.. slug: tech-debt-is-a-lie
.. date: 2025-02-24 01:10:12 UTC
.. tags: Business, DevOps, Prose, Lean Production
.. category: 
.. link: 
.. description: Why Tech debt is not analogous to financial debt
.. type: text

How Technical debt differs from financial debt

The TL;DR with the tech tech metaphor is that devs don't understand the financial aspects of debt, so they can't describe the structure to the biz folks.



If I told my execs, "to meet this date, I'm going to borrow 4 sprints, payable over 2 releases at a defect rate of 15% per release." Then we could have a conversation.



Instead, the PM asks "what can we put off until it becomes someone else's problem?"

I answer, and everyone is happy.
For now.

We need to take on tech debt to get things done sometimes. The problem is that we don't record it anywhere. The bigger problem is that we don't have the practice of looking for it.

The current formula for successful  continuous delivery is: identify unplanned work, identify bottlenecks, reduce cycle time, reduce batch size.

We don't review the decision history. If we do, it's unlikely that the history will include what kind of tech debt we incurred.
Is it debt with compounding interest? (does it get worse as time goes by?)
Can it be transferred? (does it have to be addressed before someone else takes over?)
Will I get a margin call?  (Does it impact my confidence of success? )

So my concern is not that we take on tech debt.
It's that we pretend it disappears.


Towards a more nuanced understanding of tech debt
=================================================

What I'm about to say used to be a closely held secret, until I realized that it's a systemic vulnerability...
Now I tell everyone and use it as a litmus test to see how much they have thought about this problem.

So, _tech debt_ is a funny expression because it was invented by Ward Cunningham (I think) or someone equally unfamiliar with the different kinds  of financial debt (simple interest, compounded, fixed rate, variable, collateralized, subordinate....)

In effect, an org can incur tech debt without any de jure method to track it or ensure that it gets paid back. In financial terms, this is the equivalent of Enron moving their liabilities off of the balance sheet.
The financial accounting that is typically practiced within GAAP is cost accounting, which can represent investments in capital (depreciate the cost of a forklift over three years, so that you don't impact profits as much in a single year)
... but you can't depreciate investments in efficiency.
So if you spend 20 hours to reduce the cycle time from 24 hours to 90 seconds, that is an expense. There is no way to assign value to the orders of magnitude increase in productivity. (ask me how I know)

So, when a company needs to show profit in a short term, they can lay off all their research and creative people and reduce their expenses dramatically. The fact that they will not be able to innovate and that entropy will accummulate is a problem for someone in the future..

The ReForge article is better than most at describing the context of different kinds of debt. It would have been great if they had added something about the financial structure of different debts (kind of like we do with computational complexity).
This fellow moves in that direction: https://apenwarr.ca/log/?m=202306


