# OpenGL + GLFW Setup Guide (Visual Studio)

This project uses **OpenGL**, **GLFW**, and **Visual Studio (C++)**.

---

## Requirements

- Visual Studio 2019 / 2022
- GLFW Library
- OpenGL (comes with Windows SDK)

---

# Project Configuration

## 1. VC++ Directories

### Include Directories

Go to:

```
Project
→ Properties
→ VC++ Directories
→ Include Directories
```

Add:

```
OpenGL\Include
```

---

### Library Directories

Go to:

```
Project
→ Properties
→ VC++ Directories
→ Library Directories
```

Add:

```
OpenGL\Lib
```

---

## 2. C/C++ Settings

Go to:

```
Project
→ Properties
→ C/C++
→ General
→ Additional Include Directories
```

Add:

```
glfw\include
```

---

## 3. Linker Settings

### Library Directories

Go to:

```
Project
→ Properties
→ Linker
→ General
→ Additional Library Directories
```

Add:

```
glfw\build
```

---

### Additional Dependencies

Go to:

```
Project
→ Properties
→ Linker
→ Input
→ Additional Dependencies
```

Add:

```
glfw3.lib
opengl32.lib
```

or

```
glfw3.lib;opengl32.lib;
```

---

# Folder Structure

```
Project
│
├── OpenGL
│   ├── Include
│   └── Lib
│
├── glfw
│   ├── include
│   └── build
│
├── src
│   └── main.cpp
│
└── README.md
```

---

# Build

1. Open the solution in Visual Studio.
2. Configure the project settings as described above.
3. Select **x64** platform (recommended).
4. Build the project (`Ctrl + Shift + B`).
5. Run the project (`Ctrl + F5`).

---

# Linked Libraries

- `glfw3.lib`
- `opengl32.lib`

---

# Notes

- Ensure the architecture of GLFW (`x64` or `Win32`) matches your Visual Studio project configuration.
- If using a dynamic version of GLFW, place the required `glfw3.dll` beside the generated `.exe` file.
- If you built GLFW yourself, verify that the generated `.lib` files are located in the specified `build` directory.

---

## Author

**Md. Rasel Mahmud**
