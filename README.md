# CapAI

一个致力于研发多模态高性能AI的项目。

## 多模型交互

针对GPT等现有AI的缺陷，CapAI项目将考虑采用多模型交互的方式运行，使用不同AI模型处理不同领域的任务，由一个相对强大的语言模型进行统筹调配。

## 现有模型

|名称|发布日期|最大token数|参数集大小|是否开源|硬件要求|备注|
|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|
|[capai-1006](https://huggingface.co/fwerkor/capai-1006)|2024/2/7|8k|6B|是|显存12GB+|可以使用。|
|[capai-1008](https://huggingface.co/fwerkor/capai-1008)|2024/2/18|32k|6B|是|显存12GB+|性能优异。|
|[capai-1011](https://huggingface.co/fwerkor/capai-1011)|2024/2/18|128k|6B|是|显存12GB+|存在严重缺陷，不推荐使用。|
|[capai-1017](https://huggingface.co/fwerkor/capai-1017)|2024/2/18|128k|6B|是|显存12GB+|基于capai-1011稍有优化。|
|[capai-1019](https://huggingface.co/fwerkor/capai-1019)|2024/3/2|8k|6B|是|显存12GB+|基于capai-1006优化。|

开源模型可在[HuggingFace](https://huggingface.co/fwerkor)查看。

## 超参数设置

CapAI共有以下参数可以设置
- max_length: 模型的总token限制，包括输入和输出的tokens
- temperature: 模型的温度。温度只是调整单词的概率分布。其最终的宏观效果是，在较低的温度下，我们的模型更具确定性，而在较高的温度下，则不那么确定。
- top_p: 模型采样策略参数。在每一步只从累积概率超过某个阈值 p 的最小单词集合中进行随机采样，而不考虑其他低概率的词。只关注概率分布的核心部分，忽略了尾部部分。

具体可参见[相关文档](https://blog.fwerkor.com/archives/630)


