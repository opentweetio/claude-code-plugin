---
name: twitter-management
description: This skill should be used when the user asks about tweets, scheduling posts, Twitter/X management, social media content, posting analytics, evergreen queues, or anything related to their X/Twitter presence.
version: 1.0.0
---

# Twitter/X Management with OpenTweet

You have access to OpenTweet MCP tools for managing the user's X/Twitter presence. Use these tools to help with tweet creation, scheduling, analytics, and content management.

## Available Tools

### Content Creation
- **opentweet_create_tweet** — Create a single tweet (draft, scheduled, or publish immediately)
- **opentweet_create_thread** — Create a multi-tweet thread (2-25 tweets)
- **opentweet_update_tweet** — Edit an existing draft or scheduled tweet
- **opentweet_delete_tweet** — Permanently delete a tweet

### Scheduling
- **opentweet_publish_tweet** — Publish a draft immediately to X
- **opentweet_batch_schedule** — Schedule up to 50 tweets at once with specific dates/times

### Analytics
- **opentweet_get_analytics** — Get posting stats, streaks, trends, and category breakdowns. Use `type: "best_times"` to find optimal posting hours.

### Evergreen Queue
- **opentweet_get_evergreen_settings** — Check queue configuration
- **opentweet_list_evergreen_posts** — See posts in the rotation pool
- **opentweet_add_to_evergreen** — Add a post to automatic rotation
- **opentweet_update_evergreen_post** — Adjust cooldown or pause/resume posts
- **opentweet_remove_from_evergreen** — Remove from rotation (converts back to draft)
- **opentweet_get_evergreen_history** — View what was automatically reposted

### Account
- **opentweet_get_account** — Check subscription, limits, and post counts
- **opentweet_list_accounts** — List connected X accounts (for multi-account users)

## Guidelines

- Always show the user the tweet text before publishing. Never publish without confirmation.
- When scheduling, suggest optimal times using `opentweet_get_analytics` with `type: "best_times"`.
- For threads, ensure each tweet is under 280 characters (unless user has Premium+).
- Use categories to organize content (e.g., "Tech", "Marketing", "Personal").
- When creating multiple tweets, use `opentweet_batch_schedule` for efficiency.
- For multi-account users, ask which account to use or check with `opentweet_list_accounts`.
