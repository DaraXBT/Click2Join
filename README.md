# 🎫 TelePass
> Event Management System with Telegram Integration

TelePass is an advanced event management system that integrates with Telegram's platform to streamline registration and attendance tracking. Through an intuitive Telegram bot interface, participants can register and receive personalized QR codes, while organizers benefit from real-time attendance verification, secure data management, and efficient participant tracking.

## ✨ Key Features

### 🤖 Telegram Bot Integration
- Automated registration process
- Real-time data validation
- Instant QR code delivery

### 📊 Event Management
- Role-based access control (Admin/Registrar)
- Real-time attendance tracking
- QR code verification system

### 🔐 Security Features
- Secure data encryption
- Unique registration tokens
- Role-based permissions

## 🛠️ Technology Stack

- **Backend:** Spring Boot 3.x
- **Database:** PostgreSQL
- **Integration:** Telegram Bot API
- **Build Tool:** Gradle
- **Java Version:** JDK 17

## 🚀 Getting Started

### Prerequisites
```bash
- Java 17+
- PostgreSQL 12+
- Telegram Bot Token
- Gradle 7+
```

### Installation
```bash
# Clone repository
git clone https://github.com/yourusername/telepass.git

# Navigate to project directory
cd telepass

# Build project
./gradlew build

# Run application
./gradlew bootRun
```

### Configuration
Create `application.properties`:
```properties
# Database
spring.datasource.url=jdbc:postgresql://localhost:5432/tb
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}

# Telegram Bot
telegram.bot.token=${BOT_TOKEN}
telegram.bot.username=${BOT_USERNAME}
```

## 📝 Documentation

### Database Schema
```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    phone_number VARCHAR(20) NOT NULL UNIQUE,
    full_name VARCHAR(100) NOT NULL,
    gender VARCHAR(10),
    date_of_birth DATE,
    address TEXT,
    email VARCHAR(100),
    occupation VARCHAR(100),
    registration_token VARCHAR(100) UNIQUE
);
```

### Basic Usage
1. Start registration with `/register` command
2. Complete registration form
3. Receive unique QR code
4. Present QR code at event

## 🤝 Contributing
Contributions are welcome. Please read our contributing guidelines before making a pull request.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact
- **Developer:** [Your Name]
- **Email:** your.email@example.com
- **Project Link:** https://github.com/yourusername/telepass

---

<div align="center">
  <sub>Built with ❤️ for better event management</sub>
</div>
