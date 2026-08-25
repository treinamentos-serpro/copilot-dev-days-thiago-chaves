🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# Soc Ops

A social bingo game for in-person mixers.
Break the ice, spark real conversations, and race to 5 in a row.

> 🎯 **Perfect for workshops, onboarding events, and team meetups**

📚 **[Start the Lab Guide](workshop/GUIDE.md)**

---

## Why Soc Ops?

- 🧊 **Instant icebreakers** with prompt-based bingo cards
- 👥 **Built for groups** in real-life social settings
- ⚡ **Fast setup** with Spring Boot + Maven Wrapper
- 🧪 **Workshop-ready** with step-by-step labs

## Quick Start

### Prerequisites

- [Java 21 JDK](https://adoptium.net/) or higher
- [Apache Maven 3.9+](https://maven.apache.org/) (or use the included Maven Wrapper)

### Run locally

```bash
cd socops
./mvnw spring-boot:run
```

Then open **http://localhost:8080**.

### Build & test

```bash
cd socops
./mvnw clean package
./mvnw test
```

---

## 📚 Workshop Path

| Part | Title |
|------|-------|
| [**00**](workshop/00-overview.md) | Overview & Checklist |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering |
| [**02**](workshop/02-design.md) | Design-First Frontend |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## Project Structure

- App entrypoint: [`socops/src/main/java/com/socops/SocOpsApplication.java`](socops/src/main/java/com/socops/SocOpsApplication.java)
- API routes: [`socops/src/main/java/com/socops/web/BingoRestController.java`](socops/src/main/java/com/socops/web/BingoRestController.java)
- Game logic: [`socops/src/main/java/com/socops/service/BoardAssembler.java`](socops/src/main/java/com/socops/service/BoardAssembler.java)
- UI template: [`socops/src/main/resources/templates/game.html`](socops/src/main/resources/templates/game.html)

Deploys automatically to GitHub Pages on push to `main`.
