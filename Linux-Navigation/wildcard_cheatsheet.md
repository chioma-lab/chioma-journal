
# 📝 Wildcard Cheatsheet (Linux Shell - Bash)

Wildcards (also called "globs") are used in Unix/Linux shells to match patterns in filenames.

---

## 🔹 Basic Wildcards

| Pattern     | Meaning                                          | Example Match            |
|-------------|--------------------------------------------------|---------------------------|
| `*`         | Matches **zero or more characters**              | `*.txt` → `doc.txt`, `a.txt` |
| `?`         | Matches **exactly one character**                | `file?.txt` → `file1.txt`, `fileA.txt` |
| `[]`        | Matches **any one of the characters** inside     | `file[123].txt` → `file1.txt`, `file3.txt` |
| `[^]`       | Matches **any one character NOT** listed inside  | `file[^a].txt` → `fileb.txt`, `file1.txt` |

---

## 🔹 Examples

```bash
cp *.jpg images/         # Copy all .jpg files to images folder
rm temp?.txt             # Remove temp1.txt, tempA.txt, but not temp12.txt
mv file[1-3].md docs/    # Move file1.md, file2.md, file3.md to docs/
ls data*.csv             # List all CSV files starting with 'data'
```

---

## 🔹 Notes

- Wildcards expand **only in the shell** — not inside quotes.
- You can **escape wildcards** with `\` if you want to use them literally.
- When a wildcard pattern doesn’t match anything, it may return an error or do nothing depending on your shell settings.

---

Happy scripting! 🚀

