# Path Traversal (Directory Traversal)

**Цель:** Научиться обнаруживать и использовать уязвимость "Traversal", чтобы получить доступ к произвольным файлам.

---

## Что такое Path Traversal?

**Path Traversal** (он же Directory Traversal) — это уязвимость, которая позволяет злоумышленнику получить доступ к произвольным файлам на сервере, используя пути вроде:

../../../../etc/passwd

..%2f..%2f..%2fetc%2fpasswd

**Чем опасно:**
- Доступ к конфигурационным файлам, логам, базам данных
- Возможность атак на выполнение произвольного кода (в редких случаях)

---

## Примеры полезных payload'ов

```txt
../../../../etc/passwd
..%2f..%2f..%2fetc%2fpasswd
..\\..\\..\\windows\\win.ini


Подходы: URL-энкодинг, двойное кодирование, null-byte %00, байпасы фильтров

⸻

✅ Лаборатории пройдены

Lab: Reading arbitrary files via path traversal
	•	Задача: получить содержимое файла /etc/passwd
	•	Использовал URL:
image?filename=../../../etc/passwd
	•	Содержимое не отобразилось в браузере, но лаборатория засчитана как решённая
	•	Скорее всего браузер не смог отобразить ответ, потому что ожидал изображение, а получил текст

⸻

✅ Что я узнал
	•	Даже если результат не виден в браузере, сервер может успешно вернуть файл
	•	Путь к уязвимости чаще всего скрывается в параметрах вроде filename=
	•	Иногда проще увидеть ответ через Burp Repeater или вкладку Network → Response

⸻

Полезные ссылки
- [Burp Suite](https://portswigger.net/burp)
- [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
