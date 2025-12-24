
# 04 — Supervised Learning + Linear Regression

## Supervised Learning কী?
Supervised Learning এমন একটি পদ্ধতি যেখানে মডেল শেখে:
**X → Y (input থেকে output mapping)**
এখানে—
X = input (যেমন: ইমেইল, অডিও, ছবি, বাড়ির সাইজ, বিজ্ঞাপনের তথ্য)
y = output/label (যেমন: spam/not spam, ট্রান্সক্রিপ্ট টেক্সট, দাম, ক্লিক করবে কি না)

## মূল বৈশিষ্ট্য (সবচেয়ে গুরুত্বপূর্ণ)
Supervised Learning-এ তুমি মডেলকে শেখানোর সময় সঠিক উত্তরসহ উদাহরণ দাও:
(X₁, Y₁), (X₂, Y₂), …, (Xₙ, Yₙ)
তারপর মডেল শিখে ফেলে একটা ফাংশনের মতো:
y = f(X)
এবং ট্রেনিং শেষ হলে মডেল পারে—
নতুন একটা X (আগে কখনও দেখে নাই) দিলে
y অনুমান/প্রেডিক্ট করতে
## Supervised Learning কীভাবে কাজ করে? (Step-by-step)
ডেটা সংগ্রহ: X এবং তার সঠিক y
Train (শেখানো): মডেলকে (X, y) জোড়া দেখানো
Learn: মডেল প্যাটার্ন ধরে—কোন X এ কোন y হওয়ার সম্ভাবনা বেশি
Predict: নতুন X এ মডেল y বলে দেয়
Evaluate: কতটা ঠিক বলছে তা মাপা হয় (accuracy/error ইত্যাদি)



## উদাহরণ
- **Spam filter:** X=email, Y=spam/not spam
- **Speech recognition:** X=audio, Y=text transcript
- **Translation:** X=English, Y=Spanish/Arabic/…
- **Online ads:** X=ad+user info, Y=click করবে কি না
- **Manufacturing inspection:** X=product image, Y=defect আছে কি না

## Regression কী?
Regression হলো supervised learning-এর এমন কাজ যেখানে আউটপুট **একটা সংখ্যা**:
- অসীম সংখ্যার মধ্যে যে কোনো মান হতে পার


<img width="746" height="400" alt="image" src="https://github.com/user-attachments/assets/f88fc435-4995-4fff-82d8-109e78b35bd6" />


### Housing price উদাহরণ
- X = বাড়ির size
- Y = বাড়ির দাম
মডেল ডেটা দেখে line/curve fit করে দাম অনুমান করতে পারে।

## Regression বনাম Classification (সংক্ষেপ)
- **Regression:** সংখ্যা (continuous) like : house price, temperature, sales
- **Classification:** ক্যাটাগরি/ক্লাস (finite) like : spam/not spam, disease/healthy, click/no click

## Quick Revision
- Supervised = (X,Y) দিয়ে শেখানো
- Regression = number prediction
- Classification =  ক্যাটাগরি প্রেডিক্ট


