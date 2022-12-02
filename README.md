Bugs

- [ ] Scale rather than fly reply box
- [ ] Listener on notes view not adding notes
- [ ] Pin joined relays at the top
- [ ] Load/publish user preferred relays
- [ ] Optimistically load events the user publishes (e.g. to reduce reflow for reactions/replies). Essentially, we can pretend to be our own in-memory relay.

Features

- [x] Chat
- [x] Threads/social
- [ ] Search
- [ ] Link previews https://github.com/Dhaiwat10/svelte-link-preview, https://microlink.io/sdk
- [ ] Images
- [ ] Followers, blocking
- [ ] Notifications
- [ ] Server discovery
- [ ] Favorite chat rooms

Nostr implementation comments

- [ ] It's impossible to get deletes for an event's replies/mentions in one query, since deletes can't tag anything other than what is to be deleted.
- [ ] Recursive queries are really painful, e.g. to get all notes for an account, you need to 1. get the account's notes, then get everything with those notes in their tags, then get deletions for those.
- [ ] The limit of 3 channels makes things difficult. I want to show a modal without losing all the state in the background. I am reserving one channel for one-off recursive queries.
- [ ] Why no spaces in names? Seems user hostile