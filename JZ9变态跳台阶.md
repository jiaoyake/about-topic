> 时间限制：C/C++ 1秒，其他语言2秒 
> 空间限制：C/C++ 32M，其他语言64M 
> 热度指数：544977
> 本题知识点： 贪心
### 题目描述
一只青蛙一次可以跳上1级台阶，也可以跳上2级……它也可以跳上n级。求该青蛙跳上一个n级的台阶总共有多少种跳法。
### 代码
```javascript
function jumpFloorII(number)
{
    // write code here
    if(number == 1) return 1;
    return 2 * jumpFloorII(number - 1);
}
```
分析：

```javascript
1: 1
2: 2
3: 4
4: 8
5: 16
f(n) = f(n-1) + f(n-2) + f(n-3) + ... + f(1) + 1
	 = f(n-1) + f(n-1)
	 = 2f(n-1)
```