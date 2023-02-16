# 阿里云安全恶意程序检测-学习赛

## 1. 数据集
 &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;   https://tianchi.aliyun.com/competition/entrance/231694/information
## 2. 方案及结果
>  1. Baseline: LightGBM + 祖传参数  &nbsp;&nbsp; &nbsp; score： 0.717547
>  2. TF-IDF: 
>>>    (1) LigtGBm + 祖传参数   &nbsp;&nbsp; &nbsp; score: 0.518331<br>
>>>    (2) xgboost + 祖传参数   &nbsp;&nbsp; &nbsp; score: 0.488092<br>
## 3.优化方案
>  1. 参数问题：我们所使用的模型参数全部为祖传参数，并不意味着是最合适的。我们可以通过多种调参方式进行调参，但同时意味时间和算力成本的付出。
>  2. 模型问题：我们只采用的LightGBM和xgboot两个模型，但其他模型也可尝试，如：catboost\神经网络等。（注：若不考虑模型融合的情况下，竞赛中的四大模型中已经自己设计的神经网络模型下，XGBoot效果最佳。）
>  3. 模型融合：有以下的模型融合方式：我们可以采用双模型融合或者三模型以至于四模型的方式，各自分别又可以做软融合和硬融合两种方式。
>  4. 特征工程的处理：我们通常认为特征工程的好坏决定结果的上限，我们这里只针对‘api'做了简单的处理。我们也还可以有其他的方式，如：列间交叉运算、文本数据处理等。。
>
