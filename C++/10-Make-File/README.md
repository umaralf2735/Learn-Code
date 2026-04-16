# 10 - CMake System

Kompilasi pakai `g++ file.cpp -o app` bakal merepotkan banget buat proyek game besar. Maka kita butuh CMake builder.

Bikin `CMakeLists.txt`:
```cmake
cmake_minimum_required(VERSION 3.10)
project(GameBesar)

add_executable(GameSaya main.cpp)
```
Tinggal `cmake .` dan `make`, kelar! C++ Modern sekarang sangat nyaman.
---
[⬅️ Sebelumnya](../09-Template-Generics/README.md) | [🏠 Daftar Isi Utama](../README.md)
