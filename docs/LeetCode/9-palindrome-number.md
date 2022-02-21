# PalindromeNumber

`回文数`

> 给你一个整数 `x` ，如果 `x` 是一个回文整数，返回 `true` ；否则，返回 `false` 。

回文数是指正序（从左向右）和倒序（从右向左）读都是一样的整数。例如，`121` 是回文，而 `123` 不是。

示例 1：

```text
输入：x = 121
输出：true
```

示例 2：

```text
输入：x = -121
输出：false
解释：从左向右读, 为 -121 。 从右向左读, 为 121- 。因此它不是一个回文数。
```

示例 3：

```text
输入：x = 10
输出：false
解释：从右向左读, 为 01 。因此它不是一个回文数。
```

示例 4：

```text
输入：x = -101
输出：false
```

## `Case 1`

```ts
const isPalindrome = (x: number): boolean => {
  if (x < 0) {
    return false;
  }

  let num = parseInt(x.toString().split('').reverse().join(''));
  if (num === x) {
    return true;
  }
  return false;
};
```