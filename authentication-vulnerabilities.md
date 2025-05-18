Authentication Vulnerabilities

Цель: Понять, как работает аутентификация, какие уязвимости с ней связаны, и как их можно эксплуатировать.
Фокус: перебор паролей, enumeration, обход 2FA, атаки на логины.


🔐 Что такое Authentication

Аутентификация — это механизм проверки личности пользователя.
Уязвимости возникают, если:
	•	Можно угадать имя или пароль,
	•	Сайт реагирует по-разному на существующие/несуществующие логины,
	•	2FA можно обойти или пропустить.


 🔍 Типы уязвимостей
	•	Username enumeration — система «подсказывает», какие логины существуют
	•	Brute-force attacks — перебор логинов/паролей по словарям
	•	Credential stuffing — использование утекших логинов/паролей
	•	Weak password policy — предсказуемые или простые пароли
	•	2FA bypass — обход двухфакторной авторизации
	•	Session fixation / reuse — повторное использование чужой сессии


 ✅ Пройдено (Authentication — 10 из 10)
	•	✅ What is the difference between authentication and authorization?
	•	✅ Brute-force attacks
	•	✅ Brute-forcing usernames
	•	✅ Brute-forcing passwords
	•	✅ Brute-forcing passwords – Continued
	•	✅ Username enumeration
	•	✅ Username enumeration via different responses
	•	✅ User ID controlled by request parameter with unpredictable user IDs
	•	✅ User role controlled by request parameter (cookie tampering)
	•	✅ 2FA simple bypass


 💡 Что я узнал
	•	Разные ответы на логин = enumeration, облегчает брутфорс
	•	Часто пароли угадываются через Password1, admin123, qwerty!
	•	Burp Intruder — мощный инструмент для автоматического перебора
	•	Даже 2FA можно обойти, если после логина можно перейти напрямую


 🧰 Burp Suite (как использую)
	•	HTTP history — отслеживаю POST-запросы /login, параметры username, password
	•	Использую Intruder → Sniper или Pitchfork для атаки
	•	Слежу за разницей в длине/статусе ответа (например, 200 против 302)
