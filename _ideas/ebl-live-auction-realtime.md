# Eight People, One Browser, Zero Lag: How the Live Auction Works

## The Idea
During the EBL draft, eight teams are bidding simultaneously in a web browser — and every bid shows up on everyone's screen within seconds, without anyone hitting refresh. How does a website do that?

## Why It's Interesting
Most websites work like a vending machine: you make a request, it gives you something back. Live auctions need something different — the website has to push information to you the instant it changes. The technology that makes this work (called Server-Sent Events) is the same kind of thing behind live sports scores, stock tickers, and collaborative editing tools like Google Docs. The auction is a fun, concrete way to explain a concept that's everywhere.

## Key Points to Cover
- The normal web model: you ask, the server answers (request/response)
- The problem with auctions: you need updates you didn't ask for
- How Server-Sent Events work: an open "pipe" from server to browser that stays connected
- What flows through the pipe during an auction: current bid, time remaining, who's up next, everyone's budget
- What happens when someone's internet cuts out and they reconnect — they get caught up instantly

## Potential Visuals
- Diagram: normal web request vs. SSE "open channel" — side by side
- Illustration of 8 browsers all receiving the same stream from one server
- Animated-style sequence showing a bid placed → server updates → all screens update

## Notes / Open Questions
- Avoid getting too deep into HTTP — keep it at the "pipe" metaphor level
- The 15-second bid timer is a good hook: how do all 8 screens show the same countdown?
- Could briefly mention that this is different from WebSockets (but don't go deep)
