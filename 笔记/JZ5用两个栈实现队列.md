> 时间限制：C/C++ 1秒，其他语言2秒 
> 空间限制：C/C++ 32M，其他语言64M 
> 热度指数：693955
> 本题知识点： 队列 栈
### 题目描述
用两个栈来实现一个队列，完成队列的Push和Pop操作。 队列中的元素为int类型。
### 代码
```javascript
var stack1 = [], stack2 = [];
function push(node)
{
    stack1.push(node);
}
function pop()
{
    if(stack2.length == 0){
        if(stack1.length == 0){
            return null;
        }else{
            while(stack1.length != 0){
                stack2.push(stack1.pop());
            }
        }
        return stack2.pop();
    }else{
        return stack2.pop();
    }
}
```