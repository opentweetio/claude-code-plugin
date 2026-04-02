---
description: Review and schedule your draft tweets
argument-hint: [number of days to plan]
allowed-tools: [opentweet_list_tweets, opentweet_get_analytics, opentweet_batch_schedule, opentweet_update_tweet]
---

The user wants to review and schedule their draft tweets. Their input: $ARGUMENTS

1. Fetch drafts with `opentweet_list_tweets` using `status: "draft"`.
2. If no drafts exist, let the user know and suggest creating some.
3. Get optimal posting times with `opentweet_get_analytics` using `type: "best_times"`.
4. Present the drafts in a numbered list showing the text and category.
5. Propose a schedule spreading tweets across the requested time period (default: 7 days) at optimal times.
6. Ask the user to confirm or adjust the schedule.
7. Once confirmed, use `opentweet_batch_schedule` to schedule all at once.
