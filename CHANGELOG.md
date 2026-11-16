# История изменений / Changelog

## [0.3.3](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.3.3) · Скачивание файлов и стабильность / Downloads and stability

**Русский**

- Исправлено скачивание изображений и документов из VK WorkSpace.
- Картинки можно вставлять в письмо и подпись через Ctrl+V. Если тема пуста, она заполняется именем первого вложения.
- Настройки сохраняются автоматически; исправлена потеря изменений при быстром переключении ящиков.
- Исправлены утечки ресурсов при переподключении чатов и отмене запросов adamanomatik.
- Для новых вложений действует предел 30 файлов и 100 МБ на письмо; изображение подписи — до 5 МБ. Большие входящие файлы по-прежнему можно скачивать.

**English**

- Fixed downloading images and documents from VK WorkSpace.
- Paste images into messages and signatures with Ctrl+V. An empty subject uses the first attachment’s filename.
- Settings save automatically; fixed losing edits when switching accounts quickly.
- Fixed resource leaks when reconnecting chats and cancelling adamanomatik requests.
- New outgoing attachments are limited to 30 files and 100 MB per message; signature images to 5 MB each. Large incoming files can still be downloaded.

## [0.3.0](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.3.0) · Статусы и панели / Read status and panels

**Русский**

- Нажатие на письмо сразу отмечает его прочитанным. Круглый значок переключает статус обратно.
- Панель разделов можно скрыть и вернуть; в отправленных показываются получатели.

**English**

- Clicking a message marks it read immediately. Use the round icon to toggle its status.
- Hide and restore the section toolbar; sent messages show their recipients.

## [0.2.29](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.29) · Без долгого зависания архива / Fix for archive freezes

**Русский**

- Исправлено длительное зависание при обновлении больших почтовых архивов.
- Письма и существующие отметки сохраняются; переподключать ящик не нужно.

**English**

- Fixed a long freeze when refreshing large mail archives.
- Mail and existing marks are retained; there is no need to reconnect the account.

## [0.2.28](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.28) · Меньше памяти / Lower memory use

**Русский**

- Большие архивы требуют меньше памяти; сохранённые письма можно читать и цитировать без связи с сервером.
- Добавлен журнал Pidjmail.log для разбора ошибок. Пароли и тексты писем в него не записываются.
- После обновления старые версии не смогут прочитать обновлённый почтовый кэш. Перед установкой сделайте полную резервную копию.

**English**

- Large archives use less memory; cached messages can be read and quoted while the server is unavailable.
- Added Pidjmail.log to help investigate errors. It does not record passwords or message text.
- Older versions cannot read the updated mail cache. Make a complete backup before installing.

## [0.2.27](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.27) · Меньше нагрузки в фоне / Less background load

**Русский**

- Чаты и фоновое сохранение почты меньше мешают работе с большим архивом.
- При выходе программа дожидается завершения записи данных.

**English**

- Chats and background mail saving cause fewer interruptions with large archives.
- The app waits for data to finish saving before it exits.

## [0.2.26](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.26) · Большие вложения / Large attachments

**Русский**

- Письмо открывается без ожидания загрузки всех вложений; файлы скачиваются по необходимости.
- Большие файлы и ZIP скачиваются с меньшим расходом памяти. Сняты прежние ограничения просмотра письма по его общему размеру.

**English**

- Messages open without waiting for every attachment; files download when needed.
- Large files and ZIPs download with lower memory use. Previous limits based on total message size have been removed.

## [0.2.25](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.25) · Обновление большой истории / Large-history updates

**Русский**

- Исправлена ошибка обновления прочтения и избранного в больших почтовых архивах.
- После обновления ящик не требуется отключать и подключать заново.

**English**

- Fixed updating read and starred status in large mail archives.
- There is no need to remove and reconnect your mail account after updating.

## [0.2.24](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.24) · Проверка подключения / Connection checks

**Русский**

