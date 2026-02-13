# Tools

## Opening
This section is more or less going to be a yap session out of me since not everything is going to be preventing scams, but general security. I am also writing this while drunk as FUCK, so I'll be going over this later with ChatGPT to clean up my spelling mistakes lol.

As usual, if you have any suggestions make a pull request with what you want to add.

---

## Account Security
Tools for keeping your accounts secured.

### Bitwarden
Everybody needs a **GOOD** password manager, and Bitwarden is just about the best shit you can get on the market. Listen to me, you don't need RaidVPN or Nord Shadow Legends with its built-in security suite. They overcharge you for that shit.

#### Bitwarden Premium is **TEN** dollars for a **YEAR**.
*(I originally wrote 20, but I checked, and it's literally 10 dollars. That is less than a single DoorDash order. You have no excuse.)*

You buy their premium plan for less than you'd spend on a monthly subscription like Netflix or Spotify. What do you get for $10 a year? 

*   **Integrated 2FA (TOTP) Generation:** This is the **BEST** feature that I use daily. You don't need to pull out your phone, open an app, find the code, and type it in. Bitwarden generates the code and copies it to your clipboard automatically when you auto-fill your password. It is pure laziness, but it keeps you secure.
*   **YubiKey / FIDO2 Support:** You want to use a physical hardware key to lock your vault? You need premium. This makes your passwords un-hackable unless they physically steal your key. (I use a Google Titan key—same principle. Google literally can't track me with that because that's not how FIDO works, but they definitely upcharged me for the brand lol).
*   **Vault Health Reports:** It scans the dark web for you. It tells you *"Hey, idiot, you used the password 'puppyboy123' on 50 different sites and 4 of them were breached."*
*   **Emergency Access:** If you get hit by a bus (god forbid you play in the road **ONE** time), you can set a trusted contact who can request access to your vault. If you don't deny it within X days, they get in. This saves your family from being locked out of your digital life.

**JUST DO IT.** It supports open-source developers and secures your entire life.

I also hear you saying *"But Aster, I spent too much on my fansly subscription to femboygroyper69 and I'm broke. What other options do I have?"* 

To that, I say **NOT TO WORRY**. Bitwarden has a **FREE 2FA MOBILE APP**. Everybody can use it, and it will link with your account. I'm not going to explain it, as their documentation does a very good job explaining the pros and cons [here](https://bitwarden.com/help/bitwarden-authenticator/).

>[!IMPORTANT]
>You ABSOLUTELY need a non-email based 2FA. If you do not wish for bitwarden's 2FA, I suggest you look into Google Authenticator or Microsoft Authenticator.

### Privacy.com
`privacy.com`
*(US Only mostly, sorry EU friends)*

Stop giving your real Debit Card number to sketchy sites. Privacy.com lets you make "Virtual Cards."
*   Want to sign up for a "Free Trial" that charges you if you forget to cancel?
*   Make a card on Privacy.com, set the limit to **$1**, and use that.
*   When they try to charge you $50, it declines. You win.

I LOVE privacy, I use it almost as much as bitwarden. I can spend my money on dumb shit without having to worry about my credit card getting charged 300 times at some indian market or whatnot. They also let you use ANY name and address you want, Privacy will respond that it's valid, so you can put in fake details if you want to be anonymous. The only caveat is that you have to provide them your actual information (KYC laws) but I would rather a company backed by an FDIC bank has my information rather than `totallynotascam.buy`

They offer a premium plan, but it's not necessary  here. I used it at one point, but cancelled my subscription as I didn't need it.

<details>  

<summary><b>Here's proof that I use what I advertise!</b></summary>
<img width="657" height="604" alt="image" src="https://github.com/user-attachments/assets/40ec265d-fbd4-4f1d-9687-b797e376627d" />

Blocked out are personal accounts (amazon, etc)

<img width="1863" height="946" alt="image" src="https://github.com/user-attachments/assets/4e31f6d1-de4b-4be4-ab00-b0678b5f2d5b" />

I have blocked out the login information for anything remotely identifiable. As of currently, I have about ~3000 logins stored after 5 years of usage.
  
</details>

---

## Adblocking
Stop clicking on "Download" buttons that are actually ads.

### uBlock Origin
**NOT "uBlock"**. You want **uBlock Origin**.
This is the only adblocker that matters. 
*   **Why?** Scammers use "Malvertising" (Malicious Advertising). They buy ads on Google that look like the real download link for OBS, VLC, or Steam.
*   **The Fix:** uBlock Origin deletes these ads from existence. It blocks popups, trackers, and crypto-miners.

>[!IMPORTANT]
>This is free, lightweight and is available  in EVERY browser as an extension. You have no reason not to be using this.

---

## File & Link Scanners
Stop downloading random `.exe` files and praying to god. Use these.

### VirusTotal
`virustotal.com`

Before you open *any* file you downloaded from a friend, Discord, or a shady site:
1.  Go to VirusTotal.
2.  Upload the file.
3.  It scans it with **70+ different antiviruses** at once.

> [!TIP]
> **How to read the results:**
> *   `0/70`: You are probably safe (unless it's brand new malware).
> *   `1/70` or `2/70`: Usually "False Positives" (Game cracks often trigger this). Be careful, but it might be okay.
> *   `5/70` or higher: **DELETE THAT SHIT IMMEDIATELY.**

### Tria.ge (For the advanced users)
`tria.ge`

If VirusTotal is for checking if a file is known malware, Triage is for checking how a file behaves. The technical term is a sandbox. You upload the file, and it opens it inside a virtual machine on their server so you can watch what happens.

* **Does it try to steal cookies?**
* **Does it try to connect to a Russian IP address?**
* **Does it upload me to your computer? >///<**

Tria.ge will tell you. (Maybe not if you downloaded a vtwink, but the other two it will!)

### HaveIBeenPwned
`haveibeenpwned.com`

Put your email in here. Right now.
It will tell you every single database breach your email has been found in.
*   If you see a breach from 2018 (e.g., MyFitnessPal), and you haven't changed your password since 2018... **CHANGE YOUR PASSWORD.**
*   Hackers take these old lists and try the email/password combos on every other site (Steam, Discord, Netflix). This is called "Credential Stuffing." Don't be a victim of lazy password reuse.

## Network Defense (DNS)
You know how you type `google.com` and your computer finds the IP address?

That's DNS. I could go more indepth about it but basically its a central registry that your computer asks "what's the IP address of google?" it responds with "oh yeah here's google's IP address", since your computer does not read "google.com" it only understands google's IP address (which is why when your internet goes down you see a DNS error).

Most people use their ISP's default DNS, which means your ISP (Comcast/AT&T) tracks every site you visit, and they don't block anything. They also sell off your data, and will openly hand it to the authorities without a warrant!

### Quad9
`quad9.net`

Quad9 is a free DNS provider. If you try to go to a known malware or phishing site, Quad9 just says "na fam" and blocks the connection. It is literally a condom for your internet connection.

**How to set it up:**
It takes 2 minutes. You don't need to install software.
*   **Windows:** Settings > Network & Internet > DNS > Manual.
*   **The Magic Numbers:**
    *   **Preferred:** `9.9.9.9`
    *   **Alternate:** `149.112.112.112`

Set it once, and it protects you forever (or until you reinstall Windows).

