# 🛠️ Wrangler - Custom Directive Parsing Enhancements

This project is part of an assignment to extend and improve the Wrangler project by adding support for new grammar rules in `Directives.g4`, updating the parser logic, and integrating the changes into the Wrangler Core.

---

## 🚀 What Was Done

- ✅ Modified `Directives.g4` to include new rules: `ByteSizeArg`, `TimeDurationArg`
- ✅ Regenerated ANTLR parser files with `antlr-4.13.1-complete.jar`
- ✅ Implemented visitor methods in `wrangler-core` for new rules:
  - `visitByteSizeArg`
  - `visitTimeDurationArg`
- ✅ Updated `TokenGroup` logic to support new tokens
- ✅ Created JUnit test cases for the new grammar parsing logic
- ✅ Successfully compiled and verified the project using Maven

---

## 📦 Deliverables Checklist

- ✅ Modified `Directives.g4`
- ✅ All new and modified `.java` files in `wrangler-api` and `wrangler-core`
- ✅ Unit test files added in `wrangler-core/src/test/java/...`
- ✅ Successful build and test execution (`mvn clean install`)
- ✅ AI tool usage log in [`prompts.txt`](./prompts.txt)

---

## 🧪 Build & Run Instructions

### 🔧 Prerequisites
- Java 8 or above
- Maven
- [ANTLR v4.13.1](https://www.antlr.org/download.html)

### 🔁 Regenerate Parser (if needed)

```bash
java -jar tools/antlr-4.13.1-complete.jar -Dlanguage=Java -visitor wrangler-core/src/main/antlr4/io/cdap/wrangler/parser/Directives.g4 -o wrangler-core/src/main/java/io/cdap/wrangler/parser/gen
