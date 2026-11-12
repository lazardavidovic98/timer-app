
# ⏱ Timer Application

This project is a cross-platform desktop application developed using **C++** and **Qt6**, providing functionality for three core timekeeping tools:
- **Timer** – counts down from a given time.
- **Stopwatch** – measures elapsed time with split functionality.
- **Alarm** – alerts the user at a set time.

## 🗂 Project Structure


<!-- project-tree:start -->
<p>
<a href="https://github.com/LazarDavidovic98/timer-app" title="timer-app"><img src=".github/readme-tree/00.svg" alt="timer-app" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app.sln" title="timer-app.sln"><img src=".github/readme-tree/01.svg" alt="timer-app.sln — Visual Studio solution" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/tree/main/timer-app" title="timer-app/"><img src=".github/readme-tree/02.svg" alt="timer-app/ — Qt 6 sources: a model and a panel per tool" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/main.cpp" title="timer-app/main.cpp"><img src=".github/readme-tree/03.svg" alt="timer-app/main.cpp — entry point" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/MainWindow.cpp" title="timer-app/MainWindow.cpp"><img src=".github/readme-tree/04.svg" alt="timer-app/MainWindow.cpp — tabs: Timer, StopWatch, Alarm" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/TimerModel.cpp" title="timer-app/TimerModel.cpp"><img src=".github/readme-tree/05.svg" alt="timer-app/TimerModel.cpp — countdown logic" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/TimerPanel.cpp" title="timer-app/TimerPanel.cpp"><img src=".github/readme-tree/06.svg" alt="timer-app/TimerPanel.cpp — countdown UI" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/StopWatchModel.cpp" title="timer-app/StopWatchModel.cpp"><img src=".github/readme-tree/07.svg" alt="timer-app/StopWatchModel.cpp — elapsed time and splits" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/StopWatchPanel.cpp" title="timer-app/StopWatchPanel.cpp"><img src=".github/readme-tree/08.svg" alt="timer-app/StopWatchPanel.cpp — stopwatch UI" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/SplitPanel.cpp" title="timer-app/SplitPanel.cpp"><img src=".github/readme-tree/09.svg" alt="timer-app/SplitPanel.cpp — list of split times" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/AlarmModel.cpp" title="timer-app/AlarmModel.cpp"><img src=".github/readme-tree/10.svg" alt="timer-app/AlarmModel.cpp — alarms and trigger check" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/AlarmPanel.cpp" title="timer-app/AlarmPanel.cpp"><img src=".github/readme-tree/11.svg" alt="timer-app/AlarmPanel.cpp — alarm UI" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/SoundEngine.cpp" title="timer-app/SoundEngine.cpp"><img src=".github/readme-tree/12.svg" alt="timer-app/SoundEngine.cpp — plays the alarm sound" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/timer_model_test.cpp" title="timer-app/timer_model_test.cpp"><img src=".github/readme-tree/13.svg" alt="timer-app/timer_model_test.cpp — console test for TimerModel" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/timer-app/timer-app.vcxproj" title="timer-app/timer-app.vcxproj"><img src=".github/readme-tree/14.svg" alt="timer-app/timer-app.vcxproj — Visual Studio + Qt VS Tools project" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/tree/main/timer-app/resources" title="timer-app/resources/"><img src=".github/readme-tree/15.svg" alt="timer-app/resources/ — icons, alarm.wav, resources.qrc" align="top"></a><br>
<a href="https://github.com/LazarDavidovic98/timer-app/blob/main/docs/Documentation.md" title="docs/Documentation.md"><img src=".github/readme-tree/16.svg" alt="docs/Documentation.md — design and implementation notes" align="top"></a><br>
</p>

<sub>Every row is a link to that file or folder on GitHub. Purple: folders, green: source code, grey: configuration, data and docs.</sub>
<!-- project-tree:end -->

## How to Build

### Requirements
- **Qt 6.x** (e.g. 6.6.3) with `mingw_64` or MSVC toolchain
- **CMake >= 3.14**
- **Visual Studio 2022** or **Visual Studio Code**
- Compiler: MinGW or MSVC

### Build with CMake
```bash
mkdir build
cd build
cmake .. -DCMAKE_PREFIX_PATH="C:/Qt/6.6.3/mingw_64"
cmake --build .
```

### Run
```bash
./TimeApp.exe
```

## Features

-  Start, Stop, Reset for Timer and Stopwatch
-  Alarm scheduling with toggle
-  Display of time splits for Stopwatch
-  Resource loading via `.qrc` file (icons, sounds)
-  Modular architecture

## Notes

- Font rendering warnings (e.g., `CreateFontFaceFromHDC()`) may occur on Windows. They do not impact functionality.
- If using Visual Studio, make sure the `.qrc` file is set to `Qt Resource File` in properties.

---

**Detailed documentation is available here**: [Documentation](docs/Documentation.md)

Developed as an educational project to explore GUI development in C++ using Qt.
