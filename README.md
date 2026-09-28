# lesson1

Reborn 视觉组第一讲练习项目：使用 C++17 编写并构建一个命令行问候程序。

## 环境

- Ubuntu
- GCC/G++（支持 C++17）
- CMake 3.16 或更高版本

## 构建

直接使用 g++：

```bash
g++ -std=c++17 -Wall -g main.cpp -o hello
```

使用 CMake：

```bash
cmake -S . -B build
cmake --build build
```

## 运行示例

给程序传入一个名字：

```bash
./hello Alice
```

预期输出，退出状态为 0：

```text
Hello, Alice!
```

名字中含空格时用引号将其作为一个参数：

```bash
./hello "RM Vision"
```

预期输出，退出状态为 0：

```text
Hello, RM Vision!
```

## 错误输入

没有传入名字：

```bash
./hello
```

预期输出到标准错误，退出状态为 1：

```text
Usage: ./hello <name>
```

传入两个未合并的名字：

```bash
./hello Alice Bob
```

预期输出到标准错误，退出状态为 1：

```text
Usage: ./hello <name>
```

程序要求恰好传入一个名字参数。`.gitignore` 忽略 g++ 生成的 `hello` 和 CMake 的 `build/` 构建目录。
