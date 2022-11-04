# Pandas 库

- Pandas 是基于 NumPy 的一个开源 Python 库
- 广泛用于快速分析数据、数据清洗和准备
- 简单地说，你可以把 Pandas 看作是 Python 版的 Excel

###   Pandas 两个数据结构

- series（1D）
  - 一维、带索引的数据结构
  - 可以存储任意类型的数据：int、float、字符串、python对象等
  - 它的索引叫做 index
  - 基本调用方法为s = pd.Series(data, index=index)
- dataframe（2D）
- panel（3D）


### series 

- 由索引和数据组成，索引在左，数据在右
- 一个series总是包含相同类型的数据
- 获取索引：s.index，s.columns
- 获取数据：s.values
- 查看数据：
  - s.head()
  - s.tail()
  - s. describe()  # 数据的统计摘要

- 重新定义新的索引
  - df.reindex(index=[0, 2, 5], columns=['A', 'C', 'B'])
- 设置索引：将列表、序列或dataframe设置为dataframe索引的方法


### dataframe

- 获取列数据：


### 索引

在pandas中建立索引意味着简单地从DataFrame中选择特定地数据行和列


- DataFrame.loc[ ]：基于标签
- DataFrame.iloc[ ]：基于位置或整数的
- DataFrame.ix[ ]：此函数用于基于标签和整数的（上面两种它都可以）

### 时间的创建与查看


- dates = pd.date_range('20130101', periods=6)  表示创建一个时间序列
- df = pd.DataFrame(np.random.randn(6, 4), index = dates, columns = list('ABCD'))
- ↑ 表示数据为随机的 6×4 数据，行索引是时间序列，列名是ABCD


### 合并数据的5个函数，分别的优势

- 1、join：用于基于索引的横向合并拼接
    - 如果索引不一致，会显示NAN
- 2、merge：用于基于指定列的横向合并拼接
    - pd.merge(x,y,how="left")
    - 可以指定不同的how参数表示连接方式，有inner内连、left左连、right右连、outer全连，默认为inner
- 3、concat：用于横向和纵向合并拼接
    - 横向拼接：pd.concat([x,y],axis=1)
    - 纵向拼接：pd.concat([x,y],axis=0)
- 4、append：用于纵向追加
  - x.append(y)
- 5、combine：通过使用函数，把两个DataFrame按列进行组合
  - x.combine(y,lambda a,b:np.where(a>b,a,b))


