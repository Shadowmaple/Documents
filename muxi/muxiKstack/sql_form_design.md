# 数据库物理表设计

## course_comment 评课

| 字段              | 类型         | 备注                 |
| ----------------- | ------------ | -------------------- |
| course_comment_id | varchar(50)  | 评课id               |
| course_id         | varchar(50)  | 课程id               |
| course_name       | varchar(20)  | 课程名               |
| star              | int          | 评价星级             |
| attendance        | varchar(10)  | 考勤方式             |
| exam_way          | varchar(10)  | 考核方式             |
| content           | text         | 评价内容             |
| is_annoymous      | boolean      | 是否匿名             |
| like_num          | int          | 点赞数               |
| comment_num       | int          | 一级评论数           |
| tags              | varchar(255) | 标签id列表，逗号分隔 |
| is_valid          | boolean      | 是否被折叠           |
| time              | varchar(20)  | 评课时间（时间戳）   |



## comment 评论

| 字段              | 类型        | 备注               |
| ----------------- | ----------- | ------------------ |
| comment_id        | varchar(50) | 评论id             |
| content           | text        | 评论内容           |
| like_num          | int         | 点赞数             |
| time              | var(20)     | 评论时间（时间戳） |
| user_id           | varchar(50) | 评论用户id         |
| comment_target_id | varchar(50) | 评论对象id         |
| parent_id         | varchar(50) | 父评论id           |
| is_top            | boolean     | 是否是一级评论     |
| subcomment_num    | int         | 子评论数           |

## course_tag 评课标签

| 字段     | 类型        | 备注   |
| -------- | ----------- | ------ |
| tag_id   | varchar(20) | 标签id |
| tag_name | varchar(20) | 标签名 |

## course_comment_like 评课点赞

| 字段              | 类型        | 备注   |
| ----------------- | ----------- | ------ |
| course_comment_id | varchar(50) | 评课id |
| user_id           | varchar(50) | 用户id |

## comment_like 评论点赞

| 字段       | 类型        | 备注   |
| ---------- | ----------- | ------ |
| comment_id | varchar(50) | 评论id |
| user_id    | varchar(50) | 用户id |

## class_table 排课课表

mongoDB存储

| 字段    | 类型   | 备注         |
| ------- | ------ | ------------ |
| user_id | string | 用户id       |
| classes | object | 课堂hash列表 |

