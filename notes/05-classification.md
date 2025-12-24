# 05 — Classification (Supervised Learning)

## Classification কী?
Classification হলো supervised learning-এর এমন কাজ যেখানে মডেল আউটপুট দেয়:
**কয়েকটি নির্দিষ্ট category/class এর মধ্যে ১টা**

Regression-এর মতো অসীম সংখ্যার মধ্যে নয়।

## উদাহরণ: Breast Cancer Detection
<img width="591" height="337" alt="image" src="https://github.com/user-attachments/assets/35f533f7-933b-462f-8172-96ebb3b9b436" />

লক্ষ্য: টিউমার
- **Benign (0):** ক্যানসার নয়
- **Malignant (1):** ক্যানসার/বিপদজনক

এখানে আউটপুট মাত্র ২টা → এটা Binary Classification।

## Multi-class Classification
ক্লাস ২টার বেশি হতে পারে:
<img width="612" height="307" alt="image" src="https://github.com/user-attachments/assets/265179c6-66bb-475d-b5bf-c3f0cb152707" />

- benign
- cancer type 1
- cancer type 2
(তখন আউটপুট ৩টা ক্লাস)

## Output class সংখ্যা নাও হতে পারে
- cat vs dog
- benign vs malignant
শব্দও হতে পারে, সংখ্যা (0/1/2) label হিসেবেও লেখা যায়।

## একাধিক input (features) নিলে কী হয়?
ধরা যাক:
<img width="639" height="419" alt="image" src="https://github.com/user-attachments/assets/e18457ce-fe35-4936-b466-e5269e892be3" />
- X1 = age
- X2 = tumor size
তখন মডেল একটি **decision boundary** শিখে benign আর malignant আলাদা করে।

বাস্তবে আরও features লাগে:
- thickness
- cell size uniformity
- cell shape uniformity ইত্যাদি

## Recap
- Supervised learning: X → Y, right answers দিয়ে শেখানো
- ২ ধরনের কাজ:
  - Regression: সংখ্যা
  - Classification: সীমিত ক্লাস/ক্যাটাগরি

## Quick Revision
- Classification = category prediction
- Decision boundary = ক্লাস আলাদা করার সীমারেখা



