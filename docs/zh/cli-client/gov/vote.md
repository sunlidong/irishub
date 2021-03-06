# iriscli gov vote

## 描述

给VotingPeriod状态的提议投票, 可选项包括: Yes/No/NoWithVeto/Abstain

## 使用方式

```
iriscli gov vote <flags>
```

打印帮助信息:

```
iriscli gov vote --help
```

## 特殊标志

| 名称, 速记        | 默认值                      | 描述                                                                                                                                                 | 是否必须 |
| ---------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| --option         |                            | 投票选项 {Yes, No, NoWithVeto, Abstain}                                                                                                  | Yes      |
| --proposal-id    |                            | 投票的提议ID                                                                                                            | Yes      |

## 例子

### 给提议投票

给提议投`yes`票
```shell
iriscli gov vote --chain-id=<chain-id> --proposal-id=<proposal-id> --option=Yes --from=<key_name> --fee=0.3iris
```

注意：只有验证人才能对指定提议投票，并且可投票的提议必须是`VotingPeriod`状态。

```txt
Committed at block 43 (tx hash: 01C4C3B00C6048A12AE2CF2294F63C55A69011381B819C35F11B04C921DB81CC, response:
 {
   "code": 0,
   "data": null,
   "log": "Msg 0: ",
   "info": "",
   "gas_wanted": 200000,
   "gas_used": 2048,
   "codespace": "",
   "tags": {
     "action": "vote",
     "proposal-id": "2",
     "voter": "iaa1x25y3ltr4jvp89upymegvfx7n0uduz5krcj7ul"
   }
 })
```

### 查询投票详情

[query-vote](query-vote.md)

[query-votes](query-votes.md)

[query-tally](query-tally.md)
