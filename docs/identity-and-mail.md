# Identity and Mail

Modula separates three concepts on purpose:

- Public identity
  - `handle`
  - `username`
  - `display name`
  - public-safe profile data
- Private mailbox
  - inbox
  - sent
  - drafts
  - private threads
- Credential email
  - sign-in
  - recovery
  - notifications

## Canonical identity route

The canonical public route is:

- `/identity/<handle>`

If a username alias is used and it differs from the handle, Modula resolves the identity and then canonicalizes the browser to the handle route.

## Handle vs username

- `handle`
  - public route key
  - preferred public reference
- `username`
  - alias or account-level identifier
  - can resolve to the same identity

Modula keeps `/profile` as the current-user compatibility route, but public identity should converge on `/identity/<handle>`.

## Public vs private surfaces

Public identity pages should expose only public-safe data:

- avatar
- display name
- handle
- public bio
- public module surfaces

Public identity pages must not expose:

- inbox
- drafts
- private threads
- credential email details

## Mail module basics

The Email module is identity-first:

- recipients can be resolved by handle
- recipients can be resolved by username
- recipients can be resolved by identity id
- email remains a compatibility fallback for external delivery

Core mail routes:

- `/mail`
- `/mail/inbox`
- `/mail/sent`
- `/mail/drafts`
- `/mail/compose`
- `/mail/thread/<id>`

## Messaging flow

Typical flow:

1. Search for an identity in compose.
2. Select the handle.
3. Save draft or send.
4. View the thread in Inbox or Sent.

Mail actions and workflows are also exposed through the execution layer, so Email can participate in the automation graph without allowing arbitrary package code execution.
