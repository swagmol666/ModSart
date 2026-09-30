<div align="center">

# 🟢 ModSart

**Твоя вселенная модов для Minecraft**

Платформа для публикации, поиска и скачивания модов, ресурспаков, шейдеров, модпаков и плагинов.

[Демо](#-демо) · [Возможности](#-возможности) · [Установка](#-установка) · [Скриншоты](#-скриншоты) · [Контрибьютинг](#-контрибьютинг)

</div>

---

## 📖 О проекте

**ModSart** — это открытая платформа в стиле [Modrinth](https://modrinth.com), созданная для сообщества Minecraft. Здесь можно публиковать свои проекты, находить моды под нужный загрузчик и версию игры, а также делиться ими с миллионами игроков.

Проект написан с упором на **скорость**, **тёмную тему** и **удобство разработчиков модов**.

> ⚠️ **Статус:** проект в активной разработке (alpha). API и структура БД могут меняться.

---

## ✨ Возможности

- 🔍 **Умный поиск** — по названию, автору, тегам и версии игры
- 🧩 **Поддержка загрузчиков** — Fabric, Forge, NeoForge, Quilt
- 📦 **Категории** — моды, ресурспаки, шейдеры, модпаки, плагины
- ⚡ **Быстрый отклик** — SPA-интерфейс без перезагрузок
- 🌙 **Тёмная тема** — из коробки, в стиле Modrinth
- 👤 **Профили авторов** — со статистикой, проектами и подписчиками
- ❤️ **Избранное и подписки** — следи за любимыми модами
- 🔐 **Авторизация** — через GitHub и Discord OAuth
- 📊 **Аналитика** — скачивания, просмотры, версии
- 🌍 **Локализация** — русский и английский языки

---

## 🖼 Скриншоты

<div align="center">

### Главная страница
![Главная страница](docs/screenshots/home.png)

### Карточка мода
![Карточка мода](docs/screenshots/mod-card.png)

### Профиль автора
![Профиль автора](docs/screenshots/profile.png)

</div>

---

## 🚀 Демо

Живая версия доступна по адресу: **[modsart.example.com](https://modsart.example.com)**

Тестовый аккаунт:
```
login: demo@modsart.dev
pass:  demo1234
```

---

## 🛠 Технологии

| Слой | Технологии |
|------|-----------|
| **Frontend** | HTML5, CSS3, Vanilla JS *(в планах — React + Vite)* |
| **Backend** | Node.js, Express, PostgreSQL, Prisma |
| **Хранилище** | S3-совместимое (MinIO / AWS S3) |
| **Auth** | OAuth 2.0 (GitHub, Discord) |
| **Деплой** | Docker, Docker Compose, Nginx |

---

## 📦 Установка

### Требования

- [Node.js](https://nodejs.org) ≥ 18
- [PostgreSQL](https://www.postgresql.org) ≥ 14
- [Docker](https://www.docker.com) *(опционально)*

### 1. Клонировать репозиторий

```bash
git clone https://github.com/your-username/modsart.git
cd modsart
```

### 2. Установить зависимости

```bash
npm install
```

### 3. Настроить переменные окружения

Создай файл `.env` на основе `.env.example`:

```bash
cp .env.example .env
```

```env
# База данных
DATABASE_URL=postgresql://user:password@localhost:5432/modsart

# Сервер
PORT=3000
NODE_ENV=development

# OAuth
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
DISCORD_CLIENT_ID=your_discord_client_id
DISCORD_CLIENT_SECRET=your_discord_client_secret

# S3
S3_ENDPOINT=http://localhost:9000
S3_BUCKET=modsart
S3_ACCESS_KEY=minioadmin
S3_SECRET_KEY=minioadmin
```

### 4. Запустить

```bash
# Миграции БД
npx prisma migrate dev

# Запуск в режиме разработки
npm run dev
```

Открой [http://localhost:3000](http://localhost:3000) 🎉

### Запуск через Docker

```bash
docker-compose up -d
```

---

## 📁 Структура проекта

```
modsart/
├── public/              # Статика (иконки, шрифты)
├── src/
│   ├── components/      # UI-компоненты
│   ├── pages/           # Страницы
│   ├── styles/          # CSS
│   ├── api/             # Клиент API
│   └── utils/           # Утилиты
├── server/              # Backend
│   ├── routes/          # REST-роуты
│   ├── models/          # Модели Prisma
│   ├── middleware/      # Auth, rate-limit
│   └── services/        # Бизнес-логика
├── docs/                # Документация
├── .env.example
├── docker-compose.yml
└── README.md
```

---

## 🤝 Контрибьютинг

Мы рады любой помощи! Прежде чем создавать PR:

1. Форкни репозиторий
2. Создай ветку: `git checkout -b feature/awesome-feature`
3. Закоммить изменения: `git commit -m "Add awesome feature"`
4. Запушь: `git push origin feature/awesome-feature`
5. Открой Pull Request

Пожалуйста, следуй [Code of Conduct](CODE_OF_CONDUCT.md) и [Contributing Guide](CONTRIBUTING.md).

### Идеи для контрибьютинг

- 🐛 Баг-фиксы — смотри [issues](https://github.com/your-username/modsart/issues)
- 🎨 Улучшение UI/UX
- 🌍 Переводы на другие языки
- 📝 Документация
- 🧪 Тесты

---

## 🗺 Roadmap

- [x] Тёмная тема и базовая вёрстка
- [x] Карточки модов и теги
- [ ] Регистрация и авторизация
- [ ] Загрузка файлов
- [ ] Система версий модов
- [ ] Комментарии и рейтинги
- [ ] API для лаунчеров
- [ ] Мобильное приложение

Полный список — в [Projects](https://github.com/your-username/modsart/projects).

---

## 📄 Лицензия

Проект распространяется под лицензией **MIT**. Подробности — в файле [LICENSE](LICENSE).

---

## 💚 Благодарности

- Вдохновлено [Modrinth](https://modrinth.com) и [CurseForge](https://curseforge.com)
- Иконки — [Lucide](https://lucide.dev)
- Шрифт — [Inter](https://rsms.me/inter/)

---

<div align="center">

**Сделано с ❤️ для сообщества Minecraft**

[⬆ Наверх](#-modsart)

</div>
