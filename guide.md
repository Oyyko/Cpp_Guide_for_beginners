## Cpp guide for beginners

By USTC Cpp

### 推荐入门书目：

不是很推荐大名鼎鼎的《C++ Primer》，这更多像一本工具书而不是入门书。它最大的问题就是不按顺序讲，经常会在前面的代码中遇到后面的特性。而且目前第五版只讲授到C++11，略有些落后。

推荐书目如下（按顺序阅读）：

C++17入门经典 https://book.douban.com/subject/34439378/

Effective Modern C++ https://book.douban.com/subject/26793803/

C++并发编程实战（第2版） https://book.douban.com/subject/35653912/

注：这本一定要买第二版，第一版翻译是几个外语系的，不懂任何代码的人翻译的，你可以想象翻译质量，，，第二版遇到翻译问题可以找我，我认识译者，可以帮忙说一下。

对C++的发展历史感兴趣的可以看一下：

C++ 程序设计语言（第 1 - 3 部分）（原书第 4 版） https://book.douban.com/subject/26857943/

现代C++白皮书 https://gitee.com/bexsder/Cxx_HOPL4_zh

关于C++和大学课程数据结构结合：

数据结构（清华邓俊辉）https://book.douban.com/subject/25859528/

### 常用网站

当你遇到问题想独立解决的时候，查阅顺序依次为：stackoverflow，cppreference，C++标准原文（求助群友当然是一个选项）

cppreference资料网站： https://en.cppreference.com/  

C++20标准： https://isocpp.org/files/papers/N4860.pdf

### 精进

可以观看CppCon会议的演讲，这是一个关于C++的年度会议，人们在此分享他们的感悟。

B站有转载 https://www.bilibili.com/video/BV1ha411k7pa

### 关于开发环境

每个人有自己适合的开发环境（ 

我比较推荐的是VSCode+clangd插件+cpplint插件

VSCode官方插件商店中有微软出品的一个Cpp插件，但其功能略逊于clangd。

`clangd`是一个基于clang的*语言服务器*，可以通过插件与许多编辑器一起工作。clangd集成了clang-tidy,会对你的代码风格做出指导。

cpplint是Google开发的一个C++代码风格检查工具，如果你的项目是遵循google code style的，可以使用cpplint作为代码规范的一个检查工具。

日常写一些代码的时候它们的一些代码风格提示很烦人，可以考虑先禁用这个插件，或者更改配置文件来取消不想要的风格纠正。

例如你可以在VSCode的`settings.json`里面加上

```json
"cpplint.filters": [
        "-legal/copyright",
        "-whitespace/ending_newline",
        "-whitespace/newline",
        "-build/namespaces",
    ]
```

来去掉一些烦人的提示

### 关于代码风格

如果你使用了clangd和cpplint 它们会帮你纠正一些代码风格的问题。

这里有一些常见的代码风格可以学习：

https://llvm.org/docs/CodingStandards.html

https://www.chromium.org/developers/coding-style/

https://google.github.io/styleguide/cppguide.html

我比较喜欢Chromium的