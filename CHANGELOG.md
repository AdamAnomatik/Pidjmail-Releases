# История изменений / Changelog

## 0.2.3 · 2026-11-04

- Все исправления ключа профиля и оформления установщика из предварительной 0.2.2.
- Восстановление из profile.enc.bak при отсутствующем основном файле, без пустого профиля и повторной отправки очереди.

Includes 0.2.2 key preservation and installer styling, plus safe orphaned-backup recovery without an empty reset or delivery replay.


## 0.2.2 · 2026-11-04

- Сохранение защищённого Windows ключа при переносе профиля и поиск подходящего прежнего ключа при ошибке открытия.
- Новый профиль создаётся отдельно только по выбору пользователя; исходные зашифрованные файлы сохраняются.
- Блок сайта в установщике оформлен как в Simpltask/SimplNote: значок, заголовок, описание и кнопка.

Preserve the Windows-wrapped profile key during relocation, recover with an available matching key, and offer a separate fresh profile without deleting original files. Installer website block follows Simpltask/SimplNote styling.

## 0.2.1 · 2026-11-04

- Быстрое двухфазное подключение с выбором папки и вложений; фоновая загрузка с прогрессом и временем.
- Настройки темы/языка работают во время синхронизации. Переименование/перенос папок и порядок разделов.
- Просмотр/Save As или автоматическое сохранение вложений, независимые уведомления почты/календаря/досок, трей.
- Правая панель ChatGPT/Claude: API или изолированное веб-приложение; вход зависит от сервиса, есть переход в браузер.
- Новый значок, компактные настройки, About по образцу, ссылка на сайт и выбор ярлыка в установщике.

Two-phase connection, chosen data folders, progressive background sync, responsive themes/language, folder editing, attachment modes, category notifications and tray. ChatGPT/Claude right-side API/web panels, refreshed icon/settings/About, installer website and desktop shortcut choice.


## [0.2.0] — 2026-11-04

### Русский

Первый публичный выпуск установщика Pidjmail для Windows x64.

#### Добавлено

- Пять разделов: почта, календарь, контакты, доски и будущий чат.
- Дерево серверных папок, IMAP IDLE с переподключением, восстановление из корзины.
- Фильтры «условия → действие», поиск Ctrl+F и отключаемая группировка по отправителю.
- Встроенный просмотр текста, изображений и PDF без отдельного сохранения; «Сохранить как…».
- Локальные канбан-доски и задачи, события и контакты из письма.
- Текстовые и звуковые напоминания, центр уведомлений, настройка громкости.
- Профиль, аватар, подписи ящиков и инструкции подключения почты.
- RU/EN, светлая, тёмная и системная темы.
- Запрос подтверждения прочтения MDN и необязательный OpenAI/Claude API-помощник.
- Установщик для текущего пользователя с выбором папки; обычное удаление сохраняет профиль.

#### Ограничения

Ранняя рабочая версия. OAuth, облачный календарь/контакты, полный архив и человеческий чат пока отсутствуют. Почтовые аккаунты и платные AI-запросы требуют реальной проверки. Подтверждение прочтения зависит от получателя; отмена доступна до SMTP-передачи. Установщик не подписан, автоматического обновления нет.

### English

First public Windows x64 installer release of Pidjmail.

#### Added

- Mail, Calendar, Contacts, Boards and a future Chat section.
- Server folder tree, reconnecting IMAP IDLE and restoration from Trash.
- Incoming-mail rules, Ctrl+F search and optional sender grouping.
- In-memory text, image and PDF previews with a separate Save As action.
- Local kanban tasks, plus events and contacts created from mail.
- Sound and text reminders, notification centre and volume settings.
- Profiles, avatars, account signatures and provider connection guides.
- Russian/English and light/dark/system themes.
- MDN read-receipt requests and an optional OpenAI/Claude API assistant.
- Per-user installer with directory selection and profile-preserving normal uninstall.

#### Limitations

Early working release. OAuth, cloud calendar/contact sync, full mail history and human chat are not available yet. Real mail accounts and paid AI requests require validation. Read receipts depend on the recipient; cancellation is available before SMTP transmission. The installer is unsigned and automatic updates are not available.
