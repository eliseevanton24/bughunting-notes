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

| Тема                        | Пройдено | Заметки / выводы |
|-----------------------------|----------|------------------|
| Path Traversal              | ✅        | Узнал, как читать произвольные файлы через `../` |
| Access Control              | ✅        | Узнал, как работают IDOR, эскалации прав и подмена cookie  |
| Authentication              | ✅        | Узнал, как происходит перебор логинов и паролей, обход 2FA |
| SSRF                        | ⏳        | — |
| File Upload Vulns           | ⏳        | — |
| OS Command Injection        | ⏳        | — |
| SQL Injection               | ⏳        | — |

---

## Содержание

- [`path-traversal.md`](path-traversal.md) — что такое Path Traversal, как его находить и эксплуатировать
- [`access-control.md`](access-control.md) — как работает контроль доступа, IDOR, подмена ролей и cookie
- [`authentication.md`](authentication.md) — как работает аутентификация, brute-force, username enumeration, сессии и 2FA
  
---

## Полезные ресурсы

- [Web Security Academy](https://portswigger.net/web-security)
- [Burp Suite](https://portswigger.net/burp)
- [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
- [Bug Bounty Hunter Guide](https://github.com/nahamsec/Resources-for-Beginner-Bug-Bounty-Hunters)
- [PortSwigger: Access control vulnerabilities](https://portswigger.net/web-security/access-control)
- [OWASP: Authorization Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html)

---
