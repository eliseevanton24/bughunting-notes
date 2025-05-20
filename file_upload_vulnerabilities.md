# File Upload Vulnerabilities

**Цель:** Понять, как злоумышленники могут загружать вредоносные файлы, получать удалённый доступ (RCE) или обходить фильтрацию.

Фокус: загрузка web shell, уязвимая проверка Content-Type и расширений, пути обхода валидации.

---

## 📚 Что такое File Upload Vulnerabilities

Уязвимости загрузки файлов возникают, когда приложение позволяет загрузку файлов без должной проверки типа, содержания или расширения.  
Это может привести к:
- Выполнению произвольного кода (RCE),
- Обходу авторизации,
- Захвату сервера через web shell.

---

## 🔍 Основные векторы атак

- **Unrestricted file upload** — отсутствие проверки расширения/типа файла
- **Flawed extension validation** — проверяется только расширение (можно обойти с `file.php.jpg`)
- **Flawed MIME-type validation** — проверяется `Content-Type`, но не само содержимое
- **Web shell execution** — загрузка скрипта (например, PHP) с последующим выполнением
- **Bypass via double extensions** — `file.php.png`, `file.phtml`, `file.php;.jpg`
- **Upload to accessible folder** — файл сохраняется в папке, откуда можно его запустить

---

## ✅ Пройдено (весь блок File Upload Vulnerabilities)

- 📖 What are file upload vulnerabilities?
- 🔍 How do file upload vulnerabilities arise?
- 🐚 Exploiting unrestricted file uploads to deploy a web shell
- 🧪 Exploiting flawed validation of file uploads
- 📦 Flawed file type validation
- ⚔️ Lab: Remote code execution via web shell upload
- 🛡️ Lab: Web shell upload via Content-Type restriction bypass

---

## 💡 Что я узнал

- Даже если запрещено `.php`, можно использовать `Content-Type` или двойные расширения для обхода.
- Web shell (`<?php system($_GET["cmd"]); ?>`) — мощный инструмент для RCE.
- Проверка должна быть **по содержимому**, а не по MIME или расширению.
- Загрузка в директорию, доступную извне — потенциальная угроза.

---

## 🔧 Burp Suite (использовалось)

- Отслеживал `POST`-запросы с файлами
- Менял `Content-Type` вручную (на `image/jpeg` → `application/x-php`)
- Переходил по URL загруженного файла для проверки выполнения кода
- Использовал Repeater для отправки и повтора загрузки

