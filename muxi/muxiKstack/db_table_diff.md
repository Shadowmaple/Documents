# 物理表差异汇总

评论部分：

1.  表命名：老板（course_evaluation_comments），我（comment）
    +   单复数问题
    +   直接comment，简略问题
2.  我的多了的有，子评论数（subcomment_num）、点赞数（like_num）、时间（time）、评论对象id（comment_target_id），少了评课id（course_comments_id）
    +   评论对象id一方面用于二级评论中的@操作，另一方面代替评课id（course_comments_id）
    +   点赞数目前来说没用，但可能之后也会像评课广场那样显示点赞总数，所以预先加上
    +   子评论数用于一级评论，方便后期可能有的回复数量显示，目前从原型图来看也是用不上

选课课表部分：

1.  表命名：老板（course_table），我（class_table）
    +   用class的原因是我们将course作为课程，class作为课堂，一个课程有多个课堂，而选课课表是以课堂为单位的

另外貌似老板的表命名基本上都是复数形式的，表示不理解，只是表，用复数有什么必要性吗？

