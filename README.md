使用到的原数据是“《百年孤独》 范晔译本1，来源于 Z-Library， txt 格式下载； 一份根据
维基百科整理的主要人物名单分词表格，主要由人名、词频和词性三列数据组成， 按照阅读
经验和维基百科共同编制而成。
我的数据收集几乎毫不费力， Z-library 这个游离于三界之外、 不在六道轮回之中的慈善
机构为我们打开了通往广袤的知识海洋的大门。 绘制主要人物的自定义字典主要结合了我自
己的阅读经验和维基百科的帮助。
我在数据清洗方面用到了 re 包的 sub 函数、 pd 包的 dropna 函数和 for 循环嵌套 if 循环
条件判断和列表表达式等。
数据处理如不同文件类型之间读取或者转化主要用到了 pandas 包中的 read_和
DataFrame 函数、 with……open as 上下文管理器， 用 set、 list、 dict 不同数据类型的 add 函数
和嵌套 if 表达式来生成更适配目的的数据类型。
核心的可视化部分：
1. 词云图：主要运用了 jieba 包的 lcut 函数和自定义词典、 停用词； collections 包中的
counter 函数、 most_common 函数； wordcloud 包的 generate_from_frequencies 函数
和自定义图表外观设置的参数。
2. 山脊图： 主要运用了 re 包的 finditer 函数， ridgeplot 包的 ridgeplot 函数、 update_layout
函数和 write_image 函数。
**使用这几段代码，你可以得到以下效果**
<img width="1600" height="1000" alt="wordcloud6" src="https://github.com/user-attachments/assets/412a667a-b8b4-4826-a286-99eae046e55e" />
<img width="700" height="500" alt="name_ridgeplot" src="https://github.com/user-attachments/assets/f422c27b-3955-4793-a9a9-b344da0c1a41" />

