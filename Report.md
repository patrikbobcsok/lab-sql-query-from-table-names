# Report: SQL Tables Exercise

In this exercise I tested some prompts where I had to say which tables are needed to answer a question.  

---

### ✅ Correct Ones

1. **Question:** *“Return all products with price above 500 and their stock_quantity.”*  
   - Answer: `["products"]`  
   - This was right because we only need product info here.  

2. **Question:** *“Find the names and emails of customers who ordered products with a price above 1000 in 2023, along with the total amount they spent.”*  
   - Answer: `["customers", "orders", "products"]`  
   - Also correct, because:  
     - Customers → names and emails  
     - Orders → date and total spent  
     - Products → price filter  

---

### ❌ Wrong One (Hallucination)

**Question:** *“Get the total number of orders for each customer.”*  
- Correct: `["customers", "orders"]`  
- My wrong answer: `["products"]`  

It messed up here. It added the products table when it was not needed. This is like a mini-hallucination — using a real table but not the right one.  

---

### What I Learned

- If the question asks about **people (who)** → use customers.  
- If it’s about **time, totals, or counts** → use orders.  
- If it’s about **price or stock** → use products.  
- Sometimes I added extra tables that weren’t needed → that’s the hallucination.  

---

In the end, it got most of them right, just one mistake. This exercise taught me I need to pay closer attention when choosing which tables are really needed.