- В настройках ящика появилась кнопка «Проверить подключение» с понятным отчётом.
- Отчёт помогает отличить проблемы сети, пароля и ограничений сервера; его можно скопировать для поддержки.

**English**

- Mail account settings now include Check connection with a readable report.
- The report helps distinguish network, password and server-limit issues, and can be copied for support.

## [0.2.23](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.23) · Надёжнее обновление папок / More reliable folder updates

**Русский**

- Ошибка одной папки больше не останавливает получение почты из остальных.
- Сохраняются загруженные письма, а предупреждение об ошибке остаётся до успешной проверки.

**English**

- An error in one folder no longer stops mail arriving in other folders.
- Downloaded mail is retained, and an error warning stays until a successful check.

## [0.2.22](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.22) · Понятные ошибки помощника / Clearer assistant errors

**Русский**

- adamanomatik объясняет, когда на балансе сервиса нет средств, превышен лимит или сервис перегружен.
- При временном ограничении запрос повторяется автоматически после короткой паузы.

**English**

- adamanomatik explains when a service has insufficient credit, a rate limit or an overload.
- Temporary rate limits are retried automatically after a short pause.

## [0.2.21](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.21) · Вложения и получатели / Attachments and recipients

**Русский**

- У каждого вложения своя кнопка скачивания, а все файлы можно сохранить одним ZIP.
- Папки и получателей можно перемещать перетаскиванием; файлы из Проводника — сразу в письмо.
- Пересланное письмо и предыдущая переписка отделены понятным разделителем.

**English**

- Each attachment has a download button, and all files can be saved as one ZIP.
- Drag folders and recipients to move them, and drop files from Explorer into a message.
- Forwarded messages and previous conversation have a clear separator.

## [0.2.20](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.20) · Удобнее читать и отвечать / Easier reading and replies

**Русский**

- Вернулся вид «Три колонки», а кнопки ответа и пересылки находятся над письмом.
- Выбирайте, закрывает ли крестик программу или сворачивает её в трей.
- Скрытые диски и чаты с выключенными уведомлениями освобождают память.

**English**

- The three-column view is back, with reply and forward buttons above the message.
- Choose whether the close button quits the app or minimises it to the tray.
- Hidden drives and chats with notifications disabled release memory.

## [0.2.19](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.19) · Облачные диски / Cloud drives

**Русский**

- Открывайте Яндекс Диск, Google Диск, Облако Mail, OneDrive и Dropbox внутри Pidjmail.
- Диск можно разместить рядом с почтой или отдельным окном. Чтобы приложить файл к письму, сначала скачайте его.

**English**

- Open Yandex Disk, Google Drive, Mail Cloud, OneDrive and Dropbox inside Pidjmail.
- Place a drive beside mail or in its own window. Download a file before attaching it to a message.

## [0.2.18](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.18) · Подтверждения прочтения / Read receipts

**Русский**

- Галочки в отправленных показывают полученные подтверждения прочтения. При наведении видно, кого ещё ждём.
- Можно выбрать, спрашивать ли перед отправкой подтверждения, отправлять всегда или не отправлять.
- Получатель может отказаться от подтверждения: отсутствие галочки не означает, что письмо не читали.

**English**

- Sent-mail checkmarks show received read receipts. Hover to see which recipients have not confirmed.
- Choose whether to ask before sending read receipts, send them automatically or never send them.
- Recipients may decline receipts: a missing checkmark does not mean the message was unread.

## [0.2.17](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.17) · Плавнее работа с архивом / Smoother mail archives

**Русский**

- Большие почтовые архивы меньше задерживают открытие писем, отметки и массовые действия.
- Улучшены долгие ответы локального помощника и продолжение загрузки модели после обрыва.

**English**

- Large mail archives cause fewer delays when opening messages, changing marks or applying bulk actions.
- Improved long local-assistant replies and resuming model downloads after interruptions.

## [0.2.16](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.16) · Помощник adamanomatik / adamanomatik assistant

**Русский**

