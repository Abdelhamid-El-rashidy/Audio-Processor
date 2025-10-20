# 🎛 Audio Processor

A simple audio processing application built with **C++** and **JUCE**, supporting **cross-platform builds** (Linux, macOS, Windows).

---

## 🧩 Cloning the Project with JUCE Submodule

This project uses **JUCE** as a Git submodule. To clone it properly:

### Step 1 — Clone the Repository

You can use **Git GUI** (GitHub Desktop, Sourcetree) or terminal:

```bash
git clone --recurse-submodules https://github.com/Abdelhamid-El-rashidy/Audio-Processor.git
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

💡 **Notes:**

* The `JUCE` folder appears after initialization; **do not modify or push changes** from inside it.
* To update JUCE to the latest version:

```bash
cd JUCE
git pull origin master
cd ..
git add JUCE
git commit -m "Update JUCE submodule"
git push
```

---

## ⚙️ Build Instructions (Cross-Platform, Minimal Terminal)

### 🧱 Option 1 — Build with CLion (Recommended)

1. **Open CLion**.
2. Click **“Open Project”** → select `Audio Processor/`.
3. CLion will detect **CMakeLists.txt** and **reload CMake** automatically.
4. Select **Debug** or **Release** build.
5. Click **Run ▶️** — CLion will compile and launch the JUCE app.

> ✅ This works on **Linux, macOS, and Windows**.

---

### 🐧 Linux (Ubuntu/Debian) Dependencies

Before building:

```bash
sudo apt install libasound2-dev libfreetype6-dev libx11-dev libxrandr-dev \
libxinerama-dev libxcursor-dev libxi-dev
```

You can then build manually (optional):

```bash
mkdir -p build && cd build
cmake ..
make -j$(nproc)
./AudioProcessor
```

---

### 🍏 macOS Dependencies

Install **Homebrew** and required libraries:

```bash
brew install freetype libsndfile pkg-config
```

Then you can build manually (optional):

```bash
mkdir -p build && cd build
cmake ..
cmake --build .
./AudioProcessor
```

---

### 🪟 Windows Dependencies

1. **Install Visual Studio Community**:

  * Workload: **Desktop development with C++**
  * Optional components: MSVC C++ Compiler, Windows SDK, CMake tools for Windows

2. **Install Git for Windows** (if not already installed) to clone the project.

3. Open **CLion** → select `Audio Processor/`. CLion detects CMake automatically.

4. Select **Debug** or **Release**, then click **Run ▶️**.

> ⚡ Terminal commands are optional on Windows; all building is handled via CLion + Visual Studio compiler.

---
