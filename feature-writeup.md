# IAM Permissions Explorer
 
### Solution
 
Three screens that cover the full lifecycle of a permission: granting it, monitoring it, and cleaning it up.
 
### Screen 1 - Smart Granting (Prevent)
 
Instead of digging through IAM docs, the admin just types what the user needs to do in plain english. Something like "deploy containers to EKS and read from S3 production bucket." An AI engine then suggests the minimum policies needed. Each policy gets a risk tag (low, medium, high, critical) and high-risk ones show a short warning explaining what makes them dangerous. This turns a 20-minute research task into a 2-minute thing.
 
### Screen 2 - IAM Overview Dashboard (Spot)
 
A single view that shows all users across cloud accounts with their roles, attached policies, risk scores, and when they were last active. Over-permissioned users get flagged. You can filter by risk level, cloud account, team, or activity. Basically gives the admin one place to see their entire IAM situation at a glance instead of only checking during audits.
 
### Screen 3 - Audit and Cleanup (Fix)
 
Compares what permissions each user was given vs what they actually used over the last 90 days (configurable). Groups everything into three buckets: never used, rarely used, and actively used. Each unused or risky policy has a one-click revoke button. There's also a bulk "revoke all unused" option. The screen is always accessible, with configurable reminders (monthly/quarterly) that nudge the admin to come check it.
 
### Prioritization
 
Screen 1 first because it fixes the root cause. If you grant the right permissions from the start, the cleanup problem shrinks on its own. Screen 2 second because you need to see the problem before you can fix it. Screen 3 third because it handles the backlog of bad permissions that already exist.
 
### Success Metrics
 
- Reduction in average permissions per user (are we actually reducing over-provisioning?)
- How often admins use the AI suggestions vs manually picking policies (is the tool being adopted?)
- Number of unused or risky policies revoked per audit cycle (is cleanup happening?)
- Time from access request to permission granted (is the process faster now?)
### Development Discussion Points (Bonus)
 
- Start with AWS first, add GCP and Azure support later
- Pull usage data from CloudTrail to track which permissions users actually call
- Build ready-made permission templates for common roles like developer, data analyst, and DevOps engineer so the AI has good starting points
- Add Slack or email notifications for audit reminders
---
