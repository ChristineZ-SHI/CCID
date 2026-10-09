# CCID · Streamlit

原始 CCID 应用的界面美化版，采用黑、白、绿色配色。
保留全部原始分析函数、YouTube 采集、三类文件上传、八个页签、OpenAI 总结和 scikit-learn 随机森林模型。

## 本地运行

```bash
pip install -r requirements.txt
streamlit run CCID.py
```

## Streamlit Community Cloud

将本文件夹的内容上传至 GitHub 仓库，在 Streamlit Community Cloud 创建应用，入口文件选 `CCID.py`。
必须保留 `.streamlit/config.toml` 以应用主题。Python 建议选择 3.11 或 3.12。

可在应用 Settings → Secrets 中配置：

```toml
YOUTUBE_API_KEY = "your-youtube-api-key"
OPENAI_API_KEY = "your-openai-api-key"
```

也可直接使用原版侧栏的手动输入框。不要将真实 API Key 提交至 GitHub。
界面主题是独立项目的视觉设计，未使用德勤的标志。

## 演示模式

首次打开自动加载 96 条模拟内容及 48 条模拟评论，均为程序生成的虚构记录，不含项目原始数据。
侧栏的“加载演示数据 / Load demo data”按钮可以重新载入。
规则报告自动生成，无需 API Key；预测页直接使用模拟数据训练原来的随机森林。
所有演示结果仅用于展示功能，不代表真实公司表现或经验证的商业预测。
上传文件并点击 Run Analysis 后切换到用户数据；演示数据不会混入该轮分析。
