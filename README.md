# Web Security Academy Diary

Добро пожаловать в мой публичный дневник изучения web-уязвимостей, багхантинга и работы с Burp Suite. Здесь я пошагово записываю, что изучаю, какие лаборатории прохожу, и что узнаю в процессе.

## О себе
Я начинаю путь в информационной безопасности с фокусом на багхантинг и пентест. Использую:
- [x] Burp Suite Community Edition
- [x] Web Security Academy
- [x] Kali Linux
- [ ] Платформы для CTF / bug bounty (будет позже)

---

## Мой прогресс

## Apprentice

| Тема                        | Пройдено | Заметки / выводы |
|-----------------------------|----------|------------------|
| Path Traversal              | ✅        | Узнал, как читать произвольные файлы через `../` |
| Access Control              | ✅        | Узнал, как работают IDOR, эскалации прав и подмена cookie  |
| Authentication              | ✅        | Узнал, как происходит перебор логинов и паролей, обход 2FA |
| SSRF                        | ✅        | Узнал, как заставить сервер делать запросы на localhost, 192.168.x.x, удалять пользователей |
| File Upload Vulns           | ✅        | Узнал, как загружать web shell, обходить Content-Type и запускать RCE |
| OS Command Injection        | ✅        | Узнал, как выполнять команды на сервере, использовать whoami, &, ` |
| SQL Injection               | ✅        | Узнал, как извлекать скрытые данные, обходить WHERE, входить без пароля |


## Practitioner: SQL Injection

| Тема                                                                 | Пройдено | Заметки / выводы |
|----------------------------------------------------------------------|----------|------------------|
| What is SQL injection?                                               | ⏳        | — |
| How to detect SQL injection vulnerabilities                          | ⏳        | — |
| Retrieving hidden data                                               | ⏳        | — |
| Subverting application logic                                         | ⏳        | — |
| SQL injection UNION attacks                                          | ⏳        | — |
| Determining the number of columns required                           | ⏳        | — |
| Finding columns with a useful data type                              | ⏳        | — |
| Using a SQL injection UNION attack to retrieve data                  | ⏳        | — |
| Retrieving multiple values within a single column                    | ⏳        | — |
| Examining the database                                               | ⏳        | — |
| Blind SQL injection                                                  | ⏳        | — |
| Exploiting blind SQL injection by triggering conditional responses   | ⏳        | — |
| Error-based SQL injection                                            | ⏳        | — |
| Exploiting blind SQL injection by triggering time delays             | ⏳        | — |
| Exploiting blind SQL injection using out-of-band (OAST) techniques   | ⏳        | — |
| SQL injection in different contexts                                  | ⏳        | — |
| Second-order SQL injection                                           | ⏳        | — |
| How to prevent SQL injection                                         | ⏳        | — |


---

## Содержание

- [`path-traversal.md`](path-traversal.md) — что такое Path Traversal, как его находить и эксплуатировать
- [`access-control.md`](access-control.md) — как работает контроль доступа, IDOR, подмена ролей и cookie
- [`authentication.md`](authentication.md) — как работает аутентификация, brute-force, username enumeration, сессии и 2FA
- [`server-side_request_forgery.md`](server-side_request_forgery.md) — как работает SSRF, как сканировать локальную сеть, атаковать localhost и удалять пользователей
- [`file-upload-vulnerabilities.md`](file-upload-vulnerabilities.md) — как загружается web shell, какие бывают уязвимости валидации, обход Content-Type, RCE через upload
- [`os-command-injection.md`](os-command-injection.md) — как работает OS command injection, примеры инъекций (`&`, `|`, `whoami`) и полезные команды
- [`sql-injection.md`](sql-injection.md) — как находить SQL-инъекции, извлекать скрытые данные, обходить WHERE, логиниться без пароля 
  
---

## Полезные ресурсы

- [Web Security Academy](https://portswigger.net/web-security)
- [Burp Suite](https://portswigger.net/burp)
- [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
- [Bug Bounty Hunter Guide](https://github.com/nahamsec/Resources-for-Beginner-Bug-Bounty-Hunters)
- [PortSwigger: Access control vulnerabilities](https://portswigger.net/web-security/access-control)
- [OWASP: Authorization Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html)

---
