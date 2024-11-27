# 金融科技与AI 课后作业

## 数据集准备
选取了以下5个数据集（任务类型）：
flare-fomc（Sentiment Analysis ）
https://huggingface.co/datasets/TheFinAI/flare-fomc
flare-finqa（Number Understanding）
https://huggingface.co/datasets/TheFinAI/flare-finqa
flare-headlines（Classification）
https://huggingface.co/datasets/TheFinAI/flare-headlines
flare-ner（Knowledge Extraction）
https://huggingface.co/datasets/TheFinAI/flare-ner
flare-sm-bigdata（Forecasting）
https://huggingface.co/datasets/TheFinAI/flare-sm-bigdata

其中，flare-ner数据集的长度为98，其余长度为300

所有随机抽取过的数据集均被格式化为json格式，用以下code可以打开：

```python
import json
with open('flare-sm-bigdata_test_data.json','r') as f:
    data = json.load(f)
print(data)
```

数据元素为字典，以下是一个示例：

```json
{'id': 'fomc144',
 'query': "Review the sentence from a central bank's communiqué. Designate it as HAWKISH if it expresses a tightening of monetary policy, DOVISH if it reveals an easing of monetary policy, or NEUTRAL if the stance is detached. Your response should return only HAWKISH, DOVISH, or NEUTRAL.\nText: Thus, knowing where productivity growth is headed is, in many respects, equivalent to foreseeing our economic destinies.\nAnswer:",
 'answer': 'neutral',
 'text': 'Thus, knowing where productivity growth is headed is, in many respects, equivalent to foreseeing our economic destinies.',
 'choices': ['dovish', 'hawkish', 'neutral'],
 'gold': 2}
```

