# 🎧 Audio Processor

This project is part of **CS213 - Object Oriented Programming (Cairo University)**.
It is a C++ application built using the **JUCE Framework**, providing various **audio processing** functionalities with a GUI interface.

---

## 🚀 Project Setup

### 1. Clone the Repository

Clone the project along with its submodules (JUCE framework):

```bash
git clone --recursive https://github.com/<your-username>/Audio-Processor.git
cd Audio-Processor
```

If you forgot to use `--recursive`, run:

```bash
git submodule update --init --recursive
```

---

## 🧩 Build Instructions

### Using CMake (Recommended)

1. Create a build directory:

   ```bash
   mkdir -p build/Debug
   cd build/Debug
   ```

2. Configure and build the project:

   ```bash
   cmake ../..
   make
   ```

3. Run the executable:

   ```bash
   ./AudioProcessor
   ```

---

## 🧠 Submodule Update Guide

If the **JUCE** submodule appears modified or empty, make sure it’s properly synced:

```bash
git submodule update --init --recursive
```

This ensures JUCE’s source is fetched and consistent with the project.

---

## 🛠️ Folder Structure

```
Audio-Processor/
│
├── Source/               # Main source code (.cpp/.h)
├── CMakeLists.txt        # CMake configuration
├── JUCE/                 # JUCE framework (submodule)
├── build/                # Local build directory (ignored in git)
├── README.md             # Project documentation
└── resources/            # Images, icons, and assets
```



