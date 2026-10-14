# BCC Concierge · Bangladesh China Club Ltd

বাংলাদেশ চীন ক্লাব (BCC Concierge) কনসিয়ার্জ চ্যাটবক্স ওয়েব অ্যাপ্লিকেশন।

---

## 🚀 Vercel-এ ডেপ্লয় করার উপায় (How to Deploy to Vercel)

আপনার প্রজেক্টটি Vercel-এ ডেপ্লয় করার জন্য সম্পূর্ণ প্রস্তুত করা হয়েছে। আপনি দুটি উপায়ে এটি ডেপ্লয় করতে পারেন:

### পদ্ধতি ১: Vercel CLI দিয়ে সরাসরি ডেপ্লয় (সবচেয়ে দ্রুত)

১. আপনার টার্মিনালে এই কমান্ডটি চালান:
```bash
npx vercel
```

২. যদি প্রথমবার ব্যবহার করেন, তাহলে Vercel আপনাকে লগইন করতে বলবে (GitHub/Email দিয়ে ব্রাউজারে লগইন করে নিন)।

৩. এরপর কিছু সাধারণ প্রশ্ন করবে (সবগুলোতে **Enter** চাপলেই ডিফল্ট অপশন সিলেক্ট হবে):
   - `Set up and deploy?` -> **Y** (Enter)
   - `Which scope?` -> আপনার ইউজারনেম সিলেক্ট করে Enter
   - `Link to existing project?` -> **N** (Enter)
   - `What's your project's name?` -> **bccl-concierge-chatbox** (Enter)
   - `In which directory is your code located?` -> **./** (Enter)

৪. ডেপ্লয় শেষ হলে আপনি একটি প্রিভিউ লিঙ্ক পাবেন। সরাসরি প্রোডাকশনে ডেপ্লয় করতে:
```bash
npx vercel --prod
```
বা `npm run deploy` চালান।

---

### পদ্ধতি ২: GitHub এর মাধ্যমে Vercel ড্যাশবোর্ড থেকে

১. গিটহাবে একটি নতুন রিপোজিটরি তৈরি করুন (যেমন: `bccl-concierge-chatbox`)।
২. আপনার টার্মিনালে নিচের কমান্ডগুলো চালান:
```bash
git add .
git commit -m "Initial commit for Vercel deployment"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bccl-concierge-chatbox.git
git push -u origin main
```
৩. এরপর [vercel.com](https://vercel.com) এ লগইন করুন।
৪. **"Add New..."** > **"Project"** এ ক্লিক করে আপনার GitHub রিপোজিটরিটি সিলেক্ট করুন।
৫. **"Deploy"** বাটনে ক্লিক করুন। কয়েক সেকেন্ডেই আপনার সাইট লাইভ হয়ে যাবে!

---

## 💻 লোকাল কম্পিউটারে রান করার নিয়ম (Run Locally)

```bash
npm run dev
```
বা:
```bash
npx serve .
```
ব্রাউজারে `http://localhost:3000` এ ওপেন করলেই সাইটটি দেখতে পাবেন।

---

## 📁 প্রজেক্ট স্ট্রাকচার

- `index.html` — মূল অ্যাপ্লিকেশন ফাইল (Vercel রুট ফাইল হিসেবে ব্যবহার করবে)
- `vercel.json` — Vercel রাউটিং ও সিকিউরিটি হেডার কনফিগারেশন
- `package.json` — লোকাল রান ও ডেপ্লয় স্ক্রিপ্ট
- `.gitignore` — অপ্রয়োজনীয় ফাইল বাদ রাখার কনফিগ
