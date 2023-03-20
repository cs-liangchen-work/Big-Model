这个是清华提出的大模型：

### 原始：
https://github.com/THUDM/ChatGLM-6B

### 强烈推荐的一些fine-tune的工作：

https://github.com/thaumstrial/FinetuneGLMWithPeft

https://github.com/mymusise/ChatGLM-Tuning

https://github.com/ssbuild/chatglm_finetuning

https://github.com/lich99/ChatGLM-finetune-LoRA

# 目前自己工作存在的问题：
- 数据示例：
  根据https://github.com/ssbuild/chatglm_finetuning给的数据样例
```
  给出一种qa 数据示例 , 如果想跟母模型保持一致，可以参考https://huggingface.co/THUDM/chatglm-6b 数据组织结构.
单条数据示例1
{
    "id": 0, "paragraph": [
        #一轮会话
        {
            "q": "从南京到上海的路线",
            "a": [
                "你好，南京到上海的路线如下：",
                "1. 南京到上海，可以乘坐南京地铁1号线，在南京站乘坐轨道交通1号线。",
                "2. 南京到浦东机场，可以搭乘上海地铁1号，在陆家嘴站乘坐地铁1线，在浦东国际机场站乘坐机场快线，前往上海浦东国际机场。",
                "3. 上海到南京，可以换乘上海地铁2号线，从南京站换乘地铁2线，再从南京南站换乘地铁1路，然后到达上海站"
            ]
        }
        #二轮....
    ]
}
单条数据示例2
{"id": 0, "paragraph": [

    {
        "q": "写一个诗歌，关于冬天",
        "a": [
            "冬夜寂静冷，",
             "云在天边飘，", "冰封白雪上， ", "寒冷像一场雪。",
             " ",
             "雪花融化成冰，",
             "像那雪花飘洒，",
             "在寒冷的冬天，",
             "感受春天的喜悦。",
             " 冬日里，",
             "风雪渐消，",
             "一片寂静，",
             "把快乐和温暖带回家。"
        ]
    }
    ]
}
```
