# 📊 Determining the Number of Columns Required

## 📘 Цель

Перед использованием SQL-инъекции с `UNION`, необходимо определить точное количество колонок, возвращаемых оригинальным запросом. Без этого инъекция вызовет ошибку.

---

## 🧪 Два метода:

### 1. `ORDER BY`

Последовательно выполняем запросы с увеличивающимся числом:
```sql
' ORDER BY 1--  
' ORDER BY 2--  
' ORDER BY 3--  
...

Когда появляется ошибка — значит, предыдущая цифра = количеству колонок.


 ### 2. 'UNION SELECT NULL,...'

 Пробуем подставлять разное количество NULL, пока запрос не сработает:
 ' UNION SELECT NULL--  
' UNION SELECT NULL, NULL--  
' UNION SELECT NULL, NULL, NULL--  
...


🏁 Пример для Oracle:

На Oracle нужно обязательно указывать FROM DUAL, например:
' UNION SELECT NULL FROM DUAL--


⚠️ Ошибки

Если количество NULL не совпадает с оригинальным числом колонок, возникает ошибка вида:
All queries combined using a UNION, INTERSECT or EXCEPT operator must have the same number of columns


🧬 Примечания по СУБД:
	•	-- (двойной дефис) используется как комментарий (в MySQL нужен пробел после него).
	•	В MySQL также можно использовать # вместо --.
	•	Для Oracle — обязательно FROM DUAL.

⸻

🔬 Практика

🧪 Lab: SQL injection UNION attack, determining the number of columns returned by the query

Статус: Not solved
📌 Задача — найти количество колонок, возвращаемых уязвимым SELECT, чтобы использовать это в будущих UNION-атаках.

⸻

💭 Вывод

Понимание структуры исходного SQL-запроса — фундамент для успешной SQL-инъекции через UNION. Следующий шаг — выяснить, какие столбцы отображаются в ответе и подходят для вывода данных.
