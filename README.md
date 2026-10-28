# datagov_jd356

**给数据治理与血缘专家·查询改写的语义漂移打分并按阈值给出通过与否。**

`datagov_jd356` —— 为每一项打分并与阈值比较，明确标出通过、边界与不通过三档

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`datagov_jd356.py` 拷走就能用
- 不联网、不写文件

## 对应的岗位

- 目标岗位：**美团 · 负责人数据治理与血缘专家**
- 技能主线：SQL、Spark、数据标注
- 领域标签：数据平台
- 研究方向：数据治理与血缘专家·查询改写的语义漂移

工具里的规则表就是照着上面这条岗位要求建的——每条规则都挂在技能线或领域标签上，命中时能指回具体要求。

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install loaf4gniec-datagov_jd356
```

装完直接用命令名调用：

```bash
datagov_jd356 --help
```

也可以不用安装，直接把 `datagov_jd356.py` 拷走用——它只依赖标准库。

## 为什么需要它

阈值边界单独成档，不把「刚好压在阈值上」混进通过里

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到岗位要求的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python datagov_jd356.py --file input.txt
python datagov_jd356.py --text "示例内容"
python datagov_jd356.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 阈值是固定值，不随数据自适应。
- 只判定达标与否，不解释分数来源。

## 跑测试

```bash
python test_datagov_jd356.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/loaf4gniec/datagov_jd356>

---

## 关于作者

loaf4gniec 做数据治理与血缘专家·查询改写的语义漂移相关的问题，方向对标美团的负责人数据治理与血缘专家岗位。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://loaf4gniec.github.io>
- 仓库：<https://github.com/loaf4gniec/datagov_jd356>

## 许可

MIT，见 [LICENSE](LICENSE)。
