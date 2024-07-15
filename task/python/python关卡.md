# python关卡

##### 任务一：Python实现一个wordcount函数，统计英文字符串中每个单词出现的次数。返回一个字典，key为单词，value为对应单词出现的次数。

```python
import re

texts = """
Got this panda plush toy for my daughter's birthday,
who loves it and takes it everywhere. It's soft and
super cute, and its face has a friendly look. It's
a bit small for what I paid though. I think there
might be other options that are bigger for the
same price. It arrived a day earlier than expected,
so I got to play with it myself before I gave it
to her.
"""


def wordcount(text):
    words = re.findall(r"\b[\w']+\b", text.lower())
    word_count = {}
    for word in words:
        if word in word_count:
            word_count[word] += 1
        else:
            word_count[word] = 1
    return word_count

print(wordcount(texts))
```
返回结果：
```python
{'got': 2, 'this': 1, 'panda': 1, 'plush': 1, 'toy': 1, 'for': 3, 'my': 1, "daughter's": 1, 'birthday': 1, 'who': 1, 'loves': 1, 'it': 5, 'and': 3, 'takes
': 1, 'everywhere': 1, "it's": 2, 'soft': 1, 'super': 1, 'cute': 1, 'its': 1, 'face': 1, 'has': 1, 'a': 3, 'friendly': 1, 'look': 1, 'bit': 1, 'small': 1,
 'what': 1, 'i': 4, 'paid': 1, 'though': 1, 'think': 1, 'there': 1, 'might': 1, 'be': 1, 'other': 1, 'options': 1, 'that': 1, 'are': 1, 'bigger': 1, 'the'
: 1, 'same': 1, 'price': 1, 'arrived': 1, 'day': 1, 'earlier': 1, 'than': 1, 'expected': 1, 'so': 1, 'to': 2, 'play': 1, 'with': 1, 'myself': 1, 'before':
 1, 'gave': 1, 'her': 1}
```

![运行结果](https://github.com/JMMonkey/discharge_LLM/blob/56833ea95b9204fc1fbe0b80d96ebf16e1049099/task/python/%E8%BF%90%E8%A1%8C%E7%BB%93%E6%9E%9C.png)

##### 任务二：使用本地vscode连接远程开发机，在开发机进行debug。
使用正则表达式\[\w'\] 将it's也定为一个单词进行计数。
![debug](https://github.com/JMMonkey/discharge_LLM/blob/806f0fe06eb872e8a71dcef3bdc4a241196bff8a/task/python/debug.png)

