
# Linear Regression (Part 2) — Supervised Learning কীভাবে কাজ করে? (Model Representation)

## 1) Supervised Learning-এর প্রক্রিয়া (Process)
Supervised learning-এ **training set** থাকে:

- **Input feature (x):** যেমন বাড়ির size  
- **Output target (y):** যেমন বাড়ির price (এটাই “right answer”)

### ধাপগুলো
1. Training set-এর **x এবং y** learning algorithm-এ দেওয়া হয়  
2. Algorithm ডেটা থেকে একটি **function/model** বানায়  
3. এই model নতুন input **x** পেলে একটি **prediction** দেয়

---

## 2) Model, Function, Prediction (Notation)
- **f** = function (এটাই model)  
- **x** = input / feature  
- **ŷ (y-hat)** = prediction / estimate

### y বনাম ŷ
- **y** = training data-তে থাকা আসল (true) target value  
- **ŷ** = model-এর অনুমান (estimate), true value হতে পারে বা নাও হতে পারে

উদাহরণ:  
বাড়ি এখনও বিক্রি হয়নি, তাই আসল price (y) জানা নেই। model **ŷ** দিয়ে আনুমানিক দাম বলে।

---

## 3) Linear model: f(x) = wx + b
এই ভিডিওতে model হিসেবে **straight line** ব্যবহার করা হয়েছে।

### Model formula
\[
f_{w,b}(x) = wx + b
\]

- **w** এবং **b** হলো সংখ্যা (parameters)  
- w, b এর মান বদলালে **line-এর ঢাল (slope)** এবং **উপর-নিচে অবস্থান (intercept)** বদলায়  
- একই x দিলে w,b অনুযায়ী ŷ পরিবর্তন হয়

**Prediction:**
\[
\hat{y} = f_{w,b}(x)
\]

> অনেক সময় সহজ করে শুধু **f(x)** লেখা হয়—মানে একই model, শুধু w,b সাবস্ক্রিপ্ট না লিখে।

---

## 4) কেন “linear” (সোজা লাইন) ব্যবহার করি?
- সোজা লাইন **simple** এবং বুঝতে সহজ  
- training, analysis, debugging সহজ হয়  
- পরে আরও complex (non-linear) model শেখার foundation তৈরি হয়

> কখনও কখনও curve/parabola ইত্যাদি দরকার হতে পারে, কিন্তু শুরু করার জন্য linear model খুব ভালো।

---

## 5) নামকরণ: Linear Regression (One Variable / Univariate)
এই model-এর নাম:
- **Linear Regression**

আর যেহেতু এখানে input feature মাত্র **একটা (x)**:
- **Linear regression with one variable**
- বা **Univariate linear regression**  
  - *uni* = one  
  - *variate* = variable

পরের দিকে যখন একাধিক feature (যেমন size, bedrooms, location…) ব্যবহার হবে, সেটাকে সাধারণত **multiple features / multivariate** ধাঁচে দেখা হয়।

---

## 6) Next Topic: Cost Function (খুব গুরুত্বপূর্ণ)
Linear regression কাজ করাতে হলে সবচেয়ে গুরুত্বপূর্ণ জিনিস হলো **cost function** বানানো।  
Cost function আমাদের বলে দেয়:
- model-এর prediction কতটা ভুল হচ্ছে  
- এবং কীভাবে w, b ঠিক করলে ভুল কমবে


