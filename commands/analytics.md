---
description: View your X/Twitter posting analytics and insights
argument-hint: [overview|best-times|tweets]
allowed-tools: [opentweet_get_analytics, opentweet_get_account]
---

The user wants to see their Twitter/X analytics. Their input: $ARGUMENTS

1. First, get account status with `opentweet_get_account` to show subscription info and post counts.
2. Based on user input:
   - If "best-times" or "best times": use `opentweet_get_analytics` with `type: "best_times"` and present optimal posting hours/days.
   - If "tweets": use `opentweet_get_analytics` with `type: "tweets"` to show per-tweet engagement.
   - Otherwise (default "overview"): use `opentweet_get_analytics` with `type: "overview"` to show stats, streaks, trends, and categories.
3. Present the data in a clear, readable format with key highlights.
4. Offer actionable suggestions based on the data (e.g., "Your best posting day is Tuesday at 9am").
