# Stage 01 常见注意点

- Go 未使用的 import / 局部变量会导致编译错误。
- 命名推荐 camelCase：`secondMax`，不是 snake_case。
- `range` 语法是 `for i, v := range xs`。
- map 不保证遍历顺序。
- `append` 返回新的 slice header，要接住返回值。
- `string[i]` 是 byte；处理中文不要把它当字符。
- `range string` 的 value 是 rune。
- 空字符串、空 slice、单元素都应该主动测试。
- 二分查找必须保证每轮区间严格缩小。
- 复杂度分析要区分时间与额外空间。
