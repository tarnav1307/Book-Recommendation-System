# 📚 Book Recommender System (NLP + Web App)

A simple yet powerful **Book Recommendation System** built using **Machine Learning (Collaborative Filtering)** and deployed with a **Flask web application**. This project recommends books based on user input and also displays a list of popular books.

---

## 🚀 Features

- 🔥 Display top popular books  
- 🤖 Recommend books based on similarity  
- 📊 Uses collaborative filtering approach  
- 🌐 Interactive web interface using Flask  
- ❌ Handles invalid or empty inputs gracefully  

---

## 🛠️ Tech Stack

- **Frontend:** HTML, CSS (Flask Templates)  
- **Backend:** Python, Flask  
- **Machine Learning:** NumPy, Pandas  
- **Data Storage:** Pickle files  

---

## 📂 Project Structure

```
Book-Recommender-System/
│
├── app.py
├── books.pkl
├── popular.pkl
├── pt.pkl
├── similarity_scores.pkl
│
├── templates/
│   ├── index.html
│   └── recommend.html
│
└── README.md
```

---

## ⚙️ How It Works

1. A pivot table (`pt.pkl`) is created with books and users.  
2. A similarity matrix (`similarity_scores.pkl`) is generated using cosine similarity.  
3. When a user inputs a book name:  
   - The system finds its index  
   - Retrieves similar books using similarity scores  
   - Displays top 4 recommendations  

---

## 🧠 Core Logic

```python
index = np.where(pt.index == user_input)[0][0]
similar_items = sorted(
    list(enumerate(similarity_scores[index])),
    key=lambda x: x[1],
    reverse=True
)[1:5]
```

---

## ▶️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/book-recommender-system.git
cd book-recommender-system
```

---

### 2. Create Virtual Environment (Optional)

```bash
python -m venv .venv
source .venv/Scripts/activate   # Windows
```

---

### 3. Install Dependencies

```bash
pip install flask numpy pandas
```

---

### 4. Run the Application

```bash
python app.py
```

---

### 5. Open in Browser

```
http://127.0.0.1:5000/
```

---

## 📸 Screenshots


<img width="1920" height="1200" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/3288285e-05cd-44bb-a1ed-88d15849effb" />
<img width="1920" height="1200" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/390091f6-34ae-4a54-85b1-43a9cf3f971f" />
<img width="1920" height="1200" alt="Screenshot (55)" src="https://github.com/user-attachments/assets/274b8d2d-d8a5-419f-84b3-5c8b26e055ba" />
<img width="1920" height="1200" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/a8e119e9-133e-4396-8786-8e90286e72b1" />

---

## ⚠️ Error Handling

- If input is empty → Displays error message  
- If book not found → Shows "No results found"  

---

## 📌 Future Improvements

- 🔍 Add fuzzy search for typo handling  
- 🧠 NLP-based recommendations (content-based)  
- 👤 User authentication system  
- ⭐ Personalized recommendations  
- ☁️ Deploy on cloud (Render, AWS, Vercel)  

---

## 🙌 Author

**Arnav Tripathi**  
AI/ML Enthusiast 🚀  

---

## 📜 License

This project is open-source and available under the **MIT License**.

---

## ⭐ Support

If you like this project, consider giving it a **star ⭐ on GitHub**!
