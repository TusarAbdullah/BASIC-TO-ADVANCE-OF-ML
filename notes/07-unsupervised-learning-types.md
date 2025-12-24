# Unsupervised Learning (Part 2) — Clustering ছাড়াও কী আছে?

## 1) Unsupervised Learning-এর একটু বেশি “formal” সংজ্ঞা
### Supervised Learning
- ডেটা থাকে: **X (inputs) + Y (labels)**
- লক্ষ্য: **X → Y** mapping শেখা (predict Y)

### Unsupervised Learning
- ডেটা থাকে: **শুধু X (inputs)**
- **Y (label) থাকে না**
- লক্ষ্য: ডেটার মধ্যে **pattern/structure/interesting insight** খুঁজে বের করা

---

## 2) Clustering  — দ্রুত রিক্যাপ
**Clustering** হলো unsupervised learning-এর একটি টাইপ যেখানে অ্যালগরিদম:
- একই ধরনের data point-কে **একই cluster**-এ রাখে  
- মানে, unlabeled data-কে **group** করে

উদাহরণ: Google News-এ related articles একসাথে দেখানো, market segmentation ইত্যাদি।

---

## 3) Unsupervised Learning-এর আরও ২টি গুরুত্বপূর্ণ টাইপ (এই specialization-এ)
এই specialization-এ clustering ছাড়াও আরও দুইটা unsupervised learning শিখবে:

### 3.1 Anomaly Detection (অস্বাভাবিক ঘটনা/ডেটা ধরা)
**Anomaly detection** এমন একটি পদ্ধতি যা ডেটার মধ্যে:
- **unusual / rare / unexpected** ঘটনা খুঁজে বের করে

#### কেন দরকার?
- **Fraud detection** (financial system) এ খুব গুরুত্বপূর্ণ  
  - যেমন: হঠাৎ অস্বাভাবিক বড় লেনদেন, অস্বাভাবিক লোকেশন থেকে ট্রান্স্যাকশন  
  - এগুলো fraud-এর sign হতে পারে

আরও ব্যবহার:
- সিস্টেম/সার্ভার monitoring (অস্বাভাবিক স্পাইক)
- factory sensor data (মেশিনে অস্বাভাবিক আচরণ)
- security intrusion detection

> এখনই পুরোটা পরিষ্কার না হলেও সমস্যা নেই—পরে specialization-এ বিস্তারিত আসবে।

---

### 3.2 Dimensionality Reduction (ডেটা ছোট করে “compress” করা)
**Dimensionality reduction** মানে:
- অনেক বড়/বহু-feature ডেটাকে
- **কম dimension**-এ নামিয়ে আনা  
- কিন্তু যেন **তথ্য যতটা সম্ভব preserve** থাকে

#### কেন দরকার?
- ডেটা visualize করা সহজ হয়  
- computation দ্রুত হয়  
- noise কমে যেতে পারে  
- big dataset “compress” করে কাজ করা যায়

> এটাও প্রথমে অদ্ভুত লাগতে পারে, পরে উদাহরণসহ সহজ হয়ে যাবে।

---

## 4) Quiz অংশের ধারণা — কোনটা supervised, কোনটা unsupervised?
ভিডিওতে ৪টা উদাহরণ দেওয়া হয়েছিল: ২টা unsupervised, ২টা supervised।

### Unsupervised (labels নেই, structure discover)
1) **News stories grouping (Google News clustering)**  
   - অনেক article থেকে related stories cluster করা  
2) **Market segmentation**  
   - customer data দিয়ে segment/cluster বের করা

### Supervised (labels আছে, X→y)
1) **Spam filtering** (label: spam / not spam)  
2) **Diagnosing diabetes** (label: diabetes / not diabetes)

---

## 5) Recap (এই ভিডিওর সারাংশ)
- Unsupervised learning-এ **labels (y) থাকে না**
- লক্ষ্য: ডেটার মধ্যে **pattern/structure** বের করা
- Clustering ছাড়াও:
  - **Anomaly detection** (অস্বাভাবিক ঘটনা ধরা)
  - **Dimensionality reduction** (বড় ডেটা কম dimension-এ নামানো)

---

## Quick Revision (চিটশিট)
- **Supervised:** X + y → predict y  
- **Unsupervised:** X only → find structure  
- **Clustering:** group similar points  
- **Anomaly detection:** find unusual events  
- **Dimensionality reduction:** compress features with minimal info loss  

---

## Glossary
- **Anomaly:** অস্বাভাবিক/rare ডেটা পয়েন্ট  
- **Fraud detection:** প্রতারণা/অস্বাভাবিক লেনদেন শনাক্ত করা  
- **Dimensionality:** feature সংখ্যা/ডেটার dimension  
- **Dimensionality reduction:** dimension কমানো (তথ্য যতটা সম্ভব রেখে)



