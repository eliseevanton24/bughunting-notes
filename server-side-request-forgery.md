SSRF (Server-Side Request Forgery)

Цель: Научиться использовать SSRF-уязвимости для взаимодействия с внутренними сервисами и получения данных.
Фокус: доступ к localhost, внутренним IP и обход фильтров.


📚 Что такое SSRF

SSRF — это атака, при которой злоумышленник заставляет сервер делать HTTP-запрос к другому ресурсу от своего имени.
Обычно используется для:
	•	получения доступа к внутренним системам (127.0.0.1, 192.168.0.x),
	•	обхода ограничений по IP или авторизации,
	•	раскрытия конфиденциальных данных (например, метаданных AWS или admin-панелей).


🔍 Типы атак SSRF
	•	SSRF на localhost — доступ к сервисам по 127.0.0.1, localhost
	•	SSRF на внутреннюю сеть — сканирование 192.168.0.x, 10.x.x.x


 ✅ Пройдено
	•	🧠 What is SSRF? (теория)
	•	🌐 SSRF attacks against the server
	•	🔄 SSRF attacks against the server - Continued
	•	🖥️ Lab: Basic SSRF against the local server
	•	🕸️ SSRF attacks against other back-end systems
	•	🧪 Lab: Basic SSRF against another back-end system


 💡 Что я узнал
	•	SSRF даёт доступ к скрытым интерфейсам админок без авторизации
	•	Можно перебрать внутреннюю сеть с помощью Burp Intruder (по статусу ответа)
	•	Запросы можно перенаправить на localhost/admin или 192.168.0.X
	•	Часто уязвим параметр типа stockApi, url, redirect=..., next=...
	•	SSRF опасен даже при отсутствии прямого отклика (blind SSRF)
