# Some cpp examples
## Include files
### print.hpp
```cpp
#include <fstream>
#include <iostream>
#include <string>

void print(const std::string& text, std::ofstream& out);
void print(const std::string& text, std::ostream& out = std::cout);
```
### print.cpp
```cpp
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}

void print(const std::string& text, std::ofstream& out)
{
  out << text;
}
```
## Main files
### example1.cpp
```cpp
#include <print.hpp>

int main(int argc, char** argv)
{
  print("hello");
}
```
### example2.cpp
```cpp
#include <print.hpp>

#include <fstream>

int main(int argc, char** argv)
{
  std::ofstream file("log.txt");
  print(std::string("hello"), file);
}

```

