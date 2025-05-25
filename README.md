

### 1. What is PostgreSQL? (PostgreSQL কী?)

PostgreSQL হলো একটি ওপেন-সোর্স ডেটাবেস সফটওয়্যার যা ডেটা সংরক্ষণ, খোঁজা এবং ম্যানেজ করতে ব্যবহৃত হয়।  
এটি বড় বড় প্রজেক্টেও ভালো কাজ করে এবং কাস্টম ফাংশন বা ডেটা টাইপ তৈরি করা যায়।

---

### 2. What is a database schema? (ডেটাবেস স্কিমা কী?)

স্কিমা হলো ডেটাবেসের ভেতরে আলাদা একটি নামের জায়গা, যেটার মাধ্যমে টেবিল, ফাংশন, ইত্যাদি গুছিয়ে রাখা যায়।  
এটি ডেটাবেসকে পরিষ্কার ও সুশৃঙ্খল রাখে।

---

### 3. What is Primary Key and Foreign Key? (Primary Key ও Foreign Key কী?)

- **Primary Key:** প্রতিটি রেকর্ড আলাদা করে চেনার জন্য ব্যবহার হয়। এটি ইউনিক ও NOT NULL হয়।  
  উদাহরণ: `animals` টেবিলের `animal_id`।

- **Foreign Key:** অন্য একটি টেবিলের Primary Key-এর সাথে সম্পর্ক তৈরি করে।  
  উদাহরণ: `sightings` টেবিলের `animal_id` হলো `animals` টেবিলের `animal_id` এর উপর নির্ভরশীল।

---

### 4. Difference between `CHAR` and `VARCHAR` (`CHAR` ও `VARCHAR` এর পার্থক্য)

| Feature       | `CHAR(n)`                        | `VARCHAR(n)`                     |
|---------------|----------------------------------|----------------------------------|
| Size          | Fixed size (ফিক্সড)              | Variable size (ফ্লেক্সিবল)       |
| Space usage   | Always takes full space          | Takes space as needed            |
| Example       | `'hi'` → `hi   ` (5 chars total) | `'hi'` → `hi` (2 chars only)     |

👉 সাধারণত `VARCHAR` বেশি ব্যবহার হয় কারণ এটি জায়গা বাঁচায়।

---

### 5. What is the `WHERE` clause? (`WHERE` ক্লজ কী?)

`WHERE` ক্লজ দিয়ে আমরা ডেটা থেকে নির্দিষ্ট শর্ত অনুযায়ী রেকর্ড ফিল্টার করতে পারি।

**উদাহরণ:**
```sql
SELECT * FROM animals WHERE species = 'Elephant';
