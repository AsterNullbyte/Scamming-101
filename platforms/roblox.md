# Scamming-101: Roblox

## Opening

Roblox is weird. It's often seen as a "kids game," but the black market for Roblox accounts, Limiteds (tradeable items), and Groups is a multi-million dollar industry. Because the userbase is younger, scammers (often called **"Wannabe E-Gangsters"**) are ruthless, manipulative, and surprisingly technical.

They don't just want your Robux. They want your **Limiteds** (to sell for crypto), your **Groups** (to launder money), and your **Account Age** (older accounts are valuable).

I worked at roblox for a time (I won't get into all of that), to put it very frankly everybody that works at roblox is an undiagnosed sociopathic dickbag. Roblox does not care about you, they see you as flesh wallets to be exploited and their customer service should be demonstrative of that. You might notice that there's no "Help! I was hacked!" section here, and that's because you're going to need to pray to whatever god you believe in that they don't have ChatGPT answer your support ticket, which is going to politely tell you to fuck off lol.

---

## Security - Best Practices

Roblox security is a bit different from Steam or Discord. You need to lock down the **Settings** menu itself.

1.  **Enable 2-Step Verification (Authenticator App)**
    *   Go to `Settings` > `Security`.
    *   Turn on **Authenticator App** (Very Secure).
    *   **DO NOT** rely on Email 2FA alone. Email is the first thing hackers compromise.

2.  **The "Account PIN" (Parental Lock)**
    *   Go to `Settings` > `Parental Controls` (or Security in older views).
    *   **ENABLE THE ACCOUNT PIN.**
    *   **Why?** If a hacker gets into your account, the *first* thing they try to do is change your password, email, or disable 2FA. **They cannot do this without the 4-digit PIN.** This buys you time to kick them out.

3.  **Kill All Sessions**
    *   If you suspect *anything* is wrong, go to `Settings` > `Security` > `Log out of all other sessions`. Do this regularly.

---

## The "Cookie" Warning (.ROBLOSECURITY)

Before we talk about specific scams, you need to understand **HOW** Roblox hacks happen. 99% of Roblox hacks are **Cookie Logging**.

*   **The Cookie:** Your browser stores a file called `.ROBLOSECURITY`. This is your "Session ID."
*   **The Danger:** If a hacker gets this string of text, **they do not need your password.** They do not need your 2FA. They can simply copy-paste that cookie into their browser and **BECOME YOU** instantly.

> [!CAUTION]
> **NEVER** share your `.ROBLOSECURITY` cookie.
> 
> **NEVER** drag random buttons to your bookmarks bar.
> 
> **NEVER** send network files (`.HAR`) to anyone.

---

## Common Scams - Identifying & Avoiding

### 1. The ".HAR File" / GFX Artist Scam (The #1 Method)
This is the most dangerous scam targeting "rich" users right now.

*   **The Hook:** Someone DMs you (Discord/Twitter) claiming to be a GFX Artist. "Hey! I want to make a render of your avatar for free/for a commission!"
*   **The Trap:** They say: *"To get the high-quality textures of your avatar, I need you to export your character data."*
*   **The Method:** They send you a tutorial asking you to:
    1.  Right-click your Roblox profile.
    2.  Click "Inspect Element".
    3.  Go to the **Network** tab.
    4.  Right-click and "Save as HAR with Content" (or `.har` file).
    5.  Send them the file.
*   **The Scam:** The `.HAR` file contains **EVERYTHING** your browser sent to Roblox, including your **.ROBLOSECURITY Cookie**. They load the file, find the cookie, and yoink your account.

> [!NOTE]
> **Real GFX artists DO NOT need this.** They only need your User ID or Username. They can import your avatar into Blender using plugins solely with your public username.

### 2. The "Bookmarklet" / JavaScript Scam
You see a YouTube video or TikTok: *"HOW TO GET FAKE HEADLESS / FREE ROBUX / AUTO-TRADER BOT"*

*   **The Trap:** They ask you to drag a button (or a piece of code) to your browser's **Bookmarks Bar**.
*   **The Method:** When you are on the Roblox website and click that bookmark, it executes a JavaScript command.
*   **The Scam:** The code instantly scrapes your `.ROBLOSECURITY` cookie and sends it to a Discord webhook owned by the scammer. You lose everything instantly.

### 3. The "Projected" Item Trade Scam
This targets traders.

*   **The Mechanics:**
    *   **RAP:** Recent Average Price (The graph on the item page).
    *   **Value:** What the item is *actually* worth to people.
*   **The Scam:**
    1.  A scammer takes a trash item (worth 100 Robux).
    2.  They buy their own item on an alt account for 100,000 Robux.
    3.  The "RAP" graph spikes to 100k.
    4.  They offer to trade this "100k" item for your legitimate limited (worth 50k).
    5.  You accept, thinking you made profit.
    6.  **Reality:** The item drops back to 100 Robux the next day. You traded a real limited for trash.
*   **The Fix:** Always use **Rolimons.com** to check the *true value* of an item. Never trust the Roblox RAP graph blindly.

### 4. The "Roblox Support" / "Revert Trade" Form
Someone messages you: *"I accidentally reported you for scamming! To prove you're innocent, fill out this Google Form / appeal on this website."*

*   **The Trap:** The website looks like Roblox Support.
*   **The Scam:** It asks for your username, password, and then asks you to "Paste your authentication ticket" (which is usually code for your Cookie or a 2FA code).
*   **Reality:** Roblox Support **ONLY** exists at `roblox.com/support`. They will never DM you. (It's already hard to get a non-bot reply, what makes you think they're gonna dm you unless they're looking for their money lol)

### 5. Cross-Trading / Trust Trading
*   **The Deal:** "I will give you a $50 gift card for your Adopt Me Pets." / "I will give you CS2 skins for your Limiteds."
*   **The Scam:** One person has to go first. If you go first, they block you. If they go first, the gift card is often stolen/fake.
*   **The Risk:** Cross-trading is against Roblox ToS. If you get scammed, Roblox will **NOT** help you, and might even ban you for attempting it.

### 6. "Test My Game" (Console Paste)
A friend or dev asks you to test their game. They say: *"The game is bugged, press F12 and paste this code in the Console to fix the textures."*

*   **The Scam:** The code is a script that grabs your cookie and sends it out. **NEVER PASTE CODE INTO THE BROWSER CONSOLE.**

---

## Technical Visual: The .HAR Scam
This is how they trick you into handing over the keys to the castle.

```mermaid
flowchart TD
    Start(["'GFX Artist' DMs you"]) --> Request{"'I need your<br/>Texture Data'"}
    
    Request --> Method["'Right Click > Inspect > Network'"]
    Method --> File["'Export as .HAR file'"]
    
    File --> Send["You send the file"]
    Send --> Extract["Scammer opens file<br/>Finds .ROBLOSECURITY"]
    
    Extract --> Login["Scammer uses 'EditThisCookie'<br/>to inject your session"]
    Login --> Beam["<b>ACCOUNT WIPED</b>"]
    
    style Start fill:#f9f,stroke:#333
    style Beam fill:#ff9999,stroke:#f00
    style Request fill:#ffffcc,stroke:#333
