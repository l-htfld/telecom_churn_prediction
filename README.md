<h2>Описание услуг</h2><div class="paragraph">Оператор предоставляет два основных типа услуг:</div><ol start="1"><li>Стационарную телефонную связь. Телефон можно подключить к нескольким линиям одновременно.</li><li>Интернет. Подключение бывает двух типов: через телефонную линию DSL (англ.&nbsp;digital subscriber line&nbsp;— «цифровая абонентская линия») или оптоволоконный кабель (англ. fiber optic).</li></ol><div class="paragraph">Также абонентам доступен ряд услуг:</div><ul><li>Интернет-безопасность: антивирус (Device Protection) и блокировка опасных сайтов (Online Security);</li><li>Выделенная линия технической поддержки (Tech Support);</li><li>Облачное хранилище файлов для резервного копирования данных (Online Backup);</li><li>Стриминговое телевидение (Streaming TV) и каталог фильмов (Streaming Movies).</li></ul><div class="paragraph">За услуги клиенты могут платить ежемесячно или раз в 1–2 года. Доступны различные способы расчёта и возможность получить электронный чек.</div><h2>Описание данных</h2><div class="paragraph">Данные хранятся в базе данных PostgreSQL. Она состоит из нескольких таблиц:</div><ul><li><code class="code-inline code-inline_theme_light">contract</code>&nbsp;— информация о договорах;</li><li><code class="code-inline code-inline_theme_light">personal</code>&nbsp;— персональные данные клиентов;</li><li><code class="code-inline code-inline_theme_light">internet</code>&nbsp;— информация об интернет-услугах;</li><li><code class="code-inline code-inline_theme_light">phone</code>&nbsp;— информация об услугах телефонии.</li></ul><div class="paragraph"><strong>Таблица <code class="code-inline code-inline_theme_light">telecom.contract</code></strong></div><ul><li><code class="code-inline code-inline_theme_light">customerID</code>&nbsp;— ID абонента;</li><li><code class="code-inline code-inline_theme_light">BeginDate</code>&nbsp;— дата начала действия договора;</li><li><code class="code-inline code-inline_theme_light">EndDate</code>&nbsp;— дата окончания действия договора;</li><li><code class="code-inline code-inline_theme_light">Type</code>&nbsp;— тип оплаты: раз в год-два или ежемесячно;</li><li><code class="code-inline code-inline_theme_light">PaperlessBilling</code>&nbsp;— электронный расчётный лист;</li><li><code class="code-inline code-inline_theme_light">PaymentMethod</code>&nbsp;— тип платежа;</li><li><code class="code-inline code-inline_theme_light">MonthlyCharges</code>&nbsp;— расходы за месяц;</li><li><code class="code-inline code-inline_theme_light">TotalCharges</code>&nbsp;— общие расходы абонента.</li></ul><div class="paragraph"><strong>Таблица <code class="code-inline code-inline_theme_light">personal</code></strong></div><ul><li><code class="code-inline code-inline_theme_light">customerID</code>&nbsp;— ID пользователя;</li><li><code class="code-inline code-inline_theme_light">gender</code>&nbsp;— пол;</li><li><code class="code-inline code-inline_theme_light">SeniorCitizen</code>&nbsp;— является ли абонент пенсионером;</li><li><code class="code-inline code-inline_theme_light">Partner</code>&nbsp;— есть ли у абонента супруг или супруга;</li><li><code class="code-inline code-inline_theme_light">Dependents</code>&nbsp;— есть ли у абонента дети.</li></ul><div class="paragraph"><strong>Таблица <code class="code-inline code-inline_theme_light">telecom.internet</code></strong></div><ul><li><code class="code-inline code-inline_theme_light">customerID</code>&nbsp;— ID пользователя;</li><li><code class="code-inline code-inline_theme_light">InternetService</code>&nbsp;— тип подключения;</li><li><code class="code-inline code-inline_theme_light">OnlineSecurity</code>&nbsp;— блокировка опасных сайтов;</li><li><code class="code-inline code-inline_theme_light">OnlineBackup</code>&nbsp;— облачное хранилище файлов для резервного копирования данных;</li><li><code class="code-inline code-inline_theme_light">DeviceProtection</code>&nbsp;— антивирус;</li><li><code class="code-inline code-inline_theme_light">TechSupport</code>&nbsp;— выделенная линия технической поддержки;</li><li><code class="code-inline code-inline_theme_light">StreamingTV</code>&nbsp;— стриминговое телевидение;</li><li><code class="code-inline code-inline_theme_light">StreamingMovies</code>&nbsp;— каталог фильмов.</li></ul><div class="paragraph"><strong>Таблица <code class="code-inline code-inline_theme_light">telecom.phone</code></strong></div><ul><li><code class="code-inline code-inline_theme_light">customerID</code>&nbsp;— ID пользователя;</li><li><code class="code-inline code-inline_theme_light">MultipleLines</code>&nbsp;— подключение телефона к нескольким линиям одновременно.</li></ul><div class="paragraph">Информация о договорах актуальна на 1 февраля 2020.</div>
