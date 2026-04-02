---
description: Manage your evergreen tweet queue
argument-hint: [status|add|history]
allowed-tools: [opentweet_get_evergreen_settings, opentweet_list_evergreen_posts, opentweet_add_to_evergreen, opentweet_update_evergreen_post, opentweet_remove_from_evergreen, opentweet_get_evergreen_history, opentweet_update_evergreen_settings]
---

The user wants to manage their evergreen queue. Their input: $ARGUMENTS

Based on user intent:

**Status (default):**
1. Get settings with `opentweet_get_evergreen_settings` and show queue status (enabled/disabled, posts per day, posting times, cooldown).
2. List pool posts with `opentweet_list_evergreen_posts` and show a summary.

**Add:**
1. If the user provides tweet text, use `opentweet_add_to_evergreen` with the text.
2. If the user wants to add existing posts, list drafts first, then add selected ones.

**History:**
1. Fetch history with `opentweet_get_evergreen_history` and show recent reposts.

Always explain what the evergreen queue does if the user seems unfamiliar: it automatically recycles your best tweets on a rotation with configurable cooldown periods.