- Помощника можно запустить бесплатно на компьютере или подключить через OpenRouter и собственный ключ сервиса.
- Помощник читает поддерживаемые вложения и собирает реестры для сохранения в Excel.
- Для локальной работы нужны разовая загрузка около 2,3 ГБ и примерно 8 ГБ памяти. Облачные запросы оплачиваются отдельно.

**English**

- Run the assistant locally for free, or connect through OpenRouter or your own service key.
- The assistant reads supported attachments and prepares registers you can save as Excel files.
- Local use requires an initial download of about 2.3 GB and around 8 GB of memory. Cloud requests are billed separately.

## [0.2.15](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.15) · Быстрее с большой почтой / Faster with large mailboxes

**Русский**

- Поиск, переключение разделов и работа с длинными списками стали отзывчивее.
- Улучшены читаемость мелкого текста, тёмная тема и заметность кнопок.
- Исправлено обновление списка писем при фоновой синхронизации.

**English**

- Search, navigation and long message lists are more responsive.
- Improved small-text readability, the dark theme and button visibility.
- Fixed message-list updates during background sync.

## [0.2.14](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.14) · Почта и комбайн / Mail and full workspace

**Русский**

- Выбирайте «Классическую почту» или «Комбайн» с дополнительными разделами.
- Просмотр вложений открывается на всё окно; для PDF и изображений доступны масштаб и поворот.
- Помощник adamanomatik умеет искать почту и готовить черновики, события и задачи по запросу.

**English**

- Choose Classic mail or the full workspace with additional sections.
- Attachment previews fill the window, with zoom and rotation for PDFs and images.
- The adamanomatik assistant can find mail and prepare drafts, events and tasks on request.

## [0.2.13](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.13) · Подписи и вложения / Signatures and attachments

**Русский**

- В подписи можно добавить ссылки и логотипы; предыдущая переписка сворачивается отдельно.
- Вложения находятся над письмом. Документы можно посмотреть внутри приложения или скачать одним ZIP.
- Размер всплывающих уведомлений теперь настраивается.

**English**

- Add links and logos to signatures; previous conversation is collapsed separately.
- Attachments appear above the message. Preview documents in the app or download them as a ZIP.
- Popup notification size is now adjustable.

## [0.2.12](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.12) · Панели и уведомления / Panes and notifications

**Русский**

- Для каждой рабочей панели можно независимо выбрать нужный раздел.
- Настраивайте угол экрана, цвет и длительность всплывающих уведомлений и проверяйте результат в предпросмотре.

**English**

- Choose the section shown in each workspace pane independently.
- Choose popup position, colour and duration, and preview the result.

## [0.2.11](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.11) · Архив почты и таблицы / Mail history and sheets

**Русский**

- Старая почта подгружается по мере просмотра без общего предела в 100 писем.
- Добавлен просмотр Google Таблиц. Для подключения потребуется настроить собственный Google OAuth-клиент.

**English**

- Older mail loads as you browse, without an overall 100-message limit.
- Added a Google Sheets viewer. Connecting it requires your own Google OAuth client.

## [0.2.10](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.10) · Две рабочие панели / Two workspace panes

**Русский**

- Откройте почту, календарь, контакты или задачи рядом с чатом в одном окне.
- Панели можно менять местами, располагать рядом или друг под другом и менять их размеры.

**English**

- Use mail, calendar, contacts or tasks alongside chat in one window.
- Swap panes, place them side by side or stack them, and resize them.

## [0.2.9](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.9) · Чат в отдельном окне / Chat in its own window

**Русский**

- Чат можно открыть рядом с почтой отдельным окном; выбранный сервис и масштаб запоминаются.
- При вводе получателей появляются подсказки из контактов и отправленных писем.
- Добавлены счётчики и уведомления подключённых чатов.

**English**

- Open chat in its own window beside mail; the selected service and zoom are remembered.
- Recipient suggestions use your contacts and sent mail.
- Added unread badges and notifications for connected chats.

