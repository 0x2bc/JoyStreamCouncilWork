**Situation**: There is an unspent WG’s budget for the previous term. WG’s Lead spent this budget in the next term. 

**Result**: According to the current flow, the Council will get slashed by the JSGenesis because the total amount of budget spent is more that the total amount of the budget refilled. 

**How to mitigate the risk?** 
Basically, there are two options:
1.	Change the current flow
2.	Create a control that will be triggered once the unfavorable situation is about to happen (create discord bot)
Let’s focus on the 2nd option.

I would suggest to create a Discord Bot in the Council channel 

**Requirements:**
1. Fire a notification once the WG Lead spent more than it was allocated for the current term
- Notification should contain the following info:
     - Name of the WG
     - Amount of Joy that was refilled this term
     - Amount of Joy that was spent this term
     - WG’s budget at the beginning of this term
   1.2. Bot should be muted for the first 3 days of the Council term. I believe, this time is enough for the Council to initially refill all WG’s budgets.
2. Fire a notification once it’s probable that WG’s budget will not be spent in full. 
- Criteria: 
     - Only one budget distribution left. This happens at the last date of the term.
     - [refilled amount] – [proposed spent amount for the whole term] >  [refilled amount * 5%]
- Notification should contain the following info:
     - Name of the WG
     - Proposed total amount of Joy to be distributed
     - Current amount of Joy unspent for this term (=refilled-spent)
