# NISR Test Version: Features & Implementation Plan

This document outlines the minimum viable language (MVP) for NISR, the advanced features that show our ambition, tutorial priorities, language support, lessons from other languages, and a minimal implementation roadmap.

---

## 1. Must-have Language Features (MVP)

To make NISR usable from day one, the MVP must cover the essentials:

- **Lexical rules**: a tokenizer that understands identifiers, numbers, strings, comments, and brace-based blocks. Includes keyword mapping for English, Amharic, and Arabic.
- **Basic types**: integers, floats, booleans, strings, lists, maps, and `nil`.
- **Control flow**: `if/else`, `while`, and iterator-style `for` loops.
- **Functions**: flexible definitions (with or without `fun` keyword), parameters, default values, closures, and `__init__` for class constructors.
- **Modules**: import code from other files.
- **Error handling**: clear `try/catch` with meaningful messages.
- **I/O**: console printing and basic file operations.
- **Concurrency (lightweight)**: event loop with `async/await`.

> Together, these features give us a language that feels alive, not just a toy.

---

## 2. Advanced Features That Show Ambition

These features make NISR stand out:

- **AI-native hooks**: e.g., `ai.infer("sentiment", "I love NISR!")`.
- **Multilingual syntax**: write code in English, Amharic, or Arabic.
- **WASM support**: run NISR in the browser.
- **Optional typing (future)**: gradual typing for larger projects.

---

## 3. Features to Emphasize in the Tutorial

First tutorials set the tone. Highlight:

1. Multilingual “Hello World” — English, Amharic, Arabic.
2. Types and control flow.
3. Functions and modules — abstraction and reuse.
4. Classes with `__init__` — clean OOP introduction.
5. Error handling — catching mistakes gracefully.
6. Concurrency — simple `async` example to demonstrate modern power.

> AI-native parts can come later in an “advanced section” once basics are solid.

---

## 4. Languages to Include in the First Test Version

- **Human languages**: English (default), Amharic, Arabic.
- **Interop languages**: C (FFI), Python, WASM.

> This shows both cultural inclusivity and technical versatility.

---

## 5. Lessons from Other Languages’ First Versions

- **Python 0.9**: functions, classes, exceptions, modules; kept surface area small.
- **Java 1.0**: focused on OOP and JVM portability.
- **Go 1.0**: simplicity and concurrency (goroutines, channels).
- **Rust**: later, aimed at safety and performance.

> Compared to these, NISR’s MVP is modest — simple types, functions, modules, OOP, exceptions — but our **ambition layer** (multilingual keywords, AI hooks, WASM) makes it modern from the start.

---

## 6. Minimal Implementation Plan

### Phase 0 — Spec & Examples (week 0)
- Write grammar, keyword tables.
- Produce simple multilingual demos.

### Phase 1 — Lexer & Parser (weeks 1–2)
- Implement tokenizer with multilingual mapping.
- Parse into AST.

### Phase 2 — Interpreter/Runtime (weeks 2–3)
- AST interpreter for expressions, functions, OOP, and modules.

### Phase 3 — Errors + I/O (weeks 3–4)
- Add `try/catch`.
- Console I/O and file operations.

### Phase 4 — Concurrency (weeks 4–5)
- Event loop and `async/await`.

### Phase 5 — Tooling (weeks 5–6)
- REPL, CLI runner, basic formatter.

### Phase 6 — Ambition Demos (weeks 6–8)
- AI-native stub, WASM demo, multilingual tutorial.

### Phase 7 — Docs & Release (weeks 8–10)
- Full tutorial, demo video, repo polish.

**Roles**: language designer, parser/compiler engineer, runtime engineer, stdlib developer, interop engineer, docs lead, QA/CI.

**Engineering tasks**: build lexer, parser, AST evaluator, function call stack, OOP model, `try/catch`, async scheduler, AI stub, REPL, and test suite.

> Each milestone ends with a tangible demo — proving execution, not just ideas.
