---
layout: post
title: Add new post with Jekyll
date:   2021-07-06 13:25:50 +0700
categories: jekyll update
tags: ["Jekyll", "Post"]
---

**วิธีสร้างโพสต์ใหม่ใน Jekyll**

เนื่องจากเว็บบล็อกนี้ สร้างขึ้นภายใต้เครื่องมือ [Jekyll](https://jekyllrb.com/) ดังนั้นจึงจะขอกล่าวถึงวิธีใช้งาน [Jekyll](https://jekyllrb.com/) เอาไว้บ้างสักเล็กน้อย พอเป็นแนวทางสำหรับผู้ที่เพิ่งเริ่มต้นใช้งาน [Jekyll](https://jekyllrb.com/) ใหม่ ๆ (รวมถึงตัวผู้เขียนเอง) ในการสร้างโพสต์หรือคอนเท้นต์ใหม่นั้น เราสามารถสร้างขึ้นมาได้ด้วยขั้นตอนที่ไม่ยากนักมาเริ่มกันเลย

๑ สร้างไฟล์ใหม่ขึ้นมาในโฟลเดอร์ _posts โดยให้มีชื่อไฟลเป็นรูปแบบดังนี้

```
YYYY-MM-DD-content-title.markdown
```

๒ จัดรูปแบบคอนเท้นต์ด้วย Markup Languege แบบเดียวกับที่ใช้เขียน Readme.md ใน [github](https://github.com/) นั่นล่ะ โดยมีโครงสร้างแบบนี้

```
---
layout: post
title: name-of-content
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: categories-title
---

เนื้อหาคอนเท้นต์...
```

๓ เขียนคอนเท้นต์ให้เสร็จ แล้วก็ publish ขึ้น [github pages](https://pages.github.com/) รอสัก 30 วินาที ก็สามารถเรียกดูโพสต์ที่สร้างใหม่ได้แล้ว
