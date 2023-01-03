
# Nostrex

WARNING: Nostrex is still alpha software, has bugs, and will have backwards incompatible database changes. Do not use it for a production system.

## About

Nostrex is a Nostr relay written in Elixir using the Phoenix framework. It is designed to be highly scalable to handle the rapid adoption of the Nostr protocol. Nostrex has a number of qualities and features that make it a compelling relay implementation.

### Concurrency

The Erlang OTP gives us the primitives necessary to build high-throughput, concurrent high-uptime message routing software. The OTP has been hardened and optimized over decades and a single beefy server should be able to handle millions of concurrent connections.

### Database optimization

One of the major bottlenecks of scaling a relay are the database operations. Nostrex has already implemented a number of optimizations at the DB level, including partitioning by Event `created_at` timestamps to keep table sizes in check.

## Supported NIPS
- [X] NIP 01 Basic protocol flow description
- [ ] NIP 02 Contact List and Petnames
- [ ] NIP 04 Encrypted Direct Message
- [ ] NIP 09 Event Deletion
- [ ] NIP 11 Relay Information Document
- [ ] NIP 12 Relay Information Document
- [ ] NIP 15 End of Stored Events Notice
- [ ] NIP 20 Command Results
- [ ] NIP 40 Expiration Timestamp