# Языковая школа "LinguaFlow" — Спецификация

## 1. Концепция и видение

Современная языковая школа с акцентом на персонализированное обучение. Сайт должен вызывать доверие, ощущение профессионализма и тепла. Визуально — чистый, но не холодный; профессиональный, но доступный. Целевая аудитория — взрослые 25-45 лет, ищущие качественное языковое образование.

## 2. Дизайн-система

### Цветовая палитра
```
Primary:        #6366F1 (Indigo — доверие, профессионализм)
Primary Dark:   #4F46E5 (Hover states)
Secondary:      #10B981 (Emerald — успех, прогресс)
Accent:         #F59E0B (Amber — внимание, CTA)
Background:     #F8FAFC (Slate-50)
Surface:        #FFFFFF
Text Primary:   #1E293B (Slate-800)
Text Secondary: #64748B (Slate-500)
Border:         #E2E8F0 (Slate-200)
```

### Типографика
```
Headings:   Inter (700, 600) — современный, читаемый
Body:       Inter (400, 500) — универсальный
Accent:     Inter (500 italic) — для цитат преподавателей
Fallback:   system-ui, -apple-system, sans-serif
```

### Размерная сетка
```
Base:       16px
Scale:      12 / 14 / 16 / 18 / 24 / 32 / 48 / 64px
Section:    80px vertical padding (desktop), 48px (mobile)
Container:  max-width: 1200px, padding: 0 24px
```

### Анимации
```
Duration:       200ms (micro), 300ms (standard), 500ms (emphasis)
Easing:         cubic-bezier(0.4, 0, 0.2, 1) — natural feel
Scroll reveal:  fade-up, stagger 100ms between items
Hover:          scale(1.02), shadow lift, color transition
```

### Иконки
Lucide Icons (CDN) — чистые, линейные, 24px

## 3. Структура страницы

### Header (sticky)
- Logo: "LinguaFlow" + иконка globe
- Nav: Языки | Тест | Преподаватели | Расписание | Тарифы | Личный кабинет
- CTA: "Записаться" (accent button)
- Mobile: hamburger menu

### Hero Section
- Заголовок: "Освой язык с нуля до fluency"
- Подзаголовок: описание школы (2-3 предложения)
- 2 CTA кнопки: "Пройти тест" (primary), "Выбрать язык" (secondary)
- Декоративный элемент: абстрактные языковые пузыри/круги
- Background: gradient mesh или subtle pattern

### Секция "Языки и уровни"
- Заголовок секции
- Tabs/переключатель языков: English, Spanish, German, French, Chinese
- Карточки уровней для выбранного языка (A1, A2, B1, B2, C1, C2)
- Каждая карточка: название уровня, описание, количество учеников

### Секция "Тест на уровень"
- Форма теста: 5-7 вопросов с вариантами ответов
- Прогресс-бар
- Результат: определение уровня (A1-C2) с рекомендацией
- CTA для записи на курс

### Секция "Преподаватели"
- Заголовок
- Сетка карточек (3-4 карточки):
  - Фото (placeholder gradient)
  - Имя
  - Специализация (язык + уровни)
  - Рейтинг (звёзды)
  - Стаж работы
  - Кнопка "Подробнее"

### Секция "Расписание"
- Заголовок
- Toggle: Онлайн / Офлайн
- Таблица или карточки: День | Время | Язык | Уровень | Преподаватель
- Фильтры: язык, уровень, время суток

### Секция "Форматы обучения"
- 2 карточки: Онлайн | Офлайн
- Каждая карточка: иконка, заголовок, список преимуществ (4-5 пунктов)
- Цена (опционально, для кросс-ссылки на тарифы)

### Секция "Тарифы"
- Toggle: Месяц / Год
- 3 карточки: Старт | Стандарт | Интенсив
- Каждая карточка:
  - Название
  - Цена (с переключением месяц/год)
  - Список включённого (4-5 пунктов)
  - CTA кнопка
- "Популярный" badge на Средний тариф

### Секция "Пробный урок"
- Заголовок
- Форма: Имя*, Телефон*, Email*, Язык (select), Уровень (select), Формат (radio: онлайн/офлайн)
- Кнопка "Записаться на бесплатный урок"
- Disclaimer: "Нажимая кнопку, вы соглашаетесь с политикой конфиденциальности"

### Footer
- Logo + краткое описание
- Контакты: телефон, email, адрес
- Соцсети: иконки
- Nav: политика, условия, FAQ
- Copyright

### Модальное окно "Личный кабинет"
- Tabs: Вход / Регистрация
- Форма входа: Email, Пароль, Забыли пароль?
- Форма регистрации: Имя, Email, Пароль, Подтверждение
- Соцсети для входа (иконки)

## 4. Компоненты

### Buttons
```
Primary:    bg: primary, text: white, hover: primary-dark, shadow
Secondary:  bg: transparent, border: primary, text: primary, hover: bg primary/10
Accent:     bg: accent, text: dark, hover: darken
Ghost:      bg: transparent, text: primary, hover: bg slate-100
Sizes:      sm (32px), md (40px), lg (48px)
```

### Cards
```
Background: white
Border:     1px solid border
Shadow:     0 1px 3px rgba(0,0,0,0.1)
Radius:     12px
Hover:      shadow-lg, translateY(-2px)
```

### Form Inputs
```
Height:     48px
Border:     1px solid border, focus: primary
Radius:     8px
Padding:    0 16px
Error:      border: red, text error below
```

### Navigation
```
Desktop:    horizontal, gap 32px
Mobile:     slide-in drawer from right
Active:     text: primary, font-weight: 600
```

### Test Component
```
Question card: numbered, options as radio buttons
Progress bar: full-width, primary color fill
Result:       modal or inline card with level badge
```

## 5. Состояния

### Loading
- Skeleton screens для карточек
- Spinner для кнопок при submit

### Empty
- Сообщение "Ничего не найдено" с иконкой

### Error
- Toast notification (bottom-right)
- Inline error под полями формы

### Success
- Toast notification (green)
- Модалка "Спасибо за заявку!"

## 6. Адаптивность

```
Mobile:     < 768px  — single column, hamburger menu
Tablet:     768-1024px — 2 columns where applicable
Desktop:    > 1024px — full layout
```

## 7. Технические детали

- Один файл `index.html` (HTML + CSS + JS inline)
- Google Fonts: Inter (400, 500, 600, 700)
- Lucide Icons CDN
- CSS Custom Properties для темизации
- Vanilla JS (ES6+)
- No frameworks, no build step
- Semantic HTML5

## 8. Контент-заглушки

### Преподаватели
1. Анна Петрова — English, B2-C1, 8 лет, ⭐ 4.9
2. Маркос Гарсия — Spanish, A1-B2, 5 лет, ⭐ 4.8
3. Елена Шмидт — German, A1-C1, 12 лет, ⭐ 5.0
4. Жан-Пьер Дюбуа — French, A1-B2, 6 лет, ⭐ 4.7

### Тарифы
- Старт: 4 занятия/мес, базовые материалы, 2990₽/мес
- Стандарт: 8 занятий/мес, все материалы, 4990₽/мес
- Интенсив: 12 занятий/мес, приоритетное расписание, 6990₽/мес

### Языки
- English, Spanish, German, French, Chinese (Mandarin)
