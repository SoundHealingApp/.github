# 🧘‍♀️ SoundWellnessApp

![Swift](https://img.shields.io/badge/Swift-5.9-FA7343?logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-4.0-1E90FF?logo=swift&logoColor=white)
![iOS](https://img.shields.io/badge/iOS-17+-000000?logo=apple&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-7.0-512BD4?logo=.net&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-7.0-512BD4?logo=.net&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?logo=postgresql&logoColor=white)

## 🌟 О приложении
SoundWellness - это  iOS-приложение для:
- Глубоких медитативных практик
- Научно-обоснованной звуковой терапии (Sound Bathing)

## 🔥 Ключевые особенности
  🎵 **Уникальные аудиопрограммы** с использованием:
  - Тибетских поющих чаш
  - Гонгов
  - Натуральных природных звуков
  
  🧠 **Научный подход**:
  - Специально подобранные частоты
  - Доказанная эффективность для:
    - Снижения стресса
    - Улучшения сна
    - Гармонизации состояния
    
## 🌟 Возможности

- 🎧 **Медитативные аудиосессии** — успокаивающие звуки, вибрации и голосовые практики.
- 🌄 **Цитата дня** — вдохновляющие мысли при первом запуске приложения.
- 🧭 **Онбординг** — плавное введение в возможности приложения.
- 📝 **Опросы** — определение текущего состояния пользователя для персональных рекомендаций.
- 🔴 **Прямые эфиры** — трансляции с экспертом прямо в приложении.
- 🔔 **Уведомления** — ежедневные напоминания о медитации.

## ⚙️ Технологии

### Клиентская часть (iOS)
- 📱 Swift
- 🎨 SwiftUI
- 🛠 Xcode
- 🔐 Keychain для хранения чувствительных данных
- 🔉 AVFoundation

### Серверная часть (Backend)
- 💻 C#
- 🌐 ASP.NET Core
- 🗃 PostgreSQL (через Docker)
- 🧩 Entity Framework Core (ORM)
- ☁️ Amazon S3 — для хранения медиафайлов
- 🔐 Microsoft Azure Key Vault — для хранения секретов (ключей и токенов)

## 🚀 Установка и запуск

### 📦 Сервер (локально)

1. Клонируйте репозиторий:

   ```bash
   git clone https://github.com/SoundHealingApp/SoundBathing_Server.git
   cd SoundBathing_Server
   ```

2. Поднимите базу данных с помощью Docker:

   ```bash
   docker-compose up -d
   ```

   ⚠️ Убедитесь, что установлен Docker и запущен Docker Desktop.

3. Перейдите в директорию `SoundHealing.Api` и выполните:

   ```bash
   dotnet restore
   dotnet run
   ```

4. Откройте Swagger по адресу:

   [https://localhost:7035/index.html](https://localhost:7035/index.html)

---

### 📱 Клиент (iOS-приложение)

1. Клонируйте репозиторий:

   ```bash
   git clone https://github.com/SoundHealingApp/SoundBathing_Mobile.git
   cd SoundBathing_Mobile
   ```

2. Откройте проект в Xcode.

3. Убедитесь, что установлены:
   - iOS симулятор 17+
   - зависимости:
     - `JWTDecode`
     - `SwiftKeychainWrapper`

4. Если используется локальный сервер, измените хост в `NetworkManager` на:

   ```swift
   let baseURL = "https://localhost:7035"
   ```

5. Нажмите **Run** в Xcode.
