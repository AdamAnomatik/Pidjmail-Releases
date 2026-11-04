# Конфиденциальность / Privacy

**Дата / Date:** 4 November 2026 · **Приложение / Application:** Pidjmail 0.2.0

## Русский

### Локальные данные

Pidjmail хранит параметры ящиков и интерфейса, ограниченный кэш писем, черновики и очередь, подписи, аватар, контакты, события, задачи, правила и уведомления в профиле `%APPDATA%\Pidjmail`. Пароли почты и необязательные API-ключи входят в зашифрованный профиль. Шифрование Electron safeStorage использует защиту учётной записи Windows. Резервная копия профиля также зашифрована. Это не заменяет блокировку и защиту самого компьютера.

### Сетевые соединения

- Почта передаётся напрямую выбранному IMAP/SMTP-провайдеру по TLS или обязательному STARTTLS. У Pidjmail нет собственного сервера для вашей почты.
- При включённом получении почты приложение периодически соединяется с провайдером и может держать IMAP IDLE-соединение.
- AI-помощник обращается к OpenAI или Anthropic только после запуска запроса пользователем. Передаются запрос и явно выбранный контекст письма; вложения автоматически не отправляются. Для API действуют условия выбранного сервиса.
- При запросе подтверждения прочтения отправляется стандартный заголовок с адресом отправителя. Получатель может отказаться отвечать.
- Внешние ссылки открываются по действию пользователя в браузере. Скачивание выпусков обслуживается GitHub; применяются его правила.

Приложение не содержит собственного сбора аналитики, рекламного SDK или облачной синхронизации календаря, контактов и досок. Текстовое чтение писем не загружает внешние изображения и пиксели отслеживания.

### Файлы и уведомления

Просмотр поддерживаемых входящих вложений выполняется в памяти без отдельной записи файла. «Сохранить как…» записывает файл по выбранному пути. Выбранный аватар сохраняется в профиле; исходящие вложения входят в локальный черновик/очередь. Системные уведомления могут показывать тему письма или название задачи; их можно отключить в настройках.

### Хранение и удаление

Обычное удаление программы сохраняет профиль. Для окончательного удаления данных закройте приложение и удалите его профиль и собственные резервные копии. Сохранённые через «Сохранить как…» файлы удаляются отдельно. Письма на сервере провайдера управляются отдельно; действия с письмами и папками могут синхронизироваться с сервером. Не переносите зашифрованный профиль между пользователями Windows.

Не прикладывайте профиль, пароли, ключи или личную переписку к публичным [обращениям](https://github.com/AdamAnomatik/Pidjmail-Releases/issues). Для уязвимостей см. [SECURITY.md](SECURITY.md).

## English

### Local data

Pidjmail stores account and interface settings, a bounded mail cache, drafts and delivery queue, signatures, avatar, contacts, events, tasks, rules and notifications under `%APPDATA%\Pidjmail`. Mail passwords and optional API keys are included in the encrypted profile. Electron safeStorage uses Windows account protection; the backup is encrypted as well. This does not replace protection of the computer itself.

### Network connections

- Mail connects directly to the selected IMAP/SMTP provider using TLS or mandatory STARTTLS. Pidjmail does not operate a mail relay for your messages.
- Automatic retrieval periodically contacts the provider and may keep an IMAP IDLE connection open.
- The AI assistant contacts OpenAI or Anthropic only after the user starts a request. The prompt and explicitly selected mail context are transmitted; attachments are not sent automatically. The chosen service's terms apply.
- Requesting a read receipt adds a standard header containing the sender's address. The recipient may decline to respond.
- External links open in the browser after a user action. GitHub serves release downloads under its own policies.

The application has no built-in usage analytics, advertising SDK or cloud synchronization of calendar, contacts and boards. Text-only email display does not load remote images or tracking pixels.

### Files and notifications

Supported incoming attachments are previewed in memory without writing a separate file. Save As writes to the selected location. An avatar is stored in the profile; outgoing attachments are part of local drafts and the delivery queue. System notifications may show email subjects or task titles and can be disabled in Settings.

### Retention and deletion

Normal uninstall preserves the profile. To remove local data permanently, close the application and remove the profile and your backup copies. Files explicitly saved through Save As are separate. Mail on the provider's server is managed separately; message and folder actions may synchronize to that server. Encrypted profiles should not be transferred between Windows users.

Do not attach profiles, passwords, API keys or private mail to public [issues](https://github.com/AdamAnomatik/Pidjmail-Releases/issues). Follow [SECURITY.md](SECURITY.md) for vulnerabilities.
