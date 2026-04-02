---
description: Create and schedule a tweet on X/Twitter
argument-hint: <topic or text>
allowed-tools: [opentweet_create_tweet, opentweet_get_analytics, opentweet_list_accounts]
---

The user wants to create a tweet. Their input: $ARGUMENTS

Follow these steps:

1. If the user provided a topic (not a full tweet), draft 2-3 tweet variations for them to choose from. Keep each under 280 characters.
2. If the user provided exact tweet text, use it as-is.
3. Ask the user if they want to:
   - Save as draft
   - Schedule for a specific time (suggest optimal times using `opentweet_get_analytics` with `type: "best_times"`)
   - Publish immediately
4. Create the tweet with `opentweet_create_tweet` based on their choice.
5. Confirm the action with the tweet text and status.
