# Access Control

**Цель:** Понять, как работают механизмы контроля доступа, научиться их выявлять и эксплуатировать.  
Фокус: вертикальная и горизонтальная эскалация прав, обход доступа через параметры, URL, роли.

---

## 📚 Что такое Access Control

Контроль доступа — это проверка, может ли конкретный пользователь получить доступ к определённым данным или действиям.  
Уязвимость возникает, если сервер:
- не проверяет права пользователя,
- полагается только на клиентскую сторону (например, роль в параметрах).

---

## 🔍 Типы атак

- **Horizontal privilege escalation** — доступ к чужим данным (меняем `userId`)
- **Vertical privilege escalation** — доступ к действиям админа (меняем `role`, `privilege`)
- **Unprotected functionality** — страницы или действия вообще не защищены
- **Access by parameter/URL** — параметры контролируют доступ, но не проверяются

---

## ✅ Пройденные темы и лаборатории (весь блок)

- 🔓 *Unprotected functionality*  
- 🛠️ *Lab: Unprotected admin functionality*  
- 🕵️ *Lab: Unprotected admin functionality with unpredictable URL*  
- ⚙️ *Parameter-based access control methods*  
- 🧑‍🔧 *Lab: User role controlled by request parameter*  
- 🔄 *Horizontal privilege escalation*  
- 👥 *Lab: User ID controlled by request parameter with unpredictable user IDs*  
- ⬆️ *Horizontal to vertical privilege escalation*  
- 🧾 *Lab: User ID controlled by request parameter with password disclosure*  
- 📘 *What is access control?* (теория)

---

## 💡 Что я узнал

- Проверка прав **на клиенте** — всегда плохая практика
- Часто достаточно подменить параметры `userId`, `role`, `isAdmin`
- Даже “скрытые” пути можно подобрать вручную
- **Access Control** часто встречается на реальных сайтах и даёт критичный доступ

---

## 🔧 Как я использовал Burp Suite

- Настроил прокси 
- Скачал сертификат с `http://burp` и установил в Firefox
- Работал с **Intercept OFF**, наблюдая трафик во вкладке **Proxy → HTTP history**
- Это позволяло видеть все запросы/ответы при работе с сайтом

---


## 🔗 Полезные ссылки

- [PortSwigger: Access control vulnerabilities](https://portswigger.net/web-security/access-control)
