# WorkManageSystem
WorkManageSystem   （作业管理系统）

基于Spring+SpringMVC+Hibernate框架的项目

一、系统功能说明

    1.1 系统简介
        该系统是在学习了spring的基础上进行开发的，在需求上，充分考虑了具体用户的实际情况。
        本产品将主要适用于学校教师对班级作业的管理，方便教师在线批改作业、查看学生完成作业
        情况，方便学生向老师提交作业、以及查看老师批改情况。本系统为人们提供了一个方便学校
        中老师对学生日常作业的管理的系统，方便了老师和学生之间的互动，相对传统的学生代表收
        发作业、再提交给老师这种浪费人力物力的不便捷来说，该系统大大提高了老师对学生作业管
        理的效率，在学校中，该平台对老师和学生很实用。

    1.2 系统主要功能
      （1）管理员可添加、删除、修改、查询——学生和教师；
      （2）教师可布置多次作业，设置作业的提交时间；（还可以修改作业）
      （3）学生完成作业后，将作业文件打包上传，可重新提交；
      （4）教师可批改学生提交的作业，进行打分，并设置批阅意见。
      （5）学生可查看作业的批阅情况；
      （6）教师可统计学生作业的提交情况，班级作业的提交情况等；
      （7）教师、学生可以修改密码，重置密码；
      （8）系统有三种角色登录：管理员、教师、学生。

    1.3 系统开发环境
        Windows 8操作系统 
        eclipse for J2EE ( IDE ) 
        JDK 7 
        MySQL数据库  
        Tomcat 8.0 
        Chrome浏览器。
      
二、系统设计

    2.1 系统总体设计
    
      2.1.1 系统总体功能需求
        该系统主要适用于学校教师对班级作业的管理，其中主要包括教师在线批改作业、查看学生完成作业情况，
        方便学生向老师提交作业、下载作业以及查看老师批改情况等功能。
        
      2.1.2 功能模块的具体内容和需求明细
        根据系统要求可以将作业管理系统分为管理员模块、教师模块、学生模块三大模块。如下结构图:
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/FunctionalStructure.png)

        管理员：
        1.	添加、删除、查看、修改——学生、教师、课程的基本信息；
        2.	管理平台的管理；
        3.	修改个人信息；
        教  师：
        1.	布置作业并设置提交时间；
        2.	批改学生提交的作业，进行打分和设置批阅意见；
        3.	统计学生作业的提交情况；
        4.	统计班级作业的提交情况；
        5.	查看班级作业的批阅情况和提交情况；
        6.	修改个人信息（修改或重置密码）；
        学  生：
        1. 上传作业，可以重新提交；
        2. 查看自己作业的批阅情况；
        3. 查看老师发布的作业；
        4. 修改个人信息（修改或重置密码）；
        
    2.2 界面设计（部分展示）
    
      2.2.1 主页界面
      
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/LoginPage.png)

      2.2.2 管理员界面
        管理员——教师总览页面
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/TeacherOverviewPage.png)

      2.2.3 教师界面
        教师——统计提交作业页面
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/StatisticalSubmissionPage.png)
        
      2.2.4 学生界面
        学生——主页面
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/StudentPage.png)
        
    2.4 主要功能模块
      2.4.1 管理员模块
        管理员模块：包括登录、修改教师信息、添加教师信息、删除教师信息、修改学生信息、
                   添加学生信息、删除学生信息、修改个人信息、退出等功能。如下图所示：
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/ManagerModule.png)
        
        登录：管理员通过输入用户名密码登录系统。
        修改教师信息：管理员可修改教师的信息，可以修改姓名、性别、密码和所在学院，
                     由于账号是用来标注用户唯一性信息，所以不可以修改。
        添加教师信息：管理员可以添加教师信息，通过输入账号、姓名、性别、密码和所在学院，
                     点击添加按钮即可成功添加一条教师信息。
        删除教师信息：管理员可以删除教师信息，直接在教师信息表中选取要删除的一条教师记录
                     最后，点击删除按钮即可。
        修改学生信息：管理员可修改学生的信息，可以修改姓名、性别、密码和所在学院，由于
                     学号是用来标注学生唯一性信息，所以不可以修改。
        添加学生信息：管理员可以添加学生信息，通过输入学号、姓名、性别、密码和所在学院，
                     点击添加按钮即可成功添加一条学生信息。
        删除学生信息：管理员可以删除学生信息，直接在学生信息表中选取要删除的一条学生记录，
                     然后，点击删除按钮即可。
        修改个人信息：管理员同时可以修改个人信息，包括姓名、密码等。
        退出：即管理员退出作业管理系统。

      2.4.2 教师模块
        教师模块：学生模块包括发布公告、发布作业、批改作业、统计提交情况等。
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/TeacherModule.png)
        
        发布公告：通过该功能，教师可以对某个班课程或作业变更的情况进行公告说明，学生在自己的系统中
                 会看到针对自己班的公告内容，发布教师与学生之间进行信息交流。
        发布作业：教师可以通过该功能进行作业的发布,发布作业时需要输入作业的主题、截止时间、课程、班级以及作业的内容。
        批改作业：批改作业是教师的主要功能，教师通过该功能给学生的作业进行打分和写评语，并将结果存
                 入数据库中以便学生通过查看批阅功能查看自己作业的批改情况。
        统计提交情况：教师通过该功能总览各班的各个作业的提交情况，也可以通过点击批阅链接对已提交的作业进行批阅。

      2.4.3 学生模块
        学生模块：学生模块包括查看发布作业、上传下载作业、查看批阅情况等。
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/StudentModule.png)
        
        查看发布作业：主要是让学生用户查看由教师对该学生发布的所有的作业，
                     学生可以查看作业内容以及要求，还可以查看作业的完成情况。
        上传下载作业：为学生用户提供了上传提交作业和下载作业文件的途径，学生可以根据需求
                     选择下载相应的作业文件，并且在完成作业后可以上传提交作业。
        查看批阅情况：方便学生用户对作业批改结果的查看，学生可查看到教师对学生用户已完成或未完成作业的批改情况。