## [0.2.8](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.8) · Режимы просмотра почты / Mail views

**Русский**

- Выбирайте почту по датам, список писем или чтение справа.
- Сохраняются размеры панелей; боковое меню можно свернуть.
- Добавлено отдельное подключение внешних помощников через MCP.

**English**

- Choose a date-based view, a message list or a reading pane on the right.
- Panel sizes are saved, and the sidebar can be collapsed.
- Added an optional MCP connection for external assistants.

## [0.2.7](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.7) · Отдельный чат VK / Standalone VK chat

**Русский**

- VK WorkSpace открывается сразу в отдельном веб-мессенджере.
- После обновления VK может попросить войти заново; почтовые ящики и настройки сохраняются.

**English**

- VK WorkSpace now opens its standalone web messenger directly.
- VK may ask you to sign in again after updating; mail accounts and settings are retained.

## [0.2.6](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.6) · Чаты рядом с почтой / Chat alongside mail

**Русский**

- В Pidjmail можно открыть VK WorkSpace, Google Chat, Telegram, WhatsApp и MAX.
- Вход выполняется на странице выбранного сервиса. Некоторые функции, включая звонки, могут потребовать браузер.

**English**

- Open VK WorkSpace, Google Chat, Telegram, WhatsApp and MAX inside Pidjmail.
- Sign in on the selected service’s page. Some features, including calls, may require a browser.

## [0.2.5](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.5) · Возврат из трея / Restoring from the tray

**Русский**

- Исправлено пустое окно при возврате из трея или после сна.
- В меню трея появилась команда «Восстановить интерфейс».

**English**

- Fixed a blank window when restoring from the tray or waking from sleep.
- Added Restore interface to the tray menu.

## [0.2.4](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.4) · Письма по отправителям / Mail by sender

**Русский**

- Непрочитанные письма сгруппированы по отправителям; письмо можно открыть отдельным окном.
- Добавлены индивидуальные цвета папок и отправителей, настройки подписей собраны в одном месте.
- Помощник adamanomatik доступен с верхней панели.

**English**

- Unread mail is grouped by sender, and messages can open in separate windows.
- Set individual folder and sender colours, with signature settings in one place.
- Open the adamanomatik assistant from the top toolbar.

## [0.2.3](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.3) · Восстановление профиля / Profile recovery

**Русский**

- Улучшено восстановление доступа к профилю при переносе приложения.
- Для резервной копии сохраняйте всю папку профиля и выбранные папки почты.

**English**

- Improved profile recovery when moving the app.
- For backups, keep the complete profile folder and your selected mail folders.

## [0.2.2](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.2) · Надёжнее перенос профиля / Safer profile moves

**Русский**

- Исправлено открытие зашифрованного профиля после переноса программы.
- Если профиль не открывается, можно выбрать полную резервную копию. Исходные данные сохраняются.

**English**

- Fixed opening an encrypted profile after moving the app.
- If a profile cannot be opened, choose a complete backup. Original data is preserved.

## [0.2.1](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.1) · Удобнее каждый день / Everyday improvements

**Русский**

- Подключение ящика и загрузка почты разделены: можно начать работу, пока письма загружаются в фоне.
- Папки можно переименовывать и переносить; уведомления почты, календаря и задач настраиваются отдельно.
- Добавлен помощник adamanomatik в боковой панели.

**English**

- Start using an account while its mail downloads in the background.
- Rename and move folders, and configure mail, calendar and task notifications separately.
- Added the adamanomatik assistant in the side panel.

## [0.2.0](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/tag/v0.2.0) · Первый выпуск / First release

**Русский**

- Почта, календарь, контакты и доски задач в одном приложении для Windows.
- Несколько ящиков, черновики, отложенная отправка и просмотр вложений.
- Русский и английский интерфейс, светлая и тёмная темы.

**English**

- Mail, calendar, contacts and task boards in one Windows app.
- Multiple accounts, drafts, scheduled sending and attachment previews.
- Russian and English interface, with light and dark themes.
