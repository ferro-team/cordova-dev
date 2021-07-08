---
layout: post
title: แสดงความคิดเห็นในบล็อก Jekyll ด้วย github issue api
# อย่าลืมเปลี่ยนนะ
date:   2021-07-07 11:05:50 +0700
categories: jekyll update
tags: Jekyll Comment github issue api API
---
๑. ใส่ variable ใน public repo ที่ต้องการให้แสดงความคิดเห็น ในไฟล์ <code>../blog-name/_config.yml</code>
```

issues_repo: username/repo_name
```

๒. เปิด issue ใน repo ที่เราตั้งไว้ขึ้นมา จดหมายเลข ID ไว้
```
รอหาภาพประกอบ
```

๓. ระบุคอมเม้นต์ไอดี ที่ส่วน front matter ของโพสต์ <code>../blog-name/_posts/yyyy-mm-dd-post-title.markdown</code> ตามนี้
```
comments_id: 1 #หมายเลขไอดีที่จดมา
```

๔. แก้ไขไฟล์ <code>../blog-name/_layouts/post.html</code> ใส่สคริปต์ลงไปประมาณนี้
{% raw %}
```
{% if page.comments_id %}
  {% include comments.html issue_id=page.comments_id %}
{% endif %}
```
{% endraw %}


๕. แก้ไข <code>../blog-name/_includes/comments.html</code>
{% raw %}
```js
{% assign issues_repo = site.issues_repo %}
{% assign issue_id = include.issue_id %}

<section id="comments">
    <div class="comment-actions">
        <h2>Comments <span id="comments-count"></span></h2>
        <a class="button" href="https://github.com/{{ issues_repo }}/issues/{{ issue_id }}">Post comment</a>
    </div>
    <div id="comments-wrapper">
      Loading...
    </div>
</section>

<!-- Comments script -->
<script></script>
```
{% endraw %}
