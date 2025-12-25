# Supervised Learning Process (Part 1) — Linear Regression + Training Set Notation

## 1) শেখানো হয়েছে
supervised learning-এর overall process দেখানো হয়েছে এবং এই কোর্সের প্রথম মডেল **Linear Regression** পরিচয় করানো হয়েছে।  
Linear regression মানে হলো ডেটার উপর একটি **straight line (সোজা লাইন)** ফিট করা।

এটাকে খুব “basic” মনে হলেও এটা বাস্তবে সবচেয়ে বেশি ব্যবহৃত অ্যালগরিদমগুলোর একটি। এখানে শেখা অনেক কনসেপ্ট পরের অনেক ML মডেলেও কাজে লাগবে।

---

## 2) সমস্যা: House price prediction (Portland dataset)
লক্ষ্য: বাড়ির **size** দেখে বাড়ির **price** predict করা।

- **Horizontal axis (X-axis):** বাড়ির size (square feet)
- **Vertical axis (Y-axis):** বাড়ির price (thousands of dollars)

প্রতিটি ডেটা পয়েন্ট (cross) = একটি বাড়ি, যার size এবং recent sold price জানা আছে।

### Client example
ধরা যাক একজন ক্লায়েন্টের বাড়ির size:
- **1250 square feet**

Linear regression line ফিট করে দেখা যায় 1250 sq ft-এ predicted price আনুমানিক:
- **~220,000 dollars** 

---

## 3) কেন এটা supervised learning?
কারণ training সময় মডেলকে দেওয়া হয়:
- **X = size**
- **Y = price (right answer)**

প্রতিটি training example-এ ইনপুটের সাথে সঠিক আউটপুটও আছে।  
এই “right answers” থাকার কারণেই এটি supervised learning।

---

## 4) Regression বনাম Classification (রিক্যাপ)
### Regression
- আউটপুট: **একটা সংখ্যা** (continuous)
- উদাহরণ: house price, temperature, salary

### Classification
- আউটপুট: **ক্যাটাগরি/ক্লাস** (finite set)
- উদাহরণ: cat/dog, disease/no disease, benign/malignant

**মূল পার্থক্য:**
- Regression: অসীম সংখ্যার মধ্যে যেকোনো মান হতে পারে  
- Classification: সীমিত কিছু ক্লাসের মধ্যে একটি

---

## 5) Plot এর পাশাপাশি: Data table view
ডেটাকে দুইভাবে দেখা যায়:

### (A) Plot (গ্রাফ)
প্রতিটি cross = একটি বাড়ি (size, price)

### (B) Table (টেবিল)
ডেটা টেবিলে সাধারণত ২টা কলাম:
- **Input column:** size
- **Output column:** price

ভিডিওতে বলা হয়েছে এই dataset-এ:
- **47 rows** আছে  
অর্থাৎ **47টি training example**।

উদাহরণ (Row 1):
- size = **2104 sq ft**
- price = **400** (thousand dollars)  
এই row-টাই গ্রাফে একটি পয়েন্ট হিসেবে প্লট করা হয়।

---

## 6) Standard Notation (Machine Learning-এর স্ট্যান্ডার্ড লেখা-পদ্ধতি)
এই notation গুলো পরে বারবার আসবে।

### 6.1 Training set
যে dataset দিয়ে মডেল শেখে তাকে বলা হয় **training set**।

> Client-এর house (1250 sq ft) training set-এ নেই, কারণ এখনও sold হয়নি—price জানা নেই।

### 6.2 Input variable (feature)
- **x** = input variable  
- একে **feature** বা **input feature**-ও বলা হয়  
উদাহরণ: প্রথম বাড়ির জন্য  
- x = 2104

### 6.3 Output variable (target)
- **Y** = output/target variable  
উদাহরণ: প্রথম বাড়ির জন্য  
- Y = 400

### 6.4 Number of training examples
- **m** = মোট training examples  
এই dataset-এ  
- m = 47

### 6.5 One training example
একটি training example লিখি:
- **(x, y)**

উদাহরণ:
- (2104, 400)

### 6.6 i-th training example (indexing)
নির্দিষ্ট কোনো row বোঝাতে:
- **x^(i), y^(i)**

উদাহরণ:
- i = 1 হলে  
  - x^(1) = 2104  
  - Y^(1) = 400  

> গুরুত্বপূর্ণ: এখানে **(i)** exponent না।  
> x^(2) মানে x square না—এটা শুধু **2nd example** বোঝায়।

---

## 7) Recap (সারাংশ)
- Linear regression = ডেটার উপর **সোজা লাইন** ফিট করা  
- House price prediction = regression problem (number predict)  
- Training set = (x, y) জোড়া দিয়ে মডেল শেখানো  
- Notation: x, y, m, (x,y), x^(i), y^(i)  
- (i) মানে index, exponent না

---

## Next 
পরে দেখা হবে:
- এই training set-কে কীভাবে learning algorithm-এ “feed” করে মডেল শেখানো হয়

