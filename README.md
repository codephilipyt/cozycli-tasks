# CozyCLI Tasks

**CozyCLI Tasks** is the official catalog of practice tasks for [CozyCLI](https://cozycli.com) — a small, cozy tool to learn Linux commands by doing.

This repository contains a curated collection of tasks in a simple JSON format.
Each task describes a goal (e.g. *“List all files including hidden, detailed view”*) and the expected Linux command (e.g. `ls -la`), plus a short explanation and reference link.

The tasks power both:

* the **CozyCLI Trainer** (interactive practice tool)
* the **CozyCLI Cheatsheet** (reference lookup)

---

## 📂 Structure

All tasks are stored in a single JSON file:

```
questions_reduced.json
```

Each entry looks like this:

```json
{
    "id": 3,
    "desc": "Show the absolute path of the current working directory",
    "cmd": "pwd",
    "difficulty": "easy",
    "explanation": "Prints the full path of the current directory.",
    "category": "Filesystem",
    "tags": [
      "pwd",
      "path"
    ],
    "resource": {
      "title": "pwd man page",
      "url": "https://man7.org/linux/man-pages/man1/pwd.1.html"
    },
    "distros": [
      "core"
    ]
  }
```

### Fields

* **desc** → short description of the task
* **cmd** → expected Linux command (string)
* **difficulty** → `easy`, `medium`, or `hard`
* **explanation** → short explanation (1–3 sentences)
* **category** → broad group (`Filesystem`, `Networking`, `Text Processing`, …)
* **tags** → 1–2 simple tags (optional)
* **resource** → object with `{ "title": string, "url": string }` (or `"resource missing"`)
* **distros** → distro name or core linux commands

---

## 🤝 Contributing

Contributions are very welcome! 🎉

### How to add new tasks

1. **Fork** this repository
2. Edit `questions.json`

   * Add your tasks at the end of the array (please keep valid JSON)
   * Use the same structure as shown above
   * Keep explanations short and clear
3. **Commit** your changes
4. Open a **Pull Request**

We’ll review your PR, check formatting and correctness, and merge it once ready.

---

## ✅ Guidelines

* Stick to **real, working Linux commands** (tested on common distros)
* Prefer **concise, practical tasks** over niche or overly complex ones
* Keep explanations **short (1–3 sentences)**
* Provide a `resource` link if possible (usually the manpage, e.g. `https://man7.org/...`). If none exists, use `"title": "resource missing"`

---

## 📜 License

All tasks are provided under the [MIT License](LICENSE).
This dataset is open and free to use in other projects as well.
