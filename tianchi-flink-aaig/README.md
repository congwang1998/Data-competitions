# 第三届 Apache Flink 极客挑战赛暨AAIG CUP—电商推荐抱大腿攻击识别


## How to use it
1. Download the data from [Tianchi](https://tianchi.aliyun.com/competition/entrance/531925/information), put it in tcdata folder
2. Train and inference

```
# In container terminal, train and online predict
export SGX_MODE=SIM
sh run.sh
```
3. The strong pipeline is provided by the host, which is really helpful. The model training part I optimized is [here](https://github.com/LongxingTan/Data-competitions/tree/master/tianchi-flink-aaig/root/tianchi_aiflow/workflows/tianchi_main/tf_main.py). To avoid unpredictable bugs, I still use Tensorflow 1.15 same as original baseline.


## Roadmap
- I want to learn some big data, and have already heard Flink for a long time. so I joined this competition.
- I use a simple [model](https://github.com/LongxingTan/Data-competitions/tree/master/tianchi-flink-aaig/root/tianchi_aiflow/workflows/tianchi_main/tf_main.py) to get the 2nd place, one branch MLP for user feature, and the other MLP for item feature.
- The general training trick works for this, like label smoothing, warm-up learning rate.
- How to choose the pos and neg sample is the key to get my score

## Brainstorming
- Describe the item clicked count distribution for each user may be helpful, because the black user will click many hot items and limited but frequency cold item. So how to transfer this into feature?
- The diff between ctr prediction and real click. Because the attack click shouldn't be predicted by CTR, while it happens, CTR is not wrong, some clicks are wrong.
- The graph anomaly detection
- Online learning, because the distribution is changing fast with time.

## Learn from other teams
- What I want to learn is how to build the real time feature and model warmup in Flink, I didn't complete it due to limited knowledge.
