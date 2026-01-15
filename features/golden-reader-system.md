# 🏆 Feature Spec: Golden Reader Badge & Rewards 🎁

## 📋 Overview
The **Golden Reader** system is designed to gamify the reading experience on **ilm.red**. By rewarding users for consistency and social sharing, we aim to increase engagement and community growth.

---

## 👤 User Story
> "As a dedicated reader, I want to be recognized for my progress and shared insights so that I feel motivated to finish more books and invite my friends to the platform."

---

## 🛠 Feature Logic & Triggers
To earn the **Golden Reader** status, a user must meet at least **one** of the following criteria:

* **The Finisher:** Complete 100% of any 3 books. 📚
* **The Evangelist:** Refer 2 new users who sign up via a unique "Quote-Image" link. 🔗
* **The Scholar:** Click on at least 10 glossary terms to learn more context. 🧠

### ⚙️ Backend Logic (Pseudo-code)
```python
if user.books_completed >= 3 or user.referrals >= 2:
    user.status = "Golden Reader"
    user.unlock_premium(days=7)
    trigger_notification("congratulations_badge")
