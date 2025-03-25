# 3.21
std::copy的用法 是一个标准库算法，通常用于从一个容器复制元素到另一个容器。std::copy需要三个参数：两个指定要复制的元素范围的迭代器（起始迭代器和结束迭代器），以及一个指向目标位置开始的迭代器。 指针也是一种天然的迭代器

```
std::copy(other.elements, other.elements + size, elements);
```