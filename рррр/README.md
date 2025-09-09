# A&M — Astro + Decap CMS Starter

Многостраничный сайт с удобной админкой `/admin`.

## Быстрый старт (локально)
```bash
npm i
npm run dev
```

## Деплой (Netlify + GitHub)
1. Создай **пустой репозиторий** на GitHub и запушь код:
```bash
git init
git add .
git commit -m "init: am agency site"
git branch -M main
git remote add origin https://github.com/<логин>/<repo>.git
git push -u origin main
```
2. Зайди на Netlify → **Add new site** → **Import from Git** → выбери репозиторий.  
   Build Command: `npm run build`, Publish directory: `dist`.
3. В Netlify включи **Identity** (Settings → Identity → Enable) и **Git Gateway** (Identity → Services → Enable Git Gateway).  
   Нажми **Invite users** и пригласи свой email.
4. Открой `https://<твой-сайт.netlify.app>/admin` → войди → редактируй **Кейсы** и **Команду**.  
   Все изменения попадут в Git автоматически.

## Куда сохраняются файлы из CMS
- Кейсы: `src/pages/cases/*.md`  
- Команда: `src/pages/team/*.md`  
- Настройки (название, контакты): `src/data/settings.json`  
- Медиа: `public/uploads`

## Форма
Страница `/contact` использует **Netlify Forms** (без сервера). Заявки будут в разделе **Forms** на Netlify.

## Аналитика/пиксели
Добавим Метрику/Pixel в `src/layouts/BaseLayout.astro` по желанию.
