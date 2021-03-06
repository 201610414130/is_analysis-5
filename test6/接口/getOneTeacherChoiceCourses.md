﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getOneTeacherChoiceCourses  [返回](../README.md)
[选课](../用例/选课.md)

- 功能：
    用于获取一门已被教师选课但未被学生选课状态的课程的信息以及选课教师的工号和姓名
    
- 权限：
    - 学生：只能返回已被教师选课但未被学生选课状态的课程，即接口参数user_id必须等于登录学生的student_id
    - 教师：返回全部已被教师选课的课程，即接口参数user_id必须等于登录教师的teacher_id
    
- API请求地址： 
    接口基本地址/v1/api/getOneTeacherChoiceCourses/<user_id>

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID，学生学号或教师工号|
    
- 返回实例：

        {         
            "status": true,
            "info": null,    
            "courses_id": "978-7-302-32982-502",
            "name": "IT新技术",
            "desc": "与时俱进，现在人工智能学习非常火，学生应该掌握这方面的知识",
            "eduAdmin_id": "20038888",
            "eduAdmin_name": "陈赫",
            "release_term": "发布课程的学期",
            "release_date": "课程发布的时间",
            "release_term": "2017-2018",
            "release_date": "2018-06-01 18:02:39",
            "teacher_id": "200909090909",
            "teacher_name": "胡德昆",
            "teacherChoice_date": "2018-06-01 22:02:39",
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |courses_id|课程代码|
  |name|课程名称|
  |desc|课程简介|
  |eduAdmin_id|发布课程的教务管理员的工号，如果为空，则表示课程未发布|
  |eduAdmin_name|发布课程的教务管理员的姓名，如果为空，则表示课程未发布|
  |release_term|发布课程的学期|
  |release_date|课程发布的时间|
  |teacher_id|选课教师工号|
  |teacher_name|选课教师姓名|
  |teacherChoice_date|教师选课时间|

