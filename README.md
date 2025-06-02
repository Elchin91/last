# iSponsorBlockTV for iOS

iOS приложение для блокировки спонсорских сегментов в видео на Samsung TV.

## 🚀 Автоматическая сборка

### GitHub Actions
Проект автоматически собирается через GitHub Actions на каждый push:
- ✅ Используется macOS runner с Xcode
- 📦 IPA файл доступен в Artifacts
- 🏷️ Релизы создаются автоматически при push в main
- 🔧 Поддержка демо-режима для тестирования workflow

### Локальная сборка

#### macOS
```bash
# Быстрая сборка
make build

# Полная справка
make help
```

#### Windows
```batch
# Используйте bat файлы
.\build.bat

# Или установите make
choco install make
```

## 📲 Установка через TrollStore

### Шаг 1: Получение IPA
Выберите один из способов:

**Из GitHub Releases (рекомендуется):**
1. Перейдите в [Releases](../../releases)
2. Скачайте последний `iSponsorBlockTV_v*.ipa`

**Из GitHub Actions Artifacts:**
1. Перейдите в [Actions](../../actions)
2. Выберите последний успешный build
3. Скачайте `iSponsorBlockTV-*` artifact

### Шаг 2: Установка
1. Перенесите IPA файл на iPhone любым способом:
   - AirDrop
   - Облачное хранилище (iCloud, Google Drive)
   - Email вложение
   - Через Finder/iTunes
2. Откройте файл на iPhone
3. Выберите **TrollStore** в меню "Открыть в..."
4. Нажмите **Install**
5. Готово! 🎉

## 🛠️ Разработка

### Настройка окружения
```bash
# macOS
make dev-setup

# Проверка Xcode
xcodebuild -version
```

### Команды сборки
```bash
# Сборка IPA
make build

# Очистка
make clean

# Установка (показывает инструкции)
make install

# Полная справка
make help
```

### Windows пользователям
```batch
# Установите make
choco install make
# или
scoop install make

# Альтернативно используйте .bat файлы
.\build.bat
.\clean.bat
```

## 📁 Структура проекта

```
├── .github/workflows/    # GitHub Actions workflow
├── iOS_App/             # Xcode проект
│   ├── iSponsorBlockTV.xcodeproj/
│   └── iSponsorBlockTV/
├── build_ipa.sh         # Скрипт сборки Unix
├── build.bat            # Скрипт сборки Windows
├── clean.bat            # Очистка Windows
├── export_options.plist # Настройки экспорта для TrollStore
├── Makefile            # Make команды
└── README.md           # Этот файл
```

## 🔧 Технические детails

### Настройки для TrollStore
- ✅ Метод экспорта: `ad-hoc`
- ✅ Отключена подпись кода: `CODE_SIGNING_REQUIRED=NO`
- ✅ Оптимизированы настройки экспорта
- ✅ Поддержка установки без Developer аккаунта

### GitHub Actions
- 🖥️ Сборка на `macos-latest`
- 📦 Автоматическое создание релизов
- 🗂️ Artifacts с retention 30 дней
- 🔄 Поддержка демо-режима для тестирования

## 🐛 Устранение неполадок

### Проблемы со сборкой
1. **Xcode не найден**: Установите Xcode из Mac App Store
2. **Ошибки подписи**: Проект настроен для сборки без подписи
3. **Windows пользователи**: Используйте .bat файлы или установите make

### Проблемы с установкой
1. **TrollStore не видит файл**: Убедитесь что файл имеет расширение .ipa
2. **Ошибка установки**: Попробуйте перезагрузить TrollStore
3. **Файл поврежден**: Скачайте IPA заново

## 📞 Поддержка

- **Issues** - [GitHub Issues](../../issues)
- **Telegram** - [@iSponsorBlockTV](https://t.me/iSponsorBlockTV)
- **Обсуждения** - [GitHub Discussions](../../discussions)

## 📜 Лицензия

Этот проект распространяется под лицензией MIT.

---

**Наслаждайтесь YouTube без рекламы! 🎉**

