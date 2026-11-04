# Конфиденциальность / Privacy

4 November 2026 · Pidjmail 0.2.1

## Русский

Почта соединяется напрямую с выбранным IMAP/SMTP-провайдером по TLS или обязательному STARTTLS. У Pidjmail нет собственного сервера почты, рекламного SDK или сбора аналитики. Чтение писем безопасным текстом не загружает внешние изображения и пиксели.

После проверки подключения пользователь выбирает папку писем и загрузку вложений для работы без интернета. Кэш до 100 писем на папку и скачанные вложения шифруются Electron safeStorage с защитой учётной записи Windows. Профиль, пароли, API-ключи, черновики, очередь, контакты, события, задачи, подписи, аватар и настройки также зашифрованы. Путь виден в настройках хранения. По умолчанию профиль находится в соседней с установкой папке Pidjmail Data, на том же диске. Выбор другого диска для первого ящика переносит туда профиль. В %APPDATA%/Pidjmail-location.json хранится только указатель пути. При недоступном диске нет переключения на C:. При миграции прежний зашифрованный профиль сохраняется.

По умолчанию входящие вложения просматриваются в памяти. «Сохранить как…» записывает файл по выбранному пути. Включённое пользователем автоматическое сохранение записывает обычные, незашифрованные файлы в выбранную папку. Зашифрованный кэш для работы без интернета — отдельная настройка. Исходящие вложения входят в зашифрованную очередь/черновик.

AI API отправляет промпт и выбранный пользователем контекст только по его команде; вложения автоматически не передаются. Веб-приложение ИИ загружает официальный сайт ChatGPT/Claude в отдельной изолированной сессии без доступа к почте и native API. Вход выполняется на сайте сервиса. Его правила, cookies и сетевые запросы действуют внутри этой страницы. Cookies самого сервиса сохраняются в зашифрованном профиле; хранилище веб-страницы работает в памяти. Удаление веб-подключения очищает эту сессию. Встроенный вход может ограничиваться сервисом, предусмотрен переход в браузер.

Почта проверяется автоматически, в том числе через IMAP IDLE. Уведомления могут показывать тему письма или название задачи; текст и звук почты, календаря и досок настраиваются отдельно. Сворачивание сохраняет работу в трее, полный выход её прекращает. Подтверждения прочтения зависят от решения получателя. Внешние ссылки открываются по действию пользователя. Выпуски обслуживает GitHub.

Обычное удаление приложения сохраняет профиль и папки писем. Отключение ящика не удаляет серверную почту и локальную папку. Для окончательного удаления закройте приложение и удалите профиль, выбранные папки и собственные резервные копии; сохранённые обычные файлы удаляются отдельно. Не переносите зашифрованный профиль между пользователями Windows.

Не публикуйте пароли, ключи, профили и переписку в [обращениях](https://github.com/AdamAnomatik/Pidjmail-Releases/issues). Уязвимости: [SECURITY.md](SECURITY.md).

## English

Mail connects directly to the selected provider through TLS or mandatory STARTTLS. Pidjmail has no mail relay, advertising SDK or usage analytics. Text-only mail display does not load remote images or tracking pixels.

After verification, choose a mail folder and whether to cache attachments offline. The bounded cache (100 messages per folder), offline attachments and application profile are encrypted using Electron safeStorage and Windows user protection. The profile includes credentials, optional API keys, drafts, queue, contacts, events, tasks, signatures, avatar and settings. Paths are shown in Data storage. The default profile is in Pidjmail Data beside the installation directory, on the same drive. Choosing a different drive for the first mailbox moves the profile too. %APPDATA%/Pidjmail-location.json holds only its path. There is no fallback to C: if a drive is unavailable. Legacy encrypted profiles are preserved during migration.

Incoming attachments are previewed in memory by default. Save As writes a file to the selected path. User-enabled automatic saving exports ordinary, unencrypted files to the chosen folder. Encrypted offline caching is a separate option. Outgoing attachments are included in encrypted drafts and queue.

AI API requests send a prompt and user-selected context only on command; attachments are not sent automatically. AI web apps load the official ChatGPT/Claude website in an isolated session without mail or native API access. Sign-in happens on the provider page, under its terms, cookies and network requests. First-party session cookies are stored only in the encrypted profile; other web storage is in memory. Removing the web connection clears this session. A service may restrict embedded login; a browser fallback is available.

Mail updates automatically, including through IMAP IDLE. Notifications may show mail subjects or task titles. Mail, Calendar and Boards have separate text/sound settings. Minimize keeps the app running in the tray; Quit stops it. Read receipts depend on recipients. External links open on user action. GitHub hosts release downloads.

Normal uninstall preserves the profile and mail folders. Disconnecting a mailbox preserves its local folder and server mail. For permanent deletion, quit and remove the profile, chosen folders and backup copies; exported files are separate. Do not transfer encrypted profiles between Windows users.

Never publish credentials, profiles or private mail in [issues](https://github.com/AdamAnomatik/Pidjmail-Releases/issues). See [SECURITY.md](SECURITY.md).
