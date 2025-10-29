# Slim64FS

**Slim64FS** is an open filesystem architecture built as a modern alternative to FAT32 and exFAT — maintaining their simplicity while removing their limits.

---

## 🧠 Concept

Slim64FS follows the **64/4 principle** — focusing on the 4% of features that yield 64% of real-world usability.  
It is designed for embedded devices, external storage, and AI-era distributed systems that require:

- **O(1) metadata lookup**
- **CRC-based pseudo-journaling**
- **64-bit volume and file size support**
- **Portable FUSE reference implementation (C)**
- **Apache-2.0 license**

---

## 🧩 Structure

| Directory | Purpose |
|------------|----------|
| `src/` | Core filesystem source code (C / FUSE3 baseline) |
| `docs/` | Specs, RFC drafts, whitepapers |
| `tests/` | Integration and unit tests |
| `examples/` | Mounting and utility demos |
| `tools/` | Build helpers, test harness, utilities |

---

## 🚀 Compile & Mount (Preview)

```bash
sudo apt install libfuse3-dev build-essential
git clone https://github.com/YOURNAME/Slim64FS.git
cd Slim64FS/src
make
mkdir /tmp/slim64
./slim64fs /tmp/slim64
