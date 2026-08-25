# AGENTS.md

Soc Ops — a social bingo game for in-person mixers.

## ✓ Development Checklist

Before committing changes:
- [ ] `cd socops && ./mvnw clean package` (build)
- [ ] `./mvnw test` (test)
- [ ] `./mvnw spring-boot:run` (verify UI on port 8080)

## Quick Start

- Java 21 required
- Run: `cd socops && ./mvnw spring-boot:run`
- Test: `./mvnw test`

## Key Files

- App: [socops/src/main/java/com/socops/SocOpsApplication.java](socops/src/main/java/com/socops/SocOpsApplication.java)
- Routes: [socops/src/main/java/com/socops/web/BingoRestController.java](socops/src/main/java/com/socops/web/BingoRestController.java)
- Logic: [socops/src/main/java/com/socops/service/BoardAssembler.java](socops/src/main/java/com/socops/service/BoardAssembler.java)
- UI: [socops/src/main/resources/templates/game.html](socops/src/main/resources/templates/game.html)
- CSS: [socops/src/main/resources/static/css/app.css](socops/src/main/resources/static/css/app.css)

## Architecture

Spring Boot MVC with Thymeleaf. Business logic in service layer (pure, testable). Front-end is static HTML + embedded JavaScript. Styling uses custom utility classes ([css-utilities.instructions.md](.github/instructions/css-utilities.instructions.md)) and distinctive design patterns ([frontend-design.instructions.md](.github/instructions/frontend-design.instructions.md)).

## Notes

- Tests: [BoardAssemblerTests.java](socops/src/test/java/com/socops/service/BoardAssemblerTests.java) — follow this style
- Win detection: rows, columns, diagonals, center free-space
- Workshop: [workshop/GUIDE.md](workshop/GUIDE.md)
