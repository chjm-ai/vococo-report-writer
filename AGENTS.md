# AGENTS.md

Vococo Report Writer：chjm-ai 独立维护的中文汇报写作 Skill。

## 入口

- `SKILL.md`：模型读取的规则，技能标识为 `vococo-report-writer`。
- `README.md`：定位、使用与测试边界。
- `tests/`：编辑边界样例、人工回归清单及结构检查脚本。

## 检查

无需安装依赖。结构脚本使用 Python 3 标准库：

```bash
python3 tests/check_structure.py tests/fixtures/structure.md /path/to/edited-copy.md
```

同一 fixture 自比可作脚本烟测，不能证明模型改写质量。

## 维护边界

- 汇报规则变更要同步人工核对清单，并记录 CHANGELOG。
- round8 是人工构造的测试输入，不作为真实产品事实发布。
- 未随仓库公开的实验记录，不用作可复现的效果宣传。
- 通用编辑部分保留来源说明和原作者 MIT 版权。
- 发布到本项目独立远端，不向来源仓库直接提交定制规则。
