# 🧠 SQL Practice Log

This repository contains SQL problems I’ve solved on platforms like StrataScratch.

---

### ✅ Problem: Share of Active Users  
📌 [StrataScratch Problem Link](https://platform.stratascratch.com/coding/2005-share-of-active-users)

```sql
-- My solution:
SELECT COUNT(*) * 100.0 / (
    SELECT COUNT(DISTINCT user_id)
    FROM fb_active_users
) AS us_active_share
FROM fb_active_users
WHERE status LIKE 'open'
  AND country LIKE 'USA';


