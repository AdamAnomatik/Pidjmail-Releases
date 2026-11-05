# История изменений / Changelog

## 0.2.8 · 2026-11-05

- Три режима почты: по датам с подсветкой непрочитанных, прежнее чтение справа и компактный список в стиле Mail.ru. Выбор в настройках внешнего вида.
- Изменение ширины главного меню, дат, списка, планов дня и чата ИИ; сворачивание меню. Размеры сохраняются.
- Компактное меню сервисов чата; значок ИИ без текста перенесён к аватару после горячих клавиш.
- Серые/синие галочки исходящих по подтверждениям MDN и настройка запроса для новых писем. Отсутствие подтверждения не означает «не прочитано».
- Локальный MCP: 13 инструментов, отдельный отзываемый ключ, экспорт конфигурации, подтверждение отправки/корзины внутри Pidjmail. [Руководство](MCP.ru.md). Публичный сервер/туннель и вход в аккаунты ИИ не настроены.

Three mail layouts, unread date highlights, persistent panel resizing and collapsed navigation, a compact chat picker and relocated AI icon. Outgoing read-receipt checkmarks reflect matching MDN confirmations. Opt-in local MCP with a revocable key and in-app send/Trash approval. Browser access requires a separately configured secure connection. Unsigned Windows installer.

## 0.2.7 · 2026-11-05

- VK WorkSpace открывает отдельный веб-клиент мессенджера вместо оболочки со всеми сервисами.
- Сохранённые настройки и профиль не сбрасываются. VK может попросить войти заново на отдельной странице чатов.
- Проверены настоящий экран до входа и автоматические сценарии подключения/сессий. Список чатов под реальным аккаунтом после изменения адреса пока не проверен.

VK WorkSpace now opens the standalone messenger instead of the full suite shell. Existing profile/settings remain; VK may request sign-in again. The real welcome page and automated integration tests were checked; authenticated chat display still needs user verification.

## 0.2.6 · 2026-11-05

- Выбор во вкладке «Чат»: VK WorkSpace, Google Chat, Telegram, WhatsApp, MAX.
- Отдельные изолированные веб-сессии, переключение и отключение выбранного сервиса, Save As для файлов, управление разрешением уведомлений.
- Cookies и localStorage шифруются в профиле. Часть сервисов может требовать повторный вход после перезапуска; звонки/запись голоса открываются в браузере.
- Проверены настоящие страницы до авторизации, тестовые сессии и изоляция. Учётные данные и QR-подтверждения не вводились; реальная переписка пока не проверена.

Five official web chat integrations with a service picker/switcher and isolated sessions. Encrypted cookies/localStorage, explicit Save As, and per-service notification permission. Some services require re-login after restart; calls/voice recording use your browser. Sign-in pages were checked, actual authenticated messaging was not tested. Unsigned installer.

## 0.2.5 · 2026-11-05

- Восстановление интерфейса при падении процесса и возврате из трея; проверка после пробуждения и разблокировки Windows.
- Полные фоновые копии состояния больше не отправляются скрытому окну. Исправное окно перерисовывается без сброса текущего ввода.
- Пункт «Восстановить интерфейс» в меню трея, экран ошибки с рабочей кнопкой, ограничение автоматических попыток восстановления.
- Проверены принудительное падение, пустое окно и имитация resume: очередь и сохранённый черновик остаются. Полный ночной простой и физический sleep не проверялись; точный исходный ночной триггер не установлен.
- Установщик остаётся неподписанным. Перед установкой выйти из Pidjmail через меню трея.

Restores the UI after a renderer crash or empty window, checks tray restore/resume, avoids background state traffic to a hidden renderer, and adds a tray recovery action and error screen. Existing saved drafts and queue survive recovery. Tests simulate resume and forced crashes; an overnight physical sleep was not performed.

## 0.2.4 · 2026-11-04

- Непрочитанные сгруппированы по отправителям: отдельные окна списка и письма.
- Кнопка ИИ видна сразу; ChatGPT/Claude предлагают вход в приложение или настройку API.
- Исправлена ложная ошибка «Папка изменилась» во время фоновой синхронизации.
- Компактнее список писем, чтение и настройки. Подписи объединены в разделе «Письма» с выбором ящика.
- Основной цвет приложения, общие и индивидуальные цвета папок и отправителей.
- Проверены установка поверх 0.2.3, сохранение тестовой учётной записи, повторная установка и сохранность профиля после удаления.

Unread sender cards and separate message windows, a visible AI entry, fixed folder-generation handling during sync, tighter spacing, consolidated signatures, and app/folder/sender colours. Upgrade and profile retention verified with a disposable account. Installer remains unsigned.

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
