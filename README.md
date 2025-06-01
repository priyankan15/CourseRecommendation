# CourseRecommendation
Build a semantic course recommendation engine using OpenAI embeddings and vector similarity search.
---

## Features

- Converts course titles and descriptions to embedding vectors.
- Accepts learner profiles or text-based queries.
- Uses vector similarity (cosine) to find top matching courses.
- Powered by OpenAI Embeddings + ChromaDB or FAISS.
- API or CLI-based recommendation output in JSON format.

---

## Tech Stack

- **Language:** Python 3.10+
- **LLM:** text-embedding-ada-002
- **Vector DB:** ChromaDB
- **Framework:** LangChain
- **Input Format:** CSV
- **Output:** JSON object with top N course recommendations

---

## How to Run

1. Install dependencies:
   ```bash
   pip install openai chromadb pandas python-dotenv
   ```

2. Set up `.env` file with:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   ```

3. Prepare your course catalog (e.g. `courses.csv`):
   ```
   course_id, title, description
   ```

4. Run the recommender:
   ```python
   from recommender import recommend_courses
   user_profile = "Interested in Python and Data Engineering"
   print(recommend_courses(user_profile))
   ```

---

## 📤 Sample Output

```json
{
  "query": "Interested in Python and Data Engineering",
  "top_matches": [
    {
      "title": "Data Engineering Foundations",
      "score": 0.93
    },
    {
      "title": "Python for ETL Workflows",
      "score": 0.89
    }
  ]
}
```

---

## Test Cases

- Queries with generic tech interests
- Course matches by skill tags or title similarity
- Performance validation on >100 course items

---

## Contact

> Developed as part of GenAI Skill Tracks | AI Upskilling Initiative

