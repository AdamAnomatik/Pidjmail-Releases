# Конфиденциальность / Privacy

Ключ в `encryption-key.json` уже защищён Windows DPAPI; это не открытый пароль или ключ AES. Резервная копия должна включать его и `Browser/Local State`. При недоступном ключе прежние enc сохраняются; новый профиль создаётся отдельно только по выбору пользователя.

The key in `encryption-key.json` is already wrapped by Windows DPAPI, not a plaintext password or AES key. Include it and `Browser/Local State` in backups. Original encrypted files are preserved when a key is unavailable; a separate fresh profile requires the user's explicit choice.

4 November 2026 · Pidjmail 0.2.3

## Русский

MCP выключен по умолчанию. При включении подключённый ИИ может искать/читать письма и локальные контакты, события, задачи, создавать черновики/события/задачи. Отправка и корзина требуют подтверждения в Pidjmail. Пароли, API-ключи и исходные файлы вложений через инструменты не выдаются. Сервер доступен только на loopback с отдельным ключом; экспорт конфигурации содержит этот ключ обычным текстом и предназначен для закрытого хранения. Отключение отзывает ключ. Внешний сервер/туннель автоматически не настраивается; неподтверждённые действия не сохраняются и не повторяются после перезапуска.

Почта соединяется напрямую с выбранным IMAP/SMTP-провайдером по TLS или обязательному STARTTLS. У Pidjmail нет собственного сервера почты, рекламного SDK или сбора аналитики. Чтение писем безопасным текстом не загружает внешние изображения и пиксели.

После проверки подключения пользователь выбирает папку писем и загрузку вложений для работы без интернета. Кэш до 100 писем на папку и скачанные вложения шифруются Electron safeStorage с защитой учётной записи Windows. Профиль, пароли, API-ключи, черновики, очередь, контакты, события, задачи, подписи, аватар и настройки также зашифрованы. Путь виден в настройках хранения. По умолчанию профиль находится в соседней с установкой папке Pidjmail Data, на том же диске. Выбор другого диска для первого ящика переносит туда профиль. В %APPDATA%/Pidjmail-location.json хранится только указатель пути. При недоступном диске нет переключения на C:. При миграции прежний зашифрованный профиль сохраняется.

По умолчанию входящие вложения просматриваются в памяти. «Сохранить как…» записывает файл по выбранному пути. Включённое пользователем автоматическое сохранение записывает обычные, незашифрованные файлы в выбранную папку. Зашифрованный кэш для работы без интернета — отдельная настройка. Исходящие вложения входят в зашифрованную очередь/черновик.

AI API отправляет промпт и выбранный пользователем контекст только по его команде; вложения автоматически не передаются. Веб-приложение ИИ загружает официальный сайт ChatGPT/Claude в отдельной изолированной сессии без доступа к почте и native API. Вход выполняется на сайте сервиса. Его правила, cookies и сетевые запросы действуют внутри этой страницы. Cookies самого сервиса сохраняются в зашифрованном профиле; хранилище веб-страницы работает в памяти. Удаление веб-подключения очищает эту сессию. Встроенный вход может ограничиваться сервисом, предусмотрен переход в браузер.

Почта проверяется автоматически, в том числе через IMAP IDLE. Уведомления могут показывать тему письма или название задачи; текст и звук почты, календаря и досок настраиваются отдельно. Сворачивание сохраняет работу в трее, полный выход её прекращает. Подтверждения прочтения зависят от решения получателя. Внешние ссылки открываются по действию пользователя. Выпуски обслуживает GitHub.

Обычное удаление приложения сохраняет профиль и папки писем. Отключение ящика не удаляет серверную почту и локальную папку. Для окончательного удаления закройте приложение и удалите профиль, выбранные папки и собственные резервные копии; сохранённые обычные файлы удаляются отдельно. Не переносите зашифрованный профиль между пользователями Windows.

