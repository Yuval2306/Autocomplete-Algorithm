# 🔍 AutoComplete System

A fast and efficient autocomplete search engine that finds sentences in text files, even when you make typos.

## ✨ What It Does

- 🔎 Searches through text files to find matching sentences
- ⭐ Returns top 5 results ranked by relevance  
- 🐛 Handles typos (one letter wrong, missing letters, extra letters)
- ⚡ Caches results for fast loading on next run

## 🚀 Quick Start

### First Run
```bash
python main.py /path/to/your/text/files
```
This scans all `.txt` files and creates a cache.

### Search
```
[buffer] > hello
1. (score=10) Hello world example -- texts/file.txt (line 0)
2. (score=8) Hello friend -- texts/file.txt (line 5)

[buffer] > heloo
1. (score=8) Hello world example -- texts/file.txt (line 0)

[buffer] > #
Buffer reset.
```

## 📁 Project Structure

```
Autocomplete-Algorithm/
├── 📄 autocomplete.py          # Core search engine
├── 📄 initialize.py            # Cache management
├── 📄 main.py                  # CLI interface
├── 🧪 unit_test.py             # 25+ unit tests
├── 🧪 intergration_test.py      # 8+ integration tests
└── 📖 README.md                # This file
```

## 🧠 How It Works

1. **📖 Reads** all `.txt` files from your folder
2. **🗂️ Indexes** them by breaking words into 3-letter chunks  
3. **💾 Caches** results so it loads super fast next time
4. **🔍 Searches** through indexed sentences when you type
5. **📊 Scores** results based on how well they match

**Example:** Typing "heloo" (typo) still finds "Hello world" with a small score penalty.

## ⚡ Performance

| Metric | Time |
|--------|------|
| First run (build index) | ~20 seconds |
| Reload (from cache) | 0.5 seconds |
| Search query | 0.01-0.05 seconds |

## 🧪 Testing

```bash
# Run all tests
python unit_test.py
python intergration_test.py
```

All tests pass ✅

## 📋 Requirements

- Python 3.7+
- No external packages needed

---

👨‍💻 **Author:** Yuval Boker  
Full-Stack & Software Developer
