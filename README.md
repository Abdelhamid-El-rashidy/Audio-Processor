## 🧩 Cloning the Project with JUCE Submodule

This project uses **JUCE** as a Git submodule.
To clone it properly with all dependencies, run:

```bash
git clone --recurse-submodules https://github.com/Abdelhamid-El-rashidy/Audio-Processor.git
```

If you already cloned it without the submodule, run:

```bash
git submodule update --init --recursive
```

### 💡 Notes

* The JUCE folder will appear after initialization (not stored directly in this repo).
* Do **not** modify or push changes from inside the `JUCE` folder.
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

## ⚙️ Build Instructions

### 🧱 Option 1 — Build with CLion (Recommended)

1. Open **CLion**.
2. Select **“Open Project”** and choose the folder `Audio Processor/`.
3. CLion will automatically detect your **CMakeLists.txt**.
4. Set the build configuration to **Debug** or **Release**.
5. Click **Run ▶️** to build and launch the JUCE application.

> 💡 Make sure to install dependencies before building:
>
> ```bash
> sudo apt install libasound2-dev libfreetype6-dev libx11-dev libxrandr-dev \
> libxinerama-dev libxcursor-dev libxi-dev
> ```

---

### 🧰 Option 2 — Build from Terminal

If you prefer to build manually without CLion:

```bash
# 1. Create build directory
mkdir -p build && cd build

# 2. Configure with CMake
cmake ..

# 3. Compile
make -j$(nproc)

# 4. Run the app
./AudioProcessor
```
