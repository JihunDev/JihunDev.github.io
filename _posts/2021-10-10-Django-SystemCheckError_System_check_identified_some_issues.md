---
title: Django SystemCheckError System check identified some issues
author: Jihun Kim
date: 2021-10-10 00:00:00 +0000
categories: [Django]
tags: [Django]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

```python
SystemCheckError: System check identified some issues:

ERRORS:
timelines.LikeComment.user: (fields.E304) Reverse accessor for 'timelines.LikeComment.user' clashes with reverse accessor for 'timelines.LikePost.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeComment.user' or 'timelines.LikePost.user'.
timelines.LikeComment.user: (fields.E304) Reverse accessor for 'timelines.LikeComment.user' clashes with reverse accessor for 'timelines.LikeReply.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeComment.user' or 'timelines.LikeReply.user'.
timelines.LikeComment.user: (fields.E305) Reverse query name for 'timelines.LikeComment.user' clashes with reverse query name for 'timelines.LikePost.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeComment.user' or 'timelines.LikePost.user'.
timelines.LikeComment.user: (fields.E305) Reverse query name for 'timelines.LikeComment.user' clashes with reverse query name for 'timelines.LikeReply.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeComment.user' or 'timelines.LikeReply.user'.
timelines.LikePost.user: (fields.E304) Reverse accessor for 'timelines.LikePost.user' clashes with reverse accessor for 'timelines.LikeComment.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikePost.user' or 'timelines.LikeComment.user'.
timelines.LikePost.user: (fields.E304) Reverse accessor for 'timelines.LikePost.user' clashes with reverse accessor for 'timelines.LikeReply.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikePost.user' or 'timelines.LikeReply.user'.
timelines.LikePost.user: (fields.E305) Reverse query name for 'timelines.LikePost.user' clashes with reverse query name for 'timelines.LikeComment.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikePost.user' or 'timelines.LikeComment.user'.
timelines.LikePost.user: (fields.E305) Reverse query name for 'timelines.LikePost.user' clashes with reverse query name for 'timelines.LikeReply.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikePost.user' or 'timelines.LikeReply.user'.
timelines.LikeReply.user: (fields.E304) Reverse accessor for 'timelines.LikeReply.user' clashes with reverse accessor for 'timelines.LikeComment.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeReply.user' or 'timelines.LikeComment.user'.
timelines.LikeReply.user: (fields.E304) Reverse accessor for 'timelines.LikeReply.user' clashes with reverse accessor for 'timelines.LikePost.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeReply.user' or 'timelines.LikePost.user'.
timelines.LikeReply.user: (fields.E305) Reverse query name for 'timelines.LikeReply.user' clashes with reverse query name for 'timelines.LikeComment.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeReply.user' or 'timelines.LikeComment.user'.
timelines.LikeReply.user: (fields.E305) Reverse query name for 'timelines.LikeReply.user' clashes with reverse query name for 'timelines.LikePost.user'.
        HINT: Add or change a related_name argument to the definition for 'timelines.LikeReply.user' or 'timelines.LikePost.user'.
SystemCheckError: System check identified some issues:
```

# Solution

- 모델 접근오류로 related_name= 을 변경해주면 됨
    - name설정 시 동일하게 적용하지 말고 다르게 적용해야 됌