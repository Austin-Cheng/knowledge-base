
什么是智能？真正的智能，应该是具备推理能力，能验证假设，且能为未来做准备的。合适的测评帮助我们理解智能的水平，就像人类的IQ测试。评测LLM帮助我们更好的理解LLM的优势和劣势，用于指导我们应该如何与LLM交互，以获得一个好的结果。

# 一、LLM

## GPT系列

1. GPT-4
2. GPT-3.5-turbo

## Llama系列

Meta公司，原名Facebook，发布的。2023-07-19，发布免费可商用的Llama2。

1. Llama2-70B
2. Llama2-13B
3. Llama2-7B
4. Llama 1

## Claude系列

Anthropic公司研制的

1. Claude-v1
2. Claude-instant-v1

## Vicuna系列

由多家研究机构合作推出的一个开源大语言模型，其研究团队来自于UC Berkeley、CMU、斯坦福、US San Dego和MBZUAI。该系列的模型是基于Meta LLaMA在SharedGPT开放数据集上微调得到。因此，模型本身受限于LLaMA的非商用限制以及OpenAI对ChatGPT共享数据集的限制。官方宣称该模型水平接近ChatGPT，并且超过其它开源的模型。

Vicuna官网：https://lmsys.org/blog/2023-03-30-vicuna/
Vicuna在线使用：https://chat.lmsys.org/?arena

1. Vicuna-33B，模型卡：https://www.datalearner.com/ai-models/pretrained-models/Vicuna-33B
2. Vicuna-13B，模型卡：https://www.datalearner.com/ai-models/pretrained-models/Vicuna-13B
3. Vicuna-13B，模型卡：https://www.datalearner.com/ai-models/pretrained-models/Vicuna-7B


# 二、LLM评测数据集和基准

LLM模型被设计来解决各种任务。LLM评测数据集，用于测试和对比不同的LLM模型在各种任务上的效果。比如，GLUE和SuperGLUE，旨在模拟真实世界的场景，覆盖各种任务，比如文本分类、机器翻译、阅读理解、对话生成。

评测基准：
1. chatbot arena，大模型竞技平台，伯克利大学，评测平台：https://lmsys.org/
评测榜单：https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard
2. MT-Bench，主要评估多轮问答的能力。
3. HELM
4. Big-Bench
5. MME
6. KoLA
7. DynaBench
8. MMLU
9. GLUE-X，旨在评估NLP模型在OOD场景下的robustness。
10. PromptBench，用于增强LLM微调的方法。显示LLM对adversial prompt很敏感，从而需要careful prompt以达到一个好的效果。
11. PandaLM

## 针对特定的下游任务的

1. MultiMedQA
2. C-Eval
3. M3Exam
4. GAOKAO_Bench
5. SOCKET
6. MATH
7. APPS
8. CUAD
9. CVALUES

# 三、LLM评估

在不同类型的任务上进行评测，包括Natural Language Processing Tasks、Robustness、Ethic、Bias、Trustworthiness、Social Science、Natural Science and Engineering、Medical Applications、Agent Applications和Other Applications。

GLUE: https://gluebenchmark.com/leaderboard
SuperGLUE: https://super.gluebenchmark.com/tasks


## 3.1 Natural Language Processing Tasks

一开始LLM的目标就是去提升各种NLP任务的表现，包括理解式的和生成式的。因此，就有很多关于这些任务的评测研究。

### 3.1.1 Nutural language understanding

自然语言理解，也包含很多不同的任务，皆旨在对输入的文本能有一个更好的理解。

Sentiment analysis

情感分析可以看作分类任务，是一个很流行的评测方向。模型在这个任务上的表现通常都很好，ChatGPT的表现比传统的模型效果更好，趋近于GPT-3.5的结果。对于细粒度的情感和情绪的原因分析，ChatGPT也表现超凡。
对于low-resource的情况，LLM也明显由于小型LM，但相对不是那么好，这应该是未来的一个研究方向。

Text classification

GPT-4有明显的提升，但和人的判断还是有距离。总之，LLM在语义理解的任务上表现是糟糕的。

Social knowledge understanding

对于社交知识理解，有人发现一个经有监督的精调的小模型，比如BERT，效果会明显好于zero-shot的LLM，比如GPT、GPT-J-6B。

### 3.1.2 Reasoning

推理任务，是AI的一个大的挑战，模型不仅要理解输入的文本，还要去推导最终的答案，因为答案没法一下子给出来。

mathematical reasoning

ChatGPT在数学推理上有不错的表现，在很多任务上都超过了GPT-3.5。但是要做到精通，仍需要继续优化。

symbolic reasoning

在符号推理任务上，ChatGPT的表现比GPT-3.5要差，因为ChatGPT倾向于不确定的回答，导致效果较差。

commonsense reasoning

ChatGPT不太擅长常识推理，但比non-text情感推理要好。

logical reasoning

在逻辑推理上，ChatGPT和GPT-3.5都优于传统的模型。然而，两者都面临OOD问题，ChatGPT表现的比GPT-3.5、BARD等要差。因为ChatGPT是设计用来精确、理性聊天的。

spatial reasoning

ChatGPT不擅长空间推理。

temporal reasoning

ChatGPT擅长时间推理。Llama-65B，在date推理上是开源LLM中robust最好的，逼近code-davinci-002。

multi-hop reasoning

与其他LLM一样，ChatGPT不擅长多跳推理。

domain-specific reasoning

zero-shot的InstructGPT和Codex可以处理复杂的医学推理任务，但仍然有很大的提升空间。

### 3.1.3 Natural language generation

summarization

question answering

### 3.1.4 Multilingual tasks
### 3.1.5 Factuality


## 3.2 Robustness, Ethic, Bias, and Trustworthiness



## 3.3 Social Science



## 3.4 Natural Science and Engineering



## 3.5 Medical Applications



## 3.6 Agent Applications



## 3.7 Other Applications



# 四、比赛

# 五、行业

# 六、资料

1. 如何评测大模型：https://github.com/MLGroupJLU/LLM-eval-survey
