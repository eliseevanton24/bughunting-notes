- [x] **Subverting application logic**
- [x] **Lab: SQL injection vulnerability allowing login bypass** 🧪✅

---

## 📘 Изучено:

### 📌 Subverting application logic
Разобрал, как с помощью SQL-инъекций можно **обойти логику авторизации**.  
Пример уязвимого запроса:
```sql
SELECT * FROM users WHERE username = 'administrator'--' AND password = ''

🧪 Lab: SQL injection vulnerability allowing login bypass

✅ Решил лабораторию!
Выполнил инъекцию, которая позволила войти как administrator, не зная пароля. Применил технику из предыдущей теории с комментарием --.