三、关键技术与应用

    3.1 HTML 5
        整个页面的采用了div+css的布局方式，结构清晰，功能明确，此外整体框架还通过iframe标签进行管理，
        导航栏为一个页面，其他页面均通过iframe标签显示，这样减少了代码的重复量，减轻了开发任务量，提高了效率。

    3.2 Query
        该系统根据jQuery实现了动态的页面效果，包括输入校验、动态显示和页面跳转，具体的实现代码如下：
        a、通过jQuery显示导航栏的页面跳转
        //教师添加
              $("a.addT").click(function(){
                $("iframe").attr("src","/WorkManageSystem/manager/m_addteacher");
              });
              //学生总览，删除，修改
              $("a.allS").click(function(){
                $("iframe").attr("src","/WorkManageSystem/manager/m_studentmanage");
              });

    3.3 Spring DAO
        该系统通过Spring Dao 进行数据库访问，具体的数据库方法都封装在各个实体类对应的Dao中，
        创建Dao时采用了接口编程，提高了系统的可维护性。
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/SpringDao.png)

    3.4 Spring MVC
        该系统的整体框架为Spring MVC+Hibernate，Spring MVC 负责视图层和控制层的逻辑，
        Hibernate负责数据库的数据库关系对象映射，项目的Spring MVC结构如下图所示：
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/SpringMVC.png)
   
        Spring 的各种配置目录如下图所示：
   ![image](https://github.com/TouchDreamRen/WorkManageSystem/raw/master/screenshots/Spring.png)
        
    3.5 Hibernate
        该系统的数据库操作采用了Hibernate+JDBC，Hibernate的使用简化了对数据库的操作。
        Spring中对Hibernate的配置如下:
        <beans>
          <!-- 配置hibernate相关数据库的操作 -->
          <bean id="dataSource"
            class="org.springframework.jdbc.datasource.DriverManagerDataSource">
            <!-- 数据库的驱动 -->
            <property name="driverClassName" value="com.mysql.jdbc.Driver" />
            <!-- 数据库的Id,用户名与密码 -->
            <property name="url" value="jdbc:mysql://localhost:3306/wms" />
            <property name="username" value="root" />
            <property name="password" value="smile" />
          </bean>

          <bean id="sessionFactory"
            class="org.springframework.orm.hibernate4.LocalSessionFactoryBean">
            <property name="dataSource" ref="dataSource" />
            <property name="hibernateProperties">
              <props>
                <!-- 配置不同数据库的方言 -->
                <prop key="hibernate.dialect">org.hibernate.dialect.MySQLDialect</prop>
                <!-- 其实这个参数的作用主要用于：自动创建|更新|验证数据库表结构。 
                如果不是此方面的需求建议set value="none". 其它几个参数的意思，我解释一下： 
                validate 加载hibernate时，验证创建数据库表结构 create 每次加载hibernate，
                重新创建数据库表结构，这就是导致数据库表数据丢失的原因。 
                create-drop 加载hibernate时创建，退出是删除表结构 update 加载hibernate自动更新数据库结构 -->
                <prop key="hibernate.hbm2ddl.auto">update</prop>
                <!-- 是否显示sql语句 -->
                <prop key="hibernate.show_sql">true</prop>
                <prop key="hiberante.format_sql">true</prop>
              </props>
            </property>
            <property name="configLocations">
              <list>
                <value>
                  <!-- 读取和实体相关的xml -->
                  classpath*:wms/hibernate/hibernate.cfg.test.xml
                </value>
              </list>
            </property>
          </bean>

          <!-- 定义事务管理器（声明式的事务） -->
          <bean id="transactionManager"
            class="org.springframework.orm.hibernate4.HibernateTransactionManager">
            <property name="sessionFactory" ref="sessionFactory"></property>
          </bean>

          <bean id="transactionBase"
            class="org.springframework.transaction.interceptor.TransactionProxyFactoryBean"
            lazy-init="true" abstract="true">
            <!-- 配置事务管理器 -->
            <property name="transactionManager" ref="transactionManager"></property>
            <!-- 配置事务管理器 -->
            <property name="transactionAttributes">
              <props>
                <!-- 下面就开始配置各个模块所必须的部分，
                在各自的applicationContext-XXX-beans.xml配置的对于事务管理的详细信息。 
                首先就是配置事务的传播特性，如下： -->
                <!-- 配置事务传播特性 -->
                <prop key="add*">PROPAGATION_REQUIRED,-Exception</prop>
                <prop key="update*">PROPAGATION_REQUIRED,-Exception</prop>
                <prop key="insert*">PROPAGATION_REQUIRED,-Exception</prop>
                <prop key="modify*">PROPAGATION_REQUIRED,-Exception</prop>
                <prop key="delete*">PROPAGATION_REQUIRED,-Exception</prop>
                <prop key="get*">PROPAGATION_NEVER</prop>
              </props>
            </property>
          </bean>
        </beans>

        Hibernate中对事务的配置如下：
        <!DOCTYPE hibernate-configuration PUBLIC
                "-//Hibernate/Hibernate Configuration DTD 3.0//EN"
                "http://www.hibernate.org/dtd/hibernate-configuration-3.0.dtd">
        <!-- （通常是 hibernate.cfg.xml）中声明持久性类： -->
        <hibernate-configuration>
            <session-factory>
              <!-- List of XML mapping files -->
              <mapping resource="wms/entity/Manager.hbm.xml"/>
              <mapping resource="wms/entity/Teacher.hbm.xml"/>
              <mapping resource="wms/entity/Student.hbm.xml"/>
              <mapping resource="wms/entity/Course.hbm.xml"/>
              <mapping resource="wms/entity/Clazz.hbm.xml"/>
              <mapping resource="wms/entity/Work.hbm.xml"/>
              <mapping resource="wms/entity/CheckWork.hbm.xml"/>
              <mapping resource="wms/entity/Notice.hbm.xml"/> 
                <!-- <mapping class="wms.entity.Teacher"/> -->
            </session-factory>
        </hibernate-configuration>
        
    3.6 BootStrap
        该系统页面采用了BootStrap开源框架，使得系统具备了移动设备优先的特性，通过BootStrap框架的使用，
        让页面的布局更加清晰、结构更加合理、效果更加多样。

四、总结与体会

           通过这个项目，学会了用SpringMVC+hibernate+MySql数据库开发web系统的架构，通过Hibernate的文件
       配置，极大地方便了对数据库的操作，自动生成数据库数据，这是非常方便的，使得我们开发人员对数据库操作更加
       容易。把实体类与数据库表进行匹配，简化了读取过程中产生的代码书写，使编程人员从复杂的代码中解放出来。
           SpringMVC的这种架构，层次分明，使得代码清晰，各项模块功能划分简单，更加有利于我们进行开发。在JSP
       页面使用的JSTL语言，也是非常容易的，简化了操作，个人感觉非常的方便。同时做界面时，运用了一些Bootstrap
       的框架效果，如导航栏，面包屑导航等，使得我们的页面更加具体简洁和美观。
       
    


