# 📘 Facebook Posts Collector with MongoDB

This mini-project demonstrates how to build a **Python3 connector to Facebook** using the **Meta Graph API** to collect posts (images, text, and associated comments) related to a specific topic (e.g., *"le décès du président Jacques Chirac"*). The collected data is then stored in a **MongoDB** database for further analysis or visualization.

---

## 🚀 Features

- Connects to the **Facebook Graph API**
- Fetches posts from a **Facebook Business Page**
- Filters posts by **keyword/topic**
- Collects:
  - Post message
  - Post image
  - Created time
  - Comments (with usernames and text)
- Stores structured data in a **MongoDB** collection

---

## 🔧 Setup Instructions

### 1. Create a `.env` File

Create a `.env` file in the root directory and add your credentials:

```ini
ACCESS_TOKEN=your_facebook_access_token
PAGE_ID=your_facebook_page_id
MONGODB_URI=mongodb://localhost:27017
```

### 2. Install Dependencies

```bash
pip install requests pymongo python-dotenv
```

---

## 📜 Example Usage

In `collector.py` or your notebook:

```python
from facebook_collector import get_facebook_posts, save_to_mongo

topic = "Jacques Chirac"
posts = get_facebook_posts(PAGE_ID, ACCESS_TOKEN, topic=topic)
save_to_mongo(posts)
```

---

## 💾 Project Structure

```
facebook-posts-collector/
│
├── facebook_collector.py   # Core functions (data extraction + MongoDB storage)
├── .env                    # Environment variables (not pushed to GitHub)
├── README.md               # Project documentation
```

---

## ❗ Limitations

Due to Meta's API restrictions:

* You can only access **posts from a Facebook Page you own or manage**.
* You must manually approve API permissions like `pages_read_engagement` via **Meta for Developers**.

---

## 📘 References

* [Meta for Developers – Graph API](https://developers.facebook.com/docs/graph-api/)
* [MongoDB Official Docs](https://www.mongodb.com/docs/)

---

## ✨ Future Improvements

* Add support for Instagram Basic Display API
* Add Power BI or Streamlit dashboard to explore MongoDB data
* Automate keyword monitoring with a cron scheduler or Airflow

---



---

Let me know if you want this tailored for your **Jupyter Notebook** version or want a version in **French** too!
```
