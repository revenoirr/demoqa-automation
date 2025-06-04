# 📘 DemoQA UI Automation with Playwright

Автоматизация UI-тестирования сайта [DemoQA](https://demoqa.com/) с использованием **Playwright** и **Page Object Model**.

## 📋 Описание проекта

Этот проект включает написание end-to-end UI-тестов для сайта DemoQA, покрывая основные интерактивные компоненты. Используется:

* **Playwright** для написания и запуска тестов
* **Page Object Model (POM)** для разделения логики страниц
* **Allure Report** для генерации отчётов
* **GitHub Actions** для CI/CD
* **Cross-browser testing** (Chrome и Firefox)

---

## ✅ Покрытые сценарии

| № | Страница                    | Описание                                                                                      |
| - | --------------------------- | --------------------------------------------------------------------------------------------- |
| 1 | `/alerts`                   | Обработка всех типов алертов (окна, подтверждения, промпта)                                   |
| 2 | `/automation-practice-form` | Заполнение обязательных полей формы и проверка результата                                     |
| 3 | `/text-box`                 | Заполнение текстбоксов случайными данными и проверка результата                               |
| 4 | `/tool-tips`                | Наведение на элементы и проверка отображения тултипов                                         |
| 5 | `/select-menu`              | Работа с дропдаунами и мультиселектами (значения: Group 2 Option 1, Other, Green, Black/Blue) |

---

## 🏗️ Структура проекта

```
src/
  ├── page-objects/     # Page Object Model
  ├── support/          # Вспомогательные файлы, хуки
  └── tests/            # UI-тесты (.spec.ts)
```

---

## 🚀 Установка и запуск

### 🔧 Установка зависимостей

```bash
npm install
npx playwright install --with-deps
```

### ▶️ Запуск тестов

```bash
npx playwright test           # Запуск всех тестов (Playwright)
npx playwright test --project=chromium
npx playwright test --project=firefox
npx playwright test --project=webkit


---

## 📊 Отчёты

### Allure Report

```bash
npm run allure:report  # Генерация и запуск отчёта
```

---

## 🔁 GitHub Actions (CI)

При пуше в `main` ветку автоматически запускаются:

* Установка зависимостей
* Запуск тестов
* Генерация Allure отчёта
* Загрузка отчёта как артефакта

Пайплайн: `.github/workflows/test.yml`



