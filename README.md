# 🧠 SQL Projects & TestDome Certification

## 📜 Overview
This repository showcases my **SQL learning journey**, hands-on problem solving, and the official **TestDome SQL Certificate** that places me in the **Top 25% globally** (March 14, 2025).

I developed and tested all SQL scripts here as part of practical exercises designed to simulate real-world database tasks, including **data creation, manipulation, joins, aggregation, and relational modeling**.

---

## 🏆 Certification
**Platform:** [TestDome](https://www.testdome.com/)  
**Exam:** SQL Skills Assessment  
**Result:** Top 25% (March 2025)  
**Name:** Erietta Chamalidou  

> The TestDome assessment evaluates practical SQL proficiency through real coding scenarios that measure problem-solving ability and efficiency in working with data.

---

## 📚 What I Learned

Through the exercises and certification process, I strengthened my ability to:
- Design **normalized relational databases** (`CREATE TABLE`, `PRIMARY KEY`, `FOREIGN KEY`)
- Perform **complex joins** and **set operations** (`INNER JOIN`, `LEFT JOIN`, `UNION`)
- Implement **data manipulation** queries (`INSERT`, `UPDATE`, `DELETE`)
- Use **aggregate functions** (`COUNT`, `AVG`, `GROUP BY`, `HAVING`)
- Apply **conditional logic** and handle **case sensitivity** in SQL
- Model **self-referential relationships** (e.g., employee–manager hierarchy)
- Write **clean, reusable, and efficient** SQL code

---

## 💻 Sample Highlights

### 1️⃣ Student Records and Case Sensitivity  
```sql
SELECT COUNT(*) 
FROM students 
WHERE LOWER(first_name) = 'dimitra';
```

---

### 2️⃣ Updating Enrollments by Range  
```sql
UPDATE enrollments
SET year = 2015
WHERE enrollment_id BETWEEN 20 AND 100;
```

---

### 3️⃣ Merging Distinct Animal Names  
```sql
SELECT dogsname FROM dogs
UNION
SELECT catsname FROM cats;
```

---

### 4️⃣ Friendships and Self-Referential Relationships  
```sql
CREATE TABLE friends (
  user1 INT REFERENCES users(id),
  user2 INT REFERENCES users(id),
  PRIMARY KEY (user1, user2),
  CHECK (user1 < user2)
);
```

---

### 5️⃣ Calculating Average Session Durations  
```sql
SELECT user_id, AVG(duration)
FROM sessions
GROUP BY user_id
HAVING COUNT(user_id) > 1;
```

---

### 6️⃣ Seller–Item Join  
```sql
SELECT sellers.name, items.name
FROM sellers
INNER JOIN items ON sellers.id = items.sellerId
WHERE sellers.rating > 4;
```

---

### 7️⃣ Finding Non-Manager Employees  
```sql
SELECT name 
FROM employees
WHERE id NOT IN (
  SELECT manager_id FROM employees WHERE manager_id IS NOT NULL
);
```

---

## 🧩 Tools & Technologies
- **PostgreSQL** & **MySQL**
- **VS Code SQL Extension**

---

## 🌟 Achievements
- 🥇 Ranked **Top 25% worldwide** in TestDome SQL  
- 🧩 Built structured SQL solutions reflecting **real industry cases**

---

## 🙋‍♀️ About Me
I’m **Erietta Chamalidou**, a **COBOL Developer** and **SQL enthusiast** with a passion for database systems, clean code, and continuous learning.  
You can connect with me to collaborate on projects related to:
- Database design and optimization  
- Backend testing  
- Financial systems and data analytics  
