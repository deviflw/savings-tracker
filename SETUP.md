# 📋 Инструкция по настройке GitHub

## Шаг 1: Создай репозиторий на GitHub
1. Зайди на https://github.com
2. Нажми на "+" в правом верхнем углу → "New repository"
3. Название: `savings-tracker`
4. Описание: "💪 Отвоевываю у реальности - трекер экономии"
5. Сделай его **Private** (приватным) если не хочешь чтобы все видели
6. НЕ добавляй README, .gitignore или лицензию (у нас уже есть)
7. Нажми "Create repository"

## Шаг 2: Подключи локальный репозиторий к GitHub
После создания репозитория, GitHub покажет команды. Выполни их в PowerShell:

```powershell
cd C:\Users\mila\Desktop\savings-tracker
git remote add origin https://github.com/ТВОЙ_USERNAME/savings-tracker.git
git branch -M main
git push -u origin main
```

## Шаг 3: Создай Personal Access Token
1. Зайди в GitHub → Settings (твои настройки)
2. Слева внизу найди "Developer settings"
3. Выбери "Personal access tokens" → "Tokens (classic)"
4. Нажми "Generate new token" → "Generate new token (classic)"
5. Дай название: "Savings Tracker"
6. Выбери срок действия (рекомендую 90 дней)
7. Отметь галочку "repo" (полный доступ к приватным репозиториям)
8. Внизу нажми "Generate token"
9. **ВАЖНО!** Скопируй токен сразу! Он больше не покажется!
   Токен выглядит так: `ghp_xxxxxxxxxxxxxxxxxxxxx`

## Шаг 4: Настрой GitHub Pages (если хочешь онлайн версию)
1. Зайди в репозиторий на GitHub
2. Settings → Pages (слева в меню)
3. Source: Deploy from a branch
4. Branch: main (или master)
5. Folder: / (root)
6. Нажми Save

Через пару минут сайт будет доступен по адресу:
`https://ТВОЙ_USERNAME.github.io/savings-tracker/`

## Шаг 5: Введи токен в приложении
1. Открой index.html в браузере
2. В разделе "Настройка GitHub" введи:
   - GitHub Token: тот токен что скопировала (ghp_xxx...)
   - Репозиторий: ТВОЙ_USERNAME/savings-tracker
3. Нажми "Сохранить настройки"

## 🎉 Готово!
Теперь все твои записи будут автоматически сохраняться в GitHub!

## 📝 Заметки
- Пароль для добавления записей: 23
- Данные сохраняются в файле `savings-data.json` в репозитории
- Можешь открывать сайт с любого устройства если настроила GitHub Pages
