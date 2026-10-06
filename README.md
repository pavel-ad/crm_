# Skills Learner Enterprise CRM Pro

> **GitHub JSON Database & Render.com Hosting Integration**  
> GitHub-এ `db.json` ডাটাবেস থাকবে এবং ওয়েবসাইটটি Render-এ লাইভ হোস্ট থাকবে।

---

## 🚀 ফিচারসমূহ (Key Features)

1. **GitHub JSON Database (`db.json`)**:
   - সকল ৫০০+ রেকর্ড এখন সরাসরি GitHub রিপোজিটরির `db.json` ফাইলে সংরক্ষিত।
   - যেকোনো ব্রাউজারে সাইট ওপেন করলে সরাসরি GitHub থেকে লেটেস্ট ডাটা ফেচ (Fetch) হয়ে যাবে।
   - অফলাইন ও ফাস্ট লোডিংয়ের জন্য ব্রাউজার `localStorage` ক্যাশিং যুক্ত আছে।

2. **Render.com Hosting Ready**:
   - `index.html` ফাইল তৈরি করা হয়েছে যা Render-এ রুট ডিরেক্টরিতে হোস্ট হবে।
   - `render.yaml` কনফিগারেশন যুক্ত করা হয়েছে ১-ক্লিকে ডেপ্লয় করার জন্য।
   - ঐচ্ছিক নোড সার্ভার `server.js` এবং `package.json` যুক্ত আছে (Web Service ডেপ্লয়মেন্টের জন্য)।

3. **Cloud Database Sync & Management**:
   - সাইটের হেডার ও সাইডবারে **"🗄️ GitHub DB"** স্ট্যাটাস ও সিঙ্ক প্যানেল যুক্ত করা হয়েছে।
   - **🔄 Sync**: GitHub থেকে লেটেস্ট ডাটা রিফ্রেশ করার বাটন।
   - **🚀 Push to GitHub API**: GitHub Personal Access Token (PAT) দিলে যেকোনো নতুন রেকর্ড বা এডিট সরাসরি GitHub-এ কমিট হয়ে যাবে।
   - **💾 Download db.json**: ১-ক্লিকে আপডেটেড `db.json` ডাউনলোড করার সুবিধা।
   - **📥 Import db.json**: নতুন JSON ফাইল আপলোড করে ডাটাবেস আপডেট করার সুবিধা।
   - **🗑️ Delete Record**: লিড ডিলিট করার অপশন।

---

## 📁 ফাইল স্ট্রাকচার (File Structure)

```text
├── index.html                           # Render-এর মেইন প্রোডাকশন ফাইল (Fast & Clean)
├── db.json                              # GitHub JSON ডাটাবেস (সকল লিড রেকর্ড)
├── SkillsLearner_CRM_SuperPro_Ultimate.html # লোকাল ও ব্যাকআপ ফাইল
├── server.js                            # Render Web Service-এর জন্য নোড সার্ভার
├── package.json                         # প্রজেক্ট কনফিগারেশন
├── render.yaml                          # Render Blueprint ফাইল
└── README.md                            # বিস্তারিত গাইড
```

---

## 🌐 Render-এ ওয়েবসাইট ডেপ্লয় করার নিয়ম (Step-by-Step Guide)

### পদ্ধতি ১: Render Static Site (সবচেয়ে সহজ এবং ১০০% ফ্রি)

1. [Render.com](https://render.com) এ লগইন করুন।
2. ড্যাশবোর্ডে গিয়ে **"New +"** বাটনে ক্লিক করে **"Static Site"** সিলেক্ট করুন।
3. আপনার GitHub অ্যাকাউন্ট কানেক্ট করে `crm_` রিপোজিটরিটি সিলেক্ট করুন:
   - **Repository**: `https://github.com/pavel-ad/crm_`
4. নিচের সেটিংসগুলো দিন:
   - **Name**: `skillslearner-crm` (বা যেকোনো নাম)
   - **Branch**: `main`
   - **Build Command**: *(খালি রাখুন / Leave empty)*
   - **Publish Directory**: `.` *(একটি ডট দিন, অর্থাৎ রুট ফোল্ডার)*
5. **"Create Static Site"** বাটনে ক্লিক করুন।
6. ২ মিনিটের মধ্যে আপনার ওয়েবসাইট লাইভ হয়ে যাবে! (যেমন: `https://skillslearner-crm.onrender.com`)

---

## 🔄 GitHub-এ ডাটা পুশ ও আপডেট করার নিয়ম

আপনার লোকাল মেশিনে ফাইলগুলো কমিট ও পুশ করতে টার্মিনালে নিচের কমান্ডগুলো চালান:

```bash
git add .
git commit -m "Add GitHub JSON DB and Render deployment setup"
git push origin main
```

---

## ⚙️ ব্রাউজার থেকে সরাসরি GitHub-এ অটো-সেভ করার নিয়ম (Optional PAT Setup)

আপনি চাইলে কোনো টার্মিনাল কমান্ড ছাড়াই ব্রাউজার থেকেই নতুন লিড সরাসরি GitHub-এর `db.json`-এ সেভ করতে পারেন:

1. GitHub-এ যান: **Settings > Developer Settings > Personal Access Tokens > Tokens (classic)**।
2. **"Generate new token (classic)"** এ ক্লিক করুন।
3. নোটে লিখুন `CRM DB Sync` এবং `repo` পারমিশন চেক দিন।
4. টোকেনটি কপি করুন (যেমন: `ghp_xxxxxxxxxxxx`)।
5. আপনার CRM ওয়েবসাইটে গিয়ে উপরে **"GitHub DB"** বাটনে ক্লিক করুন।
6. টোকেনটি পেস্ট করে **"কনফিগারেশন সেভ করুন"** এ ক্লিক করুন।
7. এখন **"GitHub-এ সেভ / পুশ করুন"** বাটনে ক্লিক করলেই সরাসরি GitHub রিপোজিটরিতে `db.json` আপডেট হয়ে যাবে!
