
# 🐘 PostgreSQL Database Assignment – Wildlife Conservation 🐾

## 📚 What is PostgreSQL?

PostgreSQL হচ্ছে সেই রকম একটি powerfull ডেটাবেইজ।  
ধরুন আমার কাছে একটি data Set আছে। সেটা আমার flexibility অনুসারে organize করে কোথাও store করব সেটাকে আমি Database  হিসাবে ধরে নিলাম।  
অনেক ডেটাবেইজ আছে আমার দরকার এমন একটি ডেটাবেইজ  যেখানে আমার ডাটা গুলো relational`(SQL)` 🗃️ and non-relational`(JSON)` 📦 দুই ভাবেই রাখে পারবো।

PostgreSQL একটি ওপেন-সোর্স রিলেশনাল ডেটাবেইজ ম্যানেজমেন্ট সিস্টেম (RDBMS) 🎯  
যেখানে অনেক ফিচার যেমন:  
✅ ট্রাঞ্জেকশন  
✅ ভিউস  
✅ স্টোরড প্রসিডিউর  
✅ ট্রিগার  
✅ কাস্টম ডেটা টাইপ  
সাপোর্ট করে।  

---

## 🧱 What is the purpose of a database schema in PostgreSQL?

Database এ আমাদের অনেক Data থাকে যেমন ✅টেবিল, ✅ভিউস, ✅ফাংশন ইত্যাদি।  
সেই সব ডেটার সংঘর্ষ এড়ানোর জন্য একটি স্কিমা `(schema)` 🧩 ব্যবহার করে বিভিন্ন অ্যাপ্লিকেশনের  বিভিন্ন অংশকে আলাদা করে টেবিল তৈরি করে নিরাপত্তা নিশ্চিত করা যায়।

🗂️ Data শ্রেণিবদ্ধ করে এবং একই ডেটাবেইজের মধ্যে বিভিন্ন ইউজার বা অ্যাপ্লিকেশন আলাদা করে Data ব্যবহারের সুযোগ করে দেয়।

📌 উদাহরণ: `public` স্কিমা হলো ডিফল্ট স্কিমা যেখানে টেবিলগুলো তৈরি হয়।

---

## 🔑 Primary Key & Foreign Key Concepts in PostgreSQL?

একটি database এর টেবিল বা ডেটা গুলো `uniquely identify` করাই হল `key` এর কাজ।  
এর মধ্যে অন্যতম key 👇

### 🏷️ Primary Key:
Primary Key হল একটি টেবিলের একটি বা একাধিক কলাম যা প্রতিটি রেকর্ডকে **uniquely identify** করে।  
🔒 এটি `NULL` মান support করে না।  
📍 প্রতিটি টেবিলে একটি ইউনিক মান থাকতে হবে – সেটিই প্রাইমারি key।  
➡️ Example: একটি `users` টেবিলে `user_id` প্রাইমারি কি হতে পারে।

### 🔗 Foreign Key:
Foreign Key হল একটি টেবিলের একটি কলাম যা অন্য একটি টেবিলের **Primary Key** কে রেফার করে।  
🔗 এটি দুইটি টেবলের মধ্যে সম্পর্ক স্থাপন করে।

➡️ উদাহরণ: `orders` টেবিলে `customer_id` কলামটি `Customer` টেবিলের `customer_id` কে রেফার করে নির্দেশ করে যে ব্যবহারকারী order করেছে।

---

## 🔍 Purpose of the `WHERE` Clause in a `SELECT` Statement?

`WHERE` clause SELECT statement ডেটাবেস থেকে নির্দিষ্ট রেকর্ডগুলি select করে প্রয়োজনীয় ডেটা ফিল্টার করে।  
🎯 এটি নির্দিষ্ট তথ্য খুঁজে পেতে সহায়তা করে।

📌 উদাহরণ:

```
SELECT * FROM employees WHERE department = 'Sales';
```

---

## ✏️ Modify Data Using `UPDATE` Statement?

ধরুন একটি `employees` টেবিল আছে যেখানে `salary` দেওয়া আছে।  
এখন আমার একজন employee এর `salary` পরিবর্তন (6000 থেকে 8000) করতে চাই, তাহলে আমরা `UPDATE` statement ব্যবহার করি।

📌 উদাহরণ:

```
UPDATE employees SET salary = 8000 WHERE salary = 6000;
```
