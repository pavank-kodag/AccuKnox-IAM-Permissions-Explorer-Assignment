# Problem Statement and User Persona
---
## Problem Statement
 
In most small to mid-size teams, the person handling cloud access isn't an IAM specialist. They're usually a tech lead or someone senior who does it along with their actual job. When a developer asks for access to some service, the admin can either spend 20-30 minutes going through IAM docs to find the exact right policies, or just give broad access in 30 seconds. In practice, speed always wins.
 
This leads to most users having way more permissions than they actually need. Over time this builds up into unnecessary security risk, compliance gaps, and sometimes random billing spikes that nobody connects back to IAM until something actually breaks.
 
The real problem isn't that people don't care about security. It's that doing things the right way takes too long compared to just giving full access to someone you trust.
---
## User Persona
 
Rahul, Tech Lead at a 30-person SaaS startup
 
Manages AWS access for about 8-12 developers on top of his actual engineering work. He knows cloud infra well enough but IAM isn't really his thing. When someone needs access, he checks if the request makes sense and then just attaches a broad policy because finding the exact right permissions feels like too much effort. He knows it's not great practice but the team moves fast and everyone trusts each other. His main frustrations: he has no idea which permissions are actually being used vs just sitting there, he can't easily tell who's over-permissioned, and he's worried about the day a security incident or audit forces him to sort through months of messy permission grants.
 
 
---
