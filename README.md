Nocturn
=======

Nocturn is a structured and scalable alternative to Nostr, balancing decentralization with usability and moderation.

**Key Differences from Nostr**
- **Trackers for relay discovery**, similar to BitTorrent trackers.
- **Filtered requests** to prevent scraping/global timeline abuse.
- **Optional federation-like control** via trackers, allowing better network organization.

This is not another protocol, But rather an alternative attempt to fix Nostr's [NIP](https://github.com/nostr-protocol/nips).

Why is this created
-------------------

1. **Relay Fragmentation.** Clients must connect to multiple relays just to get a complete feed. Each relay is isolated, with no native relay-to-relay communication. If a major relay goes down, users lose access to content, even if it's still on other relays.
2. **Global Timeline is a Mess.** Bad actors can spam relays, making moderation almost impossible. No structured way to follow content without being exposed to random garbage.
3. **Relay Discovery is Unorganized.** Each app maintains a hardcoded relay list, leading to fragmented user experience. No decentralized method for clients or relays to discover each other automatically.
4. **No Content Safeguards.** Because everything is open, Nostr struggles with illegal content (CP, spam, scams). Relay operators have no efficient way to prevent this while staying decentralized.

How Nocturn Solves This
-----------------------

1. **Relay-to-Relay Communication.** Instead of clients connecting to 10+ relays, relays themselves sync with other relays. Clients only need one relay to get content from the network.
2. **Hashtag & Author-Based Feeds.** Instead of a global timeline, Nocturn only allows:
    - #tag feeds (for public topics).
    - authors feeds (for following users).
3. **Trackers for Relay Discovery.** Trackers act as relay directories (like BitTorrent trackers). Clients and relays can discover new relays without hardcoded lists.
4. **More Organized Decentralization.** Trackers allow optional federation, helping relay operators manage bad actors. Still fully decentralized, but with better control mechanisms.

The Core Philosophy of Nocturn
------------------------------
- **Decentralization without chaos** – No global timeline spam.
- **Scalability** – Relay interconnection makes data distribution efficient.
- **Usability** – Clients don’t need to configure multiple relays manually.
- **Moderation, but optional** – Trackers can ban bad relays, but users can still connect freely.

## NOC-XX

- [NOC-01](01.md) - Core
- [NOC-02](02.md) - Tracker system
- [NOC-03](03.md) - Relay to Relay communications
- [NOC-04](04.md) - Search Capability
- [NOC-05](05.md) - The `t` tag

## License

Public License.
