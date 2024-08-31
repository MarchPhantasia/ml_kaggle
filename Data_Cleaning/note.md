``` python
# remove all the rows that contain a missing value
nfl_data.dropna() # 删除包含缺失值的行 如果每一行都存在缺失值，那么整个数据集将被删除

所以可以指定按照列进行删除 dropna(axis=1)


# get a small subset of the NFL dataset
# 选择了数据集的前五行和'EPA'到'Season'列之间的所有列
subset_nfl_data = nfl_data.loc[:, 'EPA':'Season'].head()
subset_nfl_data 

# replace all NA's with 0
# 使用0替换所有缺失值
subset_nfl_data.fillna(0)

# replace all NA's the value that comes directly after it in the same column, 
# then replace all the remaining na's with 0
# 缺失的值替换为同一列中紧随其后的任何值
subset_nfl_data.fillna(method='bfill', axis=0).fillna(0)

``` 