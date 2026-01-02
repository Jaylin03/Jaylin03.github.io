---
title: 留言板
date: 2026-01-03 12:00:00  # 这个字段保留（主题可能需要），不影响前端显示
type: "guestbook"
comments: true
---

<!-- 动态显示当前时间的代码 -->
<p id="guestbook-date"></p>
<script>
// 获取当前时间并格式化为「年-月-日」
const now = new Date();
const year = now.getFullYear();
const month = String(now.getMonth() + 1).padStart(2, '0'); // 月份从0开始，补0成两位数
const day = String(now.getDate()).padStart(2, '0');
const currentDate = `${year}年${month}月${day}日`;

// 渲染到页面，替换原有欢迎语
document.getElementById('guestbook-date').innerText = `欢迎来到我的博客（${currentDate}），有什么想说的可以在这里留言哦！`;
</script>