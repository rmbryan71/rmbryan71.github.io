# Why Your Password Manager Company Can't See Your Passwords

## The Idea
When you store 80 passwords with a company like Dashlane or 1Password, those companies genuinely cannot read them — not because of a policy, but because of mathematics. Understanding why that's true, and when it isn't, is one of the most practically useful things a non-technical person can learn about how the internet works.

## Why It's Interesting
"Encryption" is one of the most used and least understood words in technology. Most people assume it means "the company promised not to look." In reality, a well-designed password manager uses end-to-end encryption, which means the data is scrambled before it ever leaves your device, using a key derived from your master password that the company never has. This is a meaningful distinction — and it's why forgetting your master password can mean losing your data forever.

## Key Points to Cover
- What encryption means in plain terms: scrambling data so only someone with the right key can read it
- The difference between "encrypted in transit" and "encrypted at rest" and "end-to-end encrypted"
- Why the master password is the key — and why the company doesn't store it
- What "zero knowledge" architecture means: the company can't help you if you forget your password because they genuinely don't know it
- When this protection doesn't apply: if someone gets into your unlocked device

## Potential Visuals
- Diagram: data leaving your device already scrambled → company stores scrambled data → only your key unscrambles it
- Comparison: a bank (can access your account) vs. a password manager (mathematically cannot)
- Lock-and-key illustration showing the master password as the only key that exists

## Notes / Open Questions
- Avoid going deep into cryptographic algorithms — the concept is what matters
- The "they can't help you if you forget" detail is the most counterintuitive and important practical consequence to land clearly
- Good hook: "The company you pay to store your passwords has never seen a single one of them"
