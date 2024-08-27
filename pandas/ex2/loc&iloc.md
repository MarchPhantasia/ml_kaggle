# Question

@FCPS loc和iloc函数是什么

# Answer

`loc`和`iloc`是Pandas库中用于数据选择的两个重要函数。它们的主要区别在于如何引用数据的位置和标签。

### `loc`函数
`loc`函数是基于标签（label）的选择方法。它允许用户通过行和列的标签来选择数据。
reviews.loc[:, ['taster_name', 'taster_twitter_handle', 'points']]
#### 主要特点：
1. **基于标签**：使用行和列的标签进行选择。
2. **闭区间**：在切片时，包含起始和结束标签。

#### 示例：
```python
import pandas as pd

data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data, index=['row1', 'row2', 'row3'])

# 选择标签为'row1'的行
print(df.loc['row1'])

# 选择标签为'row1'到'row2'的行
print(df.loc['row1':'row2'])

# 选择标签为'row1'的行和标签为'A'的列
print(df.loc['row1', 'A'])
```

### `iloc`函数
`iloc`函数是基于位置（integer location）的选择方法。它允许用户通过行和列的整数位置来选择数据。
reviews.iloc[[0, 1, 2], 0]
#### 主要特点：
1. **基于位置**：使用行和列的整数位置进行选择。
2. **左闭右开**：在切片时，包含起始位置，但不包含结束位置。

#### 示例：
```python
import pandas as pd

data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data, index=['row1', 'row2', 'row3'])

# 选择位置为0的行
print(df.iloc[0])

# 选择位置为0到1的行
print(df.iloc[0:2])

# 选择位置为0的行和位置为0的列
print(df.iloc[0, 0])
```

### 总结
- **`loc`**：基于标签的选择，闭区间。
- **`iloc`**：基于位置的选择，左闭右开区间。

这两个函数在数据分析中非常有用，可以根据具体需求选择合适的方法来提取数据。

**Reference**   
[1][【python数据分析基础】—pandas中loc()与iloc()的介绍与区别_iloc函数-CSDN博客](https://blog.csdn.net/sodaloveer/article/details/133032337)  
[2][python - How are iloc and loc different? | Stack Overflow](https://stackoverflow.com/questions/31593201/how-are-iloc-and-loc-different)  
[3][Pandas loc 与 iloc：有什么区别？ | Statorials](https://statorials.org/cn/pandas-loc-%E4%B8%8E-iloc/)  
[4][【python数据分析基础】—pandas中loc()与iloc()的介绍与区别 - 菜鸡一枚 | 博客园](https://www.cnblogs.com/yymn/p/18138573)  
[5][【pandas】loc与iloc函数区别及用法详解_iloc函数和loc函数的区别-CSDN博客](https://blog.csdn.net/weixin_43298886/article/details/112632237)