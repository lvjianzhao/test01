        x = int(input('请输入一个数字：'))
        # break
    except (ValueError,NameError,Exception):
        print("您输入的不是数字！")
    else:
        print('用户输入完毕！')
```


使用else子句比把所有的语句都放在try子句里要好，这样可以避免一些意想不到，而except又无法捕获的异常。

异常处理并不仅仅处理那些直接发生在try子句中的异常，而且还能处理子句中调用的函数（甚至间接调用的函数）里抛出异常，栗子如下：

```
try:
    this_fails()
except ZeroDivisionError as err:
    print('Handling run-time error:', err)
```

在上面的栗子中，如果函数中报错类型为：ZeroDivisionError，那么
