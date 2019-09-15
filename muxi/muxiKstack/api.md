# api

## 评课评论

/comments/

发布评课

+   token，课程，评价星级，考勤方式，考核方式，课程特点，课程评价，是否匿名，用户id
+   课程id，评课id，token

获取评课详情，包括所有评论

+   课程id，评课id，token，用户id
+   token，评课信息（用户信息，评价星级，课程，课程特点，评价，点赞数，点赞状态，评论数，时间），评论（用户信息，评论，点赞数，点赞状态，时间，评论对象信息）

删除评课

+   课程id，评课id，token，用户id
+   token，message

评课/评论点赞

+   课程id，点赞对象id，token，用户id
+   token，message，点赞状态，点赞数

评论评课/回复评论

+   课程id，评论对象id，token，评论内容，用户id，是否匿名
+   token，用户信息，评论对象，评论内容，点赞状态，点赞数，时间



## 课表排课

/courseTable/

### 课表

获取课表

+   token，用户id
+   课表数量，课表列表（课表id，课表名，课堂列表（课堂id，名称，教师，上课地点，时间）），token

添加新课表、创建副本

+   token，用户id，是否创建副本，副本课表
+   token，课表id，课表名，课堂列表（课堂id，名称，教师，上课地点，时间）

删除课表

+   token，用户id，课表id
+   token，message

课表重命名

+   token，用户id，课表id，课表新名
+   token，课表id，message

### 课堂

收藏的课堂加入课表

+   token，用户id，课堂id，课表id
+   token，课表id，课堂信息（课堂id，名称，教师，上课地点，时间）

删除课堂

+   token，用户id，课堂id，课表id
+   token，课表id，message

