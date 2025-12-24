# Unsupervised Learning (Clustering) 

## Unsupervised Learning কী?
Unsupervised Learning হলো এমন Machine Learning যেখানে **ডেটার সাথে কোনো output label (y) দেওয়া থাকে না**।  
অর্থাৎ, supervised learning-এর মতো (X, y) জোড়া নেই—শুধু **X** আছে।

এখানে কাজটা হলো:
- ডেটার ভেতর থেকে **pattern/structure** খুঁজে বের করা  
- “কি interesting” তা **অ্যালগরিদম নিজে** discover করে

> “Unsupervised” নাম দেখে ভুল বোঝার দরকার নেই—এটাও supervised-এর মতোই শক্তিশালী এবং বাস্তবে অনেক কাজে লাগে।

---

##  Supervised বনাম Unsupervised (এক নজরে)
### Supervised Learning
- ডেটা: **(X, Y)**  
- লক্ষ্য: X দেখে Y predict করা  
- উদাহরণ: spam/not spam, house price, benign/malignant

### Unsupervised Learning
- ডেটা: **শুধু X** (labels নেই)  
- লক্ষ্য: ডেটার মধ্যে **গ্রুপ/প্যাটার্ন/স্ট্রাকচার** বের করা  
- উদাহরণ: clustering, market segmentation, topic grouping

---

##  Unsupervised Learning-এর সবচেয়ে কমন টাইপ: Clustering
### Clustering কী?
Clustering হলো এমন একটি অ্যালগরিদম যা **unlabeled data**-কে স্বয়ংক্রিয়ভাবে কয়েকটা **cluster/group** এ ভাগ করে।

**কেন clustering দরকার?**  
যখন তুমি জানো না ডেটার “ধরন” কয়টা, কিন্তু তুমি চাই যে ডেটা নিজে নিজে **একই ধরনের জিনিসকে একসাথে** করে দিক।

---

##  Example 1: Patient data (Age + Tumor size) কিন্তু label নেই
ধরা যাক তোমার ডেটা আছে:
- Age
- Tumor size  
কিন্তু নেই:
- benign/malignant label

তাহলে তুমি diagnosis করছ না। বরং তুমি চাও:
- ডেটার মধ্যে কি কোনো natural grouping আছে?

একটা clustering algorithm হয়তো বলবে:
- এখানে **২টা cluster** আছে  
- একদিকে ছোট সাইজ/এক ধরনের বয়সের গ্রুপ  
- অন্যদিকে বড় সাইজ/অন্য ধরনের বয়সের গ্রুপ  

এটাই unsupervised learning—কারণ কেউ আগে থেকে বলে দিচ্ছে না “কোনটা কোন ক্লাস”, অ্যালগরিদম নিজেই খুঁজে বের করছে।

---

##  Example 2: Google News — Related news grouping
![WhatsApp Image 2025-12-24 at 9 44 16 PM](https://github.com/user-attachments/assets/38f655ea-2205-4fda-bc9c-2f2c96b20748)

Google News প্রতিদিন:
- লাখ লাখ news article দেখে
- একই ঘটনার/টপিকের খবরগুলোকে **একসাথে গ্রুপ** করে

এটা clustering দিয়ে করা হয়।

ক্লাস্টারিং কীভাবে বোঝে?
- একই ধরনের শব্দ বারবার আছে কিনা (যেমন: “panda”, “twin”, “zoo”)
- এই common words দেখে related articles একসাথে করে

**মূল কারণ:**  
News topics প্রতিদিন বদলায়, তাই মানুষ বসে বসে প্রতিদিন সব টপিক define করে দেওয়া সম্ভব না।  
অ্যালগরিদমকে **নিজে নিজে** topic cluster বানাতে হয়।

---

##  Example 3: DNA Microarray Data — People types discover করা
![WhatsApp Image 2025-12-24 at 9 46 06 PM](https://github.com/user-attachments/assets/c2ffe716-859c-4496-ab4b-376f47a877dd)

DNA microarray data-তে:
- প্রতিটি **column** = একজন ব্যক্তি
- প্রতিটি **row** = একটি gene
- রং/ইন্টেনসিটি = gene expression (কোন gene কতটা active)

এখন label নেই যে কে কোন “type”।  
Clustering algorithm:
- একই ধরনের gene expression pattern যাদের, তাদের একসাথে group করে  
- যেমন: Type 1, Type 2, Type 3

এটা unsupervised কারণ:
- আগে থেকে বলা নেই “Type 1 মানুষের বৈশিষ্ট্য কী”
- অ্যালগরিদম ডেটা দেখে নিজেই type গুলো বের করে

---

##  Example 4: Customer Segmentation / Market Segmentation
![WhatsApp Image 2025-12-24 at 9 47 38 PM](https://github.com/user-attachments/assets/ae7b1576-0e95-4a4b-a394-83ede8f86c7b)

অনেক কোম্পানির বিশাল customer database থাকে।  
Clustering ব্যবহার করে:
- customer-দের কয়েকটা segment এ ভাগ করা যায়  
যেমন:
- যারা skill/knowledge বাড়াতে চায়
- যারা career growth চায়
- যারা নিজের field-এ AI-এর impact জানতে চায়

এর ফলে কোম্পানি:
- প্রত্যেক segment-এর জন্য আলাদাভাবে service/marketing ঠিক করতে পারে  
- customer বুঝতে পারে বেশি ভালোভাবে

---

##  Summary (Recap)
- **Unsupervised learning = labels ছাড়া শেখা**
- লক্ষ্য: ডেটার ভেতরে **pattern/structure** খুঁজে বের করা
- সবচেয়ে কমন unsupervised algorithm: **Clustering**
- Clustering ডেটাকে **স্বয়ংক্রিয়ভাবে group/cluster** করে
- ব্যবহার: Google News grouping, DNA data analysis, market segmentation ইত্যাদি

---

## Quick Revision (চিটশিট)
- Supervised: (X,Y) → predict y  
- Unsupervised: X only → find structure  
- Clustering: unlabeled data → clusters/groups

---

## Glossary
- **Unsupervised learning:** label ছাড়া ডেটা থেকে প্যাটার্ন বের করা  
- **Label (Y):** সঠিক উত্তর/ক্যাটাগরি (supervised-এ থাকে)  
- **Cluster:** একই ধরনের ডেটার গ্রুপ  
- **Market segmentation:** customer-দের গ্রুপ করে আলাদা আলাদা সেবা/কৌশল বানানো



