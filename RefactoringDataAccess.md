This Python code connects to a SQLite database, retrieves a user record, and returns the user data. However, it fails to abstract the database connection logic and uses a hardcoded query that's vulnerable to SQL injection.

```python
import sqlite3

def get_user_by_id(user_id):
    conn = sqlite3.connect('database.db')
    cursor = conn.cursor()
    cursor.execute(f"SELECT display_name FROM users WHERE id = {user_id}")
    user = cursor.fetchone()
    conn.close()
    return user
```

Example prompt 1
You can start by asking Copilot a general question about how to improve the code.

How can I improve this code to make it safe and easier to update and expand? List possible improvements but don't show revised code.

Example prompt 2
You can use the response to your first prompt to write a more specific prompt.

Rewrite this code to make it more scalable and easier to maintain. Use a context manager. Avoid hardcoded SQL queries and tightly coupled data access code. Instead, use a repository pattern to abstract database interactions and make the code more modular and reusable. Where possible optimize the code to improve performance. Include error trapping, and make sure the code is not vulnerable to SQL injection.
