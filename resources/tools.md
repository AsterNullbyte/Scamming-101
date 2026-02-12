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

I also hear you saying *"But Aster, I spent too much on my fansly subscription to femboygroiper69 and I'm broke. What other options do I have?"* 

To that, I say **NOT TO WORRY**. Bitwarden has a **FREE 2FA MOBILE APP**. Everybody can use it, and it will link with your account. I'm not going to explain it, as their documentation does a very good job explaining the pros and cons [here](https://bitwarden.com/help/bitwarden-authenticator/).

---

## Adblocking
Stop clicking on "Download" buttons that are actually ads.

### uBlock Origin
**NOT "uBlock"**. You want **uBlock Origin**.
This is the only adblocker that matters. 
*   **Why?** Scammers use "Malvertising" (Malicious Advertising). They buy ads on Google that look like the real download link for OBS, VLC, or Steam.
*   **The Fix:** uBlock Origin deletes these ads from existence. It blocks popups, trackers, and crypto-miners.

>[!IMPORTANT]
>This is free, lightweight and is avalible in EVERY browser as an extension. You have no reason not to be using this.

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
