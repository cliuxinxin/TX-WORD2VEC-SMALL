# TX-WORD2VEC

腾讯开源的word2vec模型。

原版15个G，一般爱好者很难玩出来。

所以做了一些小的。方便大家使用。


5000-small.txt 这个有1w词，可以下下来玩玩

45000-small.txt 这个有4.5w的词，已经能解决很多问题了

再大就没意义了，自己去下载吧，看看readme.txt文件中有说明

## 如何使用

### 读取模型

from gensim.models import KeyedVectors

model = KeyedVectors.load_word2vec_format("50-small.txt")

### 把玩模型

model.most_similar(positive=['女', '国王'], negative=['男'], topn=1)

model.doesnt_match("上海 成都 广州 北京".split(" "))

model.similarity('女人', '男人')



