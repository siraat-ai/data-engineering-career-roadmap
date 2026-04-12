# 🚀 SQL vs PySpark (Side-by-Side Examples)

## 🔹 1. SELECT Columns

### SQL

```sql
SELECT name, age FROM users;
```

### PySpark

```python
df.select("name", "age")
```

---

## 🔹 2. FILTER (WHERE)

### SQL

```sql
SELECT * FROM users WHERE age > 30;
```

### PySpark

```python
df.filter(df.age > 30)
```

---

## 🔹 3. GROUP BY + AGGREGATION

### SQL

```sql
SELECT customer_id, SUM(amount)
FROM orders
GROUP BY customer_id;
```

### PySpark

```python
df.groupBy("customer_id").sum("amount")
```

---

## 🔹 4. JOIN

### SQL

```sql
SELECT o.*, c.name
FROM orders o
JOIN customers c
ON o.customer_id = c.id;
```

### PySpark

```python
df_orders.join(df_customers, df_orders.customer_id == df_customers.id)
```

---

## 🔹 5. CREATE NEW COLUMN

### SQL

```sql
SELECT quantity * price AS revenue
FROM sales;
```

### PySpark

```python
from pyspark.sql.functions import col

df.withColumn("revenue", col("quantity") * col("price"))
```

---

# 🎯 Key Insight

👉 You can see:

* SQL = simple queries
* PySpark = same logic + more control

---

# 💬 Final Line (Add in file)

👉
**“PySpark extends SQL capabilities by enabling scalable, programmatic data processing across distributed systems.”**

---

# 🚀 Final Thought

👉
**“If you know SQL, PySpark becomes easy — it’s just SQL with power.”**

---

If you want next:
👉 I can create **1 small PySpark project based on these examples (GitHub-ready)** 🔥