Не публикуйте пароли, ключи, профили и переписку в [обращениях](https://github.com/AdamAnomatik/Pidjmail-Releases/issues). Уязвимости: [SECURITY.md](SECURITY.md).

Ограниченный локальный журнал renderer-health.jsonl в текущей папке профиля содержит только время и системные коды состояния интерфейса. В нём нет адресов, переписки, паролей и URL; автоматической отправки журнала нет.

Вкладка «Чат» загружает официальные веб-приложения VK WorkSpace, Google Chat, Telegram, WhatsApp и MAX в раздельных сессиях. Почта и нативные функции Pidjmail недоступны этим страницам. При подключении сервис получает обычные запросы браузера по своим условиям. Cookies и ограниченный localStorage хранятся в зашифрованном профиле; IndexedDB и остальное веб-хранилище остаются в памяти, поэтому возможен повторный вход. Микрофон/камера запрещены, уведомления включаются по выбору. Загрузка файла открывает Save As. Отключение очищает активную сессию и её запись в текущем профиле; серверные сообщения и обычные зашифрованные резервные копии сохраняются.

## English

MCP is off by default. When enabled, the connected AI can search/read mail and local contacts, events and tasks, and create drafts/events/tasks. Sending and moving mail to Trash require approval inside Pidjmail. Tools do not return mail passwords, API keys or original attachment files. The server uses loopback and a separate key. Configuration exports contain that key in plaintext and must be kept private; disabling access revokes it. No public server/tunnel is configured automatically. Unapproved actions are memory-only and are not replayed after restart.

Mail connects directly to the selected provider through TLS or mandatory STARTTLS. Pidjmail has no mail relay, advertising SDK or usage analytics. Text-only mail display does not load remote images or tracking pixels.

After verification, choose a mail folder and whether to cache attachments offline. The bounded cache (100 messages per folder), offline attachments and application profile are encrypted using Electron safeStorage and Windows user protection. The profile includes credentials, optional API keys, drafts, queue, contacts, events, tasks, signatures, avatar and settings. Paths are shown in Data storage. The default profile is in Pidjmail Data beside the installation directory, on the same drive. Choosing a different drive for the first mailbox moves the profile too. %APPDATA%/Pidjmail-location.json holds only its path. There is no fallback to C: if a drive is unavailable. Legacy encrypted profiles are preserved during migration.

Incoming attachments are previewed in memory by default. Save As writes a file to the selected path. User-enabled automatic saving exports ordinary, unencrypted files to the chosen folder. Encrypted offline caching is a separate option. Outgoing attachments are included in encrypted drafts and queue.

AI API requests send a prompt and user-selected context only on command; attachments are not sent automatically. AI web apps load the official ChatGPT/Claude website in an isolated session without mail or native API access. Sign-in happens on the provider page, under its terms, cookies and network requests. First-party session cookies are stored only in the encrypted profile; other web storage is in memory. Removing the web connection clears this session. A service may restrict embedded login; a browser fallback is available.

Mail updates automatically, including through IMAP IDLE. Notifications may show mail subjects or task titles. Mail, Calendar and Boards have separate text/sound settings. Minimize keeps the app running in the tray; Quit stops it. Read receipts depend on recipients. External links open on user action. GitHub hosts release downloads.

Normal uninstall preserves the profile and mail folders. Disconnecting a mailbox preserves its local folder and server mail. For permanent deletion, quit and remove the profile, chosen folders and backup copies; exported files are separate. Do not transfer encrypted profiles between Windows users.

Never publish credentials, profiles or private mail in [issues](https://github.com/AdamAnomatik/Pidjmail-Releases/issues). See [SECURITY.md](SECURITY.md).

A bounded local renderer-health.jsonl in the current profile folder records timestamps and interface status codes only, without addresses, mail content, credentials or URLs. It is not uploaded automatically.

Chat loads official VK WorkSpace, Google Chat, Telegram, WhatsApp and MAX web apps in separate sessions without mail/native bridge access. These services receive normal browser requests under their terms. Cookies and bounded localStorage are encrypted in the profile; IndexedDB and other web storage are memory-only, so sign-in may be required again. Microphone/camera permissions are denied, notifications are optional, file downloads use Save As. Disconnect clears the active session and its current profile entry; server messages and normal encrypted backups remain.

В 0.2.9 веб-чат имеет только узкий мост уведомлений: разрешение, ограниченные текстовые поля и обратный click. Доступа к почте, MCP, файлам и ключам нет. Заголовок страницы может использоваться для локального счётчика; текст уведомления попадает в локальный центр уведомлений и баннер Windows. Подсказки получателей строятся локально из контактов и загруженных исходящих.

In 0.2.9 chat pages have a narrow notification bridge only: permission, bounded text fields and click callbacks. They cannot access mail, MCP, files or keys. A page title may supply the local badge count; notification text can appear in the local notification history and Windows banners. Recipient suggestions use local contacts and cached sent mail.
