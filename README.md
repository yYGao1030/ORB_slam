零、
相应的错误已更改这里强调几个问题
对于自身的版本的问题不适合的直接去github寻找源码
地址https://github.com/raulmur/ORB_SLAM2.git
一、对于几个问题强调
1、 变异的cmake是基于14的这里有两种改法
1.就是直接将c++11改为出++14
2.在cmake中添加这个语句
set(CMAKE_CXX_STANDARD 14)
二、如果编译出了问题就去寻找源码git出来推荐一个链接可以照着修改
https://cxyzjd.com/article/meng_152634/127570220
博客https://blog.csdn.net/meng_152634/article/details/127570220?ops_request_misc=&request_id=&biz_id=102&utm_term=orb_slam2&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-7-127570220.142^v96^pc_search_result_base9&spm=1018.2226.3001.4187
内容是一致的
三、对于eigen的处理可能会报错eigen对于pangolin的版本不匹配这里不用寻找对应的版本让他去自适应
find_package(Eigen3  REQUIRED NO_MODULE)
四、！！！（最最最重要的一点不改不会报错但是不能运行）
 删掉ORB_SLAM2主目录及DBoW2和g2o目录中CMakeLists.txt文件中的 -march=native
 (core dumped)
 
