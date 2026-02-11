# Scamming-101: Steam

## Opening

Steam is the biggest storefront for PC gaming, which makes it the biggest target for scammers. Unlike Discord, where they usually just want your account to spam others, on Steam, they want your **money**. They want your skins, your trading cards, and your wallet balance.

If you have an inventory worth more than $5, you are a target.

---

## Security - Best Practices
Steam has some very specific security features that you absolutely **MUST** use.

1.  **ENABLE STEAM GUARD (Mobile Authenticator)**
    Do not use Email verification. Email is easily compromised. Download the Steam App on your phone and set up the Mobile Authenticator. This generates a code every 30 seconds that is required to log in.

>[!WARNING]
>**NEVER** disable your steam guard for any reason. You are infinitely more secure with it on than off.

3.  **Check your API Key Status**
    
    Go to `https://steamcommunity.com/dev/apikey`.
    *   **Safe:** It asks you to register a domain name (The box is empty).
    *   **DANGER:** There is already a key generated that you did not make. **REVOKE IT IMMEDIATELY.**

> [!WARNING]
> If a scammer gets your API key, they can cancel your legitimate trades and send identical offers to their own bots without you noticing. **Most users do not need an API key.** If you have one and don't know why, delete it.

4.  **Inventory Privacy**
    If you are not an active trader, set your Inventory to `Friends Only` or `Private`. Scammers use bots to scan public inventories for high-value items (Knives, Gloves, expensive TF2 hats) and target those users specifically.

---

## DM Scams - Identifying
Steam scams often start on **Discord** or via Steam Chat from a compromised friend.

### 1. "I reported you by accident"

This is the most common scam currently in circulation.
*   **The Hook:** A random person (or a friend) DMs you saying: *"Hey, I'm sorry, I accidentally reported your account for [Illegal Purchase / Duped Items] and the Admin said you're going to get banned."*
*   **The Line:** They tell you to add a specific user on Discord (who claims to be a Valve Employee) to "appeal" the ban.
*   **The REEL TRUTH:** **Valve employees will NEVER DM you on Discord.** They will never ask you to trade your items to a "verification bot" to prove they aren't duped.
>[!NOTE]
>Valve will simply take your items away if they're not legitimate or contact you with a bright yellow popup on steam that you can't close without acknowledging it if there's a problem.

### 2. "Vote for my Team" / "Join my Tournament"

A friend sends you a link: *"Hey bro, my CS2 team is one vote away from entering the finals, can you vote for us?"*
*   **The Trap:** The link leads to a phishing site that looks *exactly* like Steam. It asks you to sign in to vote.
*   **The Scam:** You just gave them your username, password, and Steam Guard code. They now own your account.

### 3. The "API" / "Middleman" Trade Scam

You are trying to trade an item. The other person says they don't trust you and wants to use a "Middleman" or a "Verification Site."
*   **The Trap:** They ask you to trade your item to a "Bot" to check if it's clean.
*   **The Scam:** There is no bot. You are trading your item to the scammer's alt account. Once you send the item, you will never see it again.

### 4. The "I'm Quitting" / Free Items Scam
You see a post on Reddit or get a DM: *"I'm quitting CS2/TF2, take my whole inventory!"*
*   **The Hook:** Greed. They offer you expensive skins for free.
*   **The Trap:** They ask you to send them a trade offer for the items you want, or click a link to "Claim" them.
*   **The Scam (Two Possibilities):**
    1.  **API Hijack:** You send a trade offer asking for their items. Their bot (using your compromised API key) **cancels** that offer instantly and sends a **new** offer that looks identical, but this time **YOU are giving them YOUR items.**
    2.  **Poisoned Items:** On the rare chance they *do* send you items, they are likely stolen ("poisoned"). If you accept them, Steam Support may flag your account for involvement in a scam network and Trade Ban you.
