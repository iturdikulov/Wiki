---
date: 2025-12-20 08:19
tags:
  - blog
---

## Golden path for my education and practice

Here is list of my projects and learning list for education, that keep me focused on my goals.

To avoid overwhelming effect, I keep this note simple as possible and hide not relevant or "future" tasks into related notes.

You can't learn all very quickly, this is marathon, not a sprint. Strategy:

1. Pick one topic and learn it deeply.
2. Apply it in practice.
3. Repeat, come back to previous projects and try to improve them!

## 1. Workflow and practice

### [[my_productivity_workflow|My productivity workflow]]

- WARN: **AI in nvim workflow:** Integrate AI tools (Copilot, Codeium) into Neovim carefully to enhance productivity without losing coding skills.
    - TODO: test completion, workflow to generate project
- TODO: Practice [[GNU_Readline]] keybindings

### [[projects|Active Projects]]

- PROJECT: [**chat_oracle**](https://github.com/iturdikulov/chat_oracle)
- PROJECT: own LLM-based system to search (nomic embeddings)
- PROJECT: [dev](https://github.com/iturdikulov/dev)
- PROJECT: [nvim](https://github.com/iturdikulov/nvim)

### [[my_awesome_software_list|Software]]

- TODO: **MCP in Docker:** Explore Model Context Protocol servers for context-aware AI interactions.
    - TODO: install hello-world MCP
    - TODO: registry of new MCP servers
- TODO: Review [[my_awesome_software_list]]

### [[LeetCode|DSA practice]]

- WARN: [Super Easy / Easy Problems](https://leetcode.com/) 
    - TODO: Solve first 3 problems
- TODO: [Advent of Code 2020](https://adventofcode.com/2020)
- TODO: [About - Project Euler](https://projecteuler.net/)

## 2. Science: Data Structures and Algorithms, Math

### [[computer_science|Computer Science]]

- WARN: [Learn Data Structures and Algorithms in Python [Full Course] | Boot.dev](https://www.boot.dev/courses/learn-data-structures-and-algorithms-python)
    - TODO: quick check previous chapters, prepare note
- WARN: [Beej's Guide to Learning Computer Science](https://beej.us/guide/bglcs/html/split/)
- WARN: Книга: *Code: The Hidden Language of Computer Hardware* — для понимания "железа".
- TODO: [Sorting Algorithms (Toptal)](https://www.toptal.com/developers/sorting-algorithms) — визуализация.
    - TODO: check first visualization, try to understandit
- TODO: [[Wengrow-Data_structures_and_algorithms]]
    - TODO: sync note with new book
- TODO: [[InterviewCake_Team-Coding_interview_practice]]
-   - TODO: check first chapter

### [[programming_foundations|Programming Foundations]]

- WARN: Книга: *Столяров "Азы программирования"* — структурное мышление.
    - TODO: sync with [[Stolyarov-Azy_programmirovaniya]]
- TODO: Книга: [[Abelson_and_Sussman-SICP]]
- TODO: **Lua:** Scripting for Neovim configuration and game logic.
- TODO: **Bash/Zsh:** Shell scripting, automation, and dotfiles management.
- TODO: [Beej's Guide to C Programming](https://beej.us/guide/bgc/html/split/)
- TODO: Книга: *Язык программирования C (Керниган, Ричи)* — для понимания работы памяти и указателей.
- TODO: [[C#Learning path]]
- TODO: [Go by Example](https://gobyexample.com/)

### [[mathematics|Mathematics]]

- WARN: Киселёв Алгебра, в 2-х частях
    - TODO: поиск практически задач
- TODO: Книга: No Bullshit Guide to Linear Algebra
- TODO: [BetterExplained.com](https://betterexplained.com/) — интуитивное понимание концепций.
- TODO: [[Math_is_fun_community-Math_is_fun]]
- TODO: [100 уроков Математики (А. Савватеев)](https://www.youtube.com/playlist?list=PLqBfxn8OBMGrsA_YynaQWqHKhL7kEvL4X)

## 3. AI & ML Engineering

- PROJECT: [Fine-tuning LLMs Guide | Unsloth Documentation](https://docs.unsloth.ai/get-started/fine-tuning-llms-guide)
- TODO: [Gemini CLI Hands-on](https://codelabs.developers.google.com/gemini-cli-hands-on?hl=ru#0)
- TODO: [Mistral Prompting Capabilities](https://docs.mistral.ai/capabilities/completion/prompting_capabilities) & Grok prompting tutor
- TODO: [Vector Similarity Search from Basics to Production](https://mlops.community/vector-similarity-search-from-basics-to-production/)
- TODO: **Inference:** Optimization techniques (quantization, pruning) for deploying models.

### Fundamentals & ML Basics

- WARN: Книга: *Deep Learning with Python (Francois Chollet)* — база по нейросетям (Keras/TensorFlow).
- TODO: **Math for AI:** Векторы, матрицы, косинусное сходство (Cosine Similarity).

### LLM Engineering & RAG

- WARN: boot.dev RAG course
- TODO: **LLM APIs:** OpenAI / Anthropic / Mistral / Gemini CLI.
- TODO: **RAG (Retrieval-Augmented Generation):**
    - TODO: Архитектура RAG (Chunking, Embedding, Retrieval, Generation).
    - TODO: **Vector Databases:** `pgvector` (внутри Postgres), Qdrant или ChromaDB.
    - TODO: [Vector Similarity Search Guide](https://mlops.community/vector-similarity-search-from-basics-to-production/).
- TODO: **Frameworks:**
    - TODO: **LangChain** или **LlamaIndex** — оркестрация цепочек.
    - TODO: **DSPy** — программирование промптов (тренд 2025).

### Fine-Tuning & Local Models

- TODO: **Fine-tuning:** [Unsloth Guide](https://docs.unsloth.ai/get-started/fine-tuning-llms-guide) (LoRA/QLoRA).
- TODO: **Inference:** Запуск локальных моделей (Ollama, vLLM).
- TODO: **Prompt Engineering:** Context caching, Chain-of-Thought.

## 4. [[backend#Learning path|Backend]]

### [[Python#Learning path|Python]]

- WARN: **AsyncIO:** Глубокое понимание event loop, coroutines, tasks. Это критично для FastAPI и AI.
- WARN: [The Hitchhiker’s Guide to Python](https://docs.python-guide.org/)
- WARN: boot.dev Python
- WARN: 99 Bottles of OOP
- WARN: [*Cosmic Python*](https://www.cosmicpython.com/book/preface.html) (Architecture Patterns) — главы про доменную модель.
- TODO: **Docs:** [Python Official FAQ](https://docs.python.org/3/faq/programming.html) — база.
- TODO: **Typing:** `TypedDict`, `Protocol`, Generics. Использование `mypy` / `pyright`.
- TODO: **Modern Structures:** `dataclasses` vs `Pydantic`.
- TODO: **Code Quality:** Линтеры (Ruff), форматтеры (Black/Ruff).
- TODO: [CS50's Introduction to Programming with Python](https://pll.harvard.edu/course/cs50s-introduction-programming-python)
- TODO: [Python Must Watch](https://github.com/s16h/py-must-watch)
- TODO: [Python Morsels](https://www.pythonmorsels.com/)

### Event-Driven Architecture (EDA)

- TODO: **Message Brokers:**
    - WARN: **RabbitMQ:** Exchange types, queues, dead letter exchanges. Library `aio-pika`.
    - TODO: **Kafka:** Basics, partitions, consumer groups. Книга: *Kafka Streams in Action*.
- TODO: **FastStream:** Modern framework for Kafka/RabbitMQ (must learn for Python in 2025).
- WARN: **Task Queues:** Celery (classic), AIO-pika.
- WARN: boot.dev pub/sub course
- TODO: [Bedzhek B. - Kafka Streams in Action. Applications and event-driven microservices.](https://rutracker.org/forum/viewtopic.php?t=6711317)
- TODO: [Apache Kafka Quickstart](https://kafka.apache.org/quickstart)
- TODO: [FastStream Article (Habr)](https://habr.com/ru/articles/822505/)

### Testing & Observability

- TODO: **Testing:** `pytest` (fixtures, markers), `testcontainers` (DB in docker for tests).
- TODO: vitest/jest

### API & Frameworks

- WARN: **Flask:** Обзорно (Flask Mega Tutorial), чтобы понимать легаси-код.
- TODO: **FastAPI:** Основной инструмент. Изучить Dependency Injection, Middleware, Background Tasks.
- WARN: **Pydantic V2:** Валидация данных, `.model_dump()`, сериализация, работа с `Settings` (.env).
- TODO: **Web Protocols:** HTTP/2, WebSockets, основы gRPC (важно для микросервисов).
- TODO: **WebSockets:** Implement WS services (e.g., Starlette/FastAPI websockets, aiohttp).
- TODO: [FastAPI Documentation](https://fastapi.tiangolo.com/)
- TODO: [Flask Documentation](https://flask.palletsprojects.com/) & [Flask Mega-Tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)
- TODO: [MDN Django Tutorial](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/Django)
- TODO: [FastAPI Tips: Use Lifespan State](https://github.com/Kludex/fastapi-tips?tab=readme-ov-file#6-use-lifespan-state-instead-of-appstate)
- TODO: [Django REST Framework Quickstart](https://www.django-rest-framework.org/tutorial/quickstart/) - Rewrite SQLite article notes for website column.
- TODO: **Pydantic Settings:** Configuration management using `pydantic-settings`.

### Data Layer

- WARN: Boot.dev SQL Course
- WARN: Книга: *The Art of PostgreSQL*
- WARN: **Redis:** Caching, pub/sub, message broker basics.
- TODO: [Asyncpg with FastAPI and Air](https://daniel.feldroy.com/posts/2025-10-using-asyncpg-with-fastapi-and-air)
- TODO: [Guide to SQL JOINs](https://kb.databasedesignbook.com/posts/sql-joins/)
- TODO: Indexes, transactions, isolation levels (ACID).
- TODO: **ORM:**
    - TODO: *Pony ORM* — optional (interesting, but less common in enterprise).
    - TODO: **Must Have:** **SQLAlchemy 2.0** (AsyncSession) — industry standard.
    - TODO: Migrations: **Alembic**.
- TODO: **NoSQL:**
    - TODO: **MongoDB** — document-oriented DB.
    - TODO: [Redis with Python & FastAPI](https://redis.io/learn/develop/python/fastapi)

### DevOps 

- WARN: **Linux:** Basic bash commands, scripting.
- WARN: **Linux Distributions:** Understand differences between Debian-based, RHEL-based, and Arch-based systems.
- TODO: **Monitoring:** Prometheus + Grafana (metrics), Sentry (error tracking).
- TODO: **Nginx:** Reverse proxy, load balancing, caching, and SSL configuration.
- TODO: **systemd:** Managing services, timers, and analyzing logs with journalctl.
- TODO: **CI/CD:** GitLab CI/CD or GitHub Actions basics.
- TODO: **Docker & Compose:** Writing optimized Dockerfiles (multi-stage builds).
- TODO: **Git:** Visualization, rebase vs merge, git flow.
    - TODO: [Git Visualization Guide (YouTube)](https://www.youtube.com/watch?v=C2aFC8wFp2A)
- TODO: **Kubernetes (K8s) Basics:** Pods, Deployments, Services, and local clusters (Minikube/Kind).

## 5. [[web_development#Learning path|Web development]]

- WARN: [Learn JavaScript [Full Course] | Boot.dev](https://www.boot.dev/courses/learn-javascript)
- WARN: [MDN JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Language_overview)
- WARN: [Learn JavaScript in Y Minutes](https://learnxinyminutes.com/javascript/)
- WARN: [Learn X in Y minutes (TypeScript)](https://learnxinyminutes.com/typescript/).
- TODO: ES6+ syntax (destructuring, arrow functions, promises).
- TODO: [Modern JavaScript Tutorial (RU)](https://learn.javascript.ru/)
- TODO: [web.dev](https://web.dev/) - Guidance for modern web development.
- TODO: **Node.js:** Runtime environment, Event Loop, File System API.

- WARN: **Vue 3 Ecosystem:**
    - [Vue.js Guide (RU)](https://ru.vuejs.org/guide/introduction.html)
    - TODO: **Composition API:** `<script setup>`.
    - TODO: **State:** Pinia.
    - TODO: **UI:** Vuetify or Tailwind CSS.
    - TODO: **Vue Router:** SPA routing, history mode, navigation guards.
    - TODO: **Build:** Vite tutorial.
    - TODO: **Testing:** Unit testing with Vitest or Jest.
    - TODO: **Integration:** Interaction with Flask, FastAPI (Axios/Fetch), JWT authorization, API client generation.

## 6. Architecture, High Load and Messaging

### Architecture Patterns

- TODO: [ByteByteGo - TODO: YouTube](https://www.youtube.com/@ByteByteGo/videos)
    - TODO: pick 1 video
- TODO: **Design Patterns:** *Head First Design Patterns* (Adapter, Factory, Strategy, Singleton).
- TODO: **Clean Architecture:** 3-layer architecture (Controller -> Service -> Repository).
- TODO: **SOLID:** Principles, especially Liskov Substitution (examples in Python).
- TODO: **Common App Patterns:** Repository pattern, Service layer, Dependency Injection examples.

## 7. Lists & collection of courses

- [Computer Science Roadmap](https://roadmap.sh/computer-science)
- [Frontend Developer Roadmap](https://roadmap.sh/frontend)
- [Backend Developer Roadmap](https://roadmap.sh/backend)
- [Boot.dev](https://boot.dev/)
- [Техносфера - Мир программирования](https://www.technosphera.ru/lib/8)
- [Pragmatic Bookshelf](https://pragprog.com/)
- [The Odin Project](https://www.theodinproject.com/)
- [Professional Programming Resources](https://github.com/charlax/professional-programming)
- [Full Stack Open](https://fullstackopen.com/en/)
- [Exercism](https://exercism.org/tracks)

## 8. Hobby & Education

- [[computer_graphics#Learning path|Computer graphics]]
- [[art#Learning path]] is a great way to express my thoughts in easy to understand form, and I want to do it better
- [[mathematics#Learning path]]
- [[physics#Learning path]]
- [[Russian#Learning path]] and [[English#Learning path]]
- [[history|History]] is improving your understanding of current world events and help to avoid mistakes from past.
