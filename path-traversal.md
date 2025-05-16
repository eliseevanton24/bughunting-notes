# Path Traversal (Directory Traversal)

**Цель:** Научиться обнаруживать и использовать уязвимость "Traversal", чтобы получить доступ к файлам вне предполагаемой директории.

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

---

## Лаборатории пройдены

_Пока не проходил. Вернусь и запишу, когда завершу лабораторию._

---

## Что я узнал

_Пока в процессе. Сюда добавлю выводы после практики._

---

## Что изучить дальше

- [ ] Байпасы фильтров (`%2e`, `%2e%2e`, `%c0%af`)
- [ ] Path Traversal в upload-формах
- [ ] LFI → RCE цепочки

---

## Полезные ссылки

- 🔗 [PayloadAllTheThings — Path Traversal](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/File%20Inclusion#path-traversal)
- 🔗 [PortSwigger: Path Traversal](https://portswigger.net/web-security/file-path-traversal)
