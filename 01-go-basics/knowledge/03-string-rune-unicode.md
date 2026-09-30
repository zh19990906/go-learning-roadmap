# String / byte / rune / Unicode

## 核心结论

Go 的 string 本质上是一串 UTF-8 字节。

```go
s := "中国"
len(s) // 通常是 6：字节数
```

`s[i]` 返回 `byte`，不是完整 Unicode 字符。

## byte

`byte` 是 `uint8` 的别名，表示一个字节。

```go
s := "abc"
fmt.Println(s[0])       // 97
fmt.Printf("%c\n", s[0]) // a
```

## rune

`rune` 是 `int32` 的别名，通常表示 Unicode code point。

```go
chars := []rune("中国")
len(chars) // 2
```

Python 3 的 `"中国"[0]` 直接得到字符；Go 的 `string[0]` 得到 byte，这是一处重要差异。

## range string

```go
for _, ch := range "a中b" {
    fmt.Printf("%T %c\n", ch, ch)
}
```

这里的 `ch` 本身就是 rune，因此可以直接传给 `unicode` 包。

## unicode 常用判断

```go
unicode.IsLetter(ch)
unicode.IsDigit(ch)
unicode.IsNumber(ch)
unicode.IsSpace(ch)
unicode.IsPunct(ch)
unicode.IsUpper(ch)
unicode.IsLower(ch)
unicode.IsControl(ch)
unicode.IsPrint(ch)
unicode.IsGraphic(ch)
```

转换：

```go
unicode.ToLower(ch)
unicode.ToUpper(ch)
unicode.ToTitle(ch)
```

Python 对照：

```text
str.isalpha()  -> unicode.IsLetter
str.isdigit()  -> unicode.IsDigit
str.isspace()  -> unicode.IsSpace
str.lower()    -> unicode.ToLower（逐 rune）
str.upper()    -> unicode.ToUpper（逐 rune）
```

## 注意

- `range string` 得到 rune，但 index 仍是字节位置。
- 需要按字符下标随机访问时，先转 `[]rune(s)`。
- rune 是码点，不等同于所有“人眼字符”；emoji/组合字符可能更复杂。