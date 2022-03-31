# forFudan' RIME
RIME schema's, lua, and themes created by Yuhao Zhu. 朱宇浩所定义的 RIME 方案、lua脚本和主题。


## 目录
方案列表
- [🍀️四叶草小鹤双拼14键 for iOS clover_flypy_14](https://github.com/forFudan/rime/tree/main/clover_flypy_14)，基于[🍀️四叶草拼音](https://github.com/fkxxyz/rime-cloverpinyin)设计。
- [🍀️四叶草小鹤双拼14键 for iOS clover_zrm_14](https://github.com/forFudan/rime/tree/main/clover_zrm_14)，基于 [🍀️四叶草拼音](https://github.com/fkxxyz/rime-cloverpinyin)设计。

lua 脚本列表
- [中文字符过滤](https://github.com/forFudan/rime/tree/main/lua/character_filter)（GB2312或GBK）。可以自定义字符集。可以用于不支持字符集过滤的鼠须毫。
  - [filter_forfudan_freq.lua](https://github.com/forFudan/rime/blob/main/lua/character_filter/filter_forfudan_freq.lua) （推荐！GB2312+台湾国字常用字+其他常用字+标点符号。共8675个字符）
  - [filter_forfudan_gb2312.lua](https://github.com/forFudan/rime/blob/main/lua/character_filter/filter_forfudan_gb2312.lua)
  - [filter_forfudan_gbk.lua](https://github.com/forFudan/rime/blob/main/lua/character_filter/filter_forfudan_gbk.lua)

```
使用方法:
(1) 需要将此 lua 文件放在 lua 文件夹下
(2) 需要在 rime.lua 中添加以下代码激活本脚本:
filter_forfudan_freq = require("filter_forfudan_freq")
(3) 需要在 switches 添加状态:
- options: [filter_forfudan_freq, filter_disabled]
  states: [常用字, 不筛选]
  reset: 0
(4) 需要在 engine/filters 添加:
- lua_filter@filter_forfudan_freq
(5) 需要添加以下代码防止符号不上屏:
filter_forfudan_freq:
  tags: [abc]
(6) 建议关闭预测以提升性能, CPU 性能强大的朋友可以忽略本条:
translator/enable_completion: false
```

主题列表
- [十四键·宇宙](https://github.com/forFudan/rime/tree/main/theme/cosmic14key) for iOS.