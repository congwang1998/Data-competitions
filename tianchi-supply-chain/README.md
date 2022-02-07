# 2021阿里云供应链大赛—需求预测及单级库存优化

## How to use it
1. Download the data from [Tianchi](https://tianchi.aliyun.com/competition/entrance/531934/information), put it in tcdata folder
2. Train and inference

```
sh run.sh
```

## Roadmap
1. This is a complex but also simple competition. The task is complex, but my solution to get the 2nd place is simple
2. The key is that I use a faultless ensemble method to set the safety stock, which considered weekly and daily fluctuation, you can see the details [here](https://github.com/LongxingTan/Data-competitions/tree/master/tianchi-supply-chain/code/predict.py)
3. The demand prediction is a simple GBDT method, which shows obvious progress than my rule method

## Brainstorming
- An end to end NN solution is always attractive for this task


## Learn from other teams
- 我最后一场天池比赛了，事不过三。第一场的AI earth前一位季军是刷小号上去的；第二场的Flink第4是初赛刷小号的；这一场我遥遥领先，答辩把我从第2降到第5。
