# Troubleshooting Notes

感谢 [Taeyoung96](https://github.com/Taeyoung96/Troubleshooting-Note) 的仓库给我的启发。  
这个项目让我开始系统地记录我在学习、开发、或者使用 AI 过程中遇到的问题和解决方案。

我暂时没有博客，这个仓库就是我的问题记录中心。  

我希望帮助那些和我相似的**笨蛋**更容易的从网上/AI学习知识

这里将会逐步记录我**蒸馏**出的知识。

如果题目很大的话我会单独开一个`.md`

**不定期更新**

---

## 记录格式

🔑 **关键词**:  
⚠️ **问题出现**:  
✅ **解决方案**:  
📚 **出处**:  

---

🔑 **关键词**: `.md` 怎么换行  
⚠️ **问题出现**: 我在 `README` 使用 “段落之间空一行” 换行的时候，段落之间总是空一行。  
✅ **解决方案**: 在句末使用 `<br>` 或在行尾加两个空格。  
📚 **出处**: [GitHub Flavored Markdown Spec](https://github.github.com/gfm/#paragraphs)

---

🔑 **关键词**: `.md` 怎么将文字标黑只有鼠标放上去才显示  
⚠️ **问题出现**: 想在 `README` 里写一点 `████████`。  
✅ **解决方案**: Markdown 本身不支持这种交互效果。我找到两种别的办法：  

<details>
  <summary>1. 鼠标悬停提示: <span title="我其实在吐槽">这句话表面很冷静</span></summary>

  ```html
  <span title="我其实在吐槽">这句话表面很冷静</span>。
  ```
</details>

<details>
  <summary>2. 用&lt;details&gt;标签</summary>
  
  ```html
  <details>
    <summary>标题</summary>
    被遮住的内容在这里。
  </details>
  ```
</details>

📚 **出处**: [GPT]

---

🔑 **关键词**: `.md` 怎么将 ``` 显示出来  
⚠️ **问题出现**: Markdown 内嵌代码块时想显示反引号。  
✅ **解决方案**:  
* 直接使用更多数量的反引号，例如外层 `~~~~` 包裹内层 ```。
* 或者使用 HTML 实体：`&#96;&#96;&#96;`

📚 **出处**: [GitHub Docs – Writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

🔑 **关键词**: `.md` 怎么正常显示 `<`、`>`、`特殊符号`  
⚠️ **问题出现**: 在 README 里直接写 `<details>`、`<div>` 时会被当作 HTML 解析。  
✅ **解决方案**: 使用 HTML 实体转义：  `<` → `&lt;` 、 `>` → `&gt;`  
📚 **出处**: [GitHub Flavored Markdown Spec – HTML blocks](https://github.github.com/gfm/#html-blocks)

---

🔑 **关键词**: `.md` 在 `<details>` 里显示代码块  
⚠️ **问题出现**: 在 `<details>` 标签里写 ``` 的代码块时，渲染失败或代码不显示。  
✅ **解决方案**: 最简单的做法是在 `last line` 标签和代码块之间**空一行**。  
📚 **出处**: [GitHub Flavored Markdown Spec – HTML blocks](https://github.github.com/gfm/#html-blocks)

---
