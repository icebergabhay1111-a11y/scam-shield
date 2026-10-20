# Scam Shield

**Check before you pay, share or panic.** Scam Shield reads a WhatsApp forward or SMS, or listens to a call on speaker, and warns you the moment it looks like a scam. It explains exactly which lines gave it away and tells you what to do next, in **English, Hindi or Tamil**.

## What it catches

| Scam | Example red flags it spots |
|---|---|
| **Digital arrest** | "CBI / crime branch / customs", "arrest warrant", "stay on video call", "don't tell anyone", "transfer to RBI safe account for verification" |
| **Fake KYC / account block** | "KYC expired", "account will be blocked today", short links (bit.ly), cheap domains (.xyz, .top) |
| **UPI refund** | "sent by mistake / galti se", "enter UPI PIN to receive", "scan QR to get refund", collect requests |
| **OTP theft** | "OTP bata dijiye", "share the code" |
| **Remote access** | AnyDesk, TeamViewer, .apk files |
| **Electricity bill** | "connection will be disconnected tonight 9:30, call officer 98…" |
| **Task / part-time job** | "earn ₹3000 daily", "like YouTube videos", "prepaid task deposit" |
| **Lottery / prize** | "you won KBC lottery", "pay processing fee" |
| **Investment** | "guaranteed returns", "double your money" |
| **SIM block** | "your number will be blocked, press 9" |

It understands **English, Hinglish, Hindi (Devanagari), Tamil and Tanglish**, including mixed-language messages.

## How it works

1. **About 25 red-flag signals** written as patterns in all three languages. Each signal has a weight.
2. **Combination rules.** Scammers stack tactics, so authority + arrest threat + secrecy + money transfer scores far higher than any one signal alone.
3. **Near-certain asks** (OTP, UPI PIN to receive, staying on a video call) always count as "scam likely".
4. **Verdict:** 0–29 no scam signs, 30–59 be careful, 60–100 scam likely, with the scam type, the truth ("You never need a UPI PIN to receive money") and 3–4 steps.
5. **Live call mode** turns speech into text with the browser's speech recognition (hi-IN, ta-IN, en-IN), checks every sentence and **speaks a warning plus vibrates** as soon as the risk crosses a level.

Message checking runs **entirely on the phone**. No server, no API key, and nothing is stored or uploaded.

## Run it

- Laptop: open `index.html` in Chrome.
- Phone: open **https://icebergabhay1111-a11y.github.io/scam-shield/** in Chrome. Live listening needs https and a microphone permission.

## 2-minute demo for judges

1. **Hook (15 s).** "Indians lost thousands of crores to cyber fraud last year, and 'digital arrest' calls target our parents. They panic, they're told to keep it secret, and they pay."
2. **Paste demo (40 s).** Tap the **Digital arrest (Hindi)** example. Show the red stamp, the six red flags quoted from the message, and the highlighted text. Switch the interface to Tamil.
3. **Live call (45 s).** A teammate calls and reads the Hinglish script from speaker: "main CBI officer bol raha hoon… video call mat kato… kisi ko mat batana…". Scam Shield interrupts out loud: "सावधान। यह डिजिटल अरेस्ट ठगी लगती है…"
4. **Close (20 s).** It's private (on-device), works in Indian languages, needs no install, and always points to 1930 and Chakshu.

## Honest limitations

- It's a rule-based engine. It explains itself well but can miss new wording. Next step: a small multilingual classifier trained on reported scam messages.
- Live listening uses Chrome's speech service, which needs internet and may send audio to Google. On iPhone Safari, live mode may not work; message checking works everywhere.
- Hindi and Tamil text should be reviewed by native speakers before real use.
- Speech accuracy drops on a noisy speakerphone.

## Ideas to extend

- **Android share target.** Make it a PWA so you can "Share → Scam Shield" straight from WhatsApp.
- **Screenshot OCR.** Tesseract.js reads Hindi and Tamil from a screenshot of a message.
- **Family alert.** Send a "Papa got a digital-arrest call" message to a family member.
- **Number check.** Flag +92 or other spoofed and international numbers.

## Official help

- **1930**: National Cyber Crime Helpline
- **cybercrime.gov.in**: report online
- **sancharsaathi.gov.in/sfc**: Chakshu, for reporting fraud calls and messages
