Kyligence Insight for Superset 使用手册
=======================================

Kyligence Insight for Superset 是 Kyligence工程师深度定制的可视化工具，
与Kyligence/Kylin无缝集成，一键同步cube并自动适配Kyligence/Kylin查询语法，本文将分步介绍
Kyligence Insight for Superset的使用方法。

登录
----

打开sueprset界面，输入默认管理员的用户名和密码 admin/admin 即可登录 |image0|

导入/刷新cube
-------------
首先需要在 **数据源- 数据库** 处增加Kyligence的项目的连接串 |image31|

其中，数据库URL的格式为 **kylin://username:password@host:port/project** ，如果您需要在SQL实验中使用该项目中的表，则需要勾选 在SQL实验室中显示  |image32|

在Superset界面内点击 **数据源- Kylin 数据源刷新**，即可导入/刷新所有已经增加的项目下的cube |image1|

刷新成功后会自动进入 **数据源- Kylin Cubes** 界面，显示全部cube |image2|

查询Cube
--------

在 **数据源-Kylin Cubes** 点击cube名称，即可进入分析界面
在各栏选择相应的值，如时间筛选值，维度和度量值，以及行数限制等，然后点击左上角的
**运行查询** ，即可运行查询，得到结果集图表 |image3|

点击 **图表类型** 可以更改可视化图表类型 |image4|

比如选择饼图 |image5|

导出CSV文件
--------

在数据探索页面点击CSV按钮即可导出CSV  |image29|

在SQL实验室页面点击CSV按钮即可导出CSV  |image30|

注：使用EXCEL打开标准UTF-8编码的CSV文件的方法为：

点击 **数据** - **从文本** |image25|

使用 **分割符号** 的方式导入，选择文件原始格式为 **从UTF-8** |image26|

选择分隔符为 **逗号** |image27|

即可正常显示中文 |image28|

保存与分享
----------

在数据探索界面，点击左上角的保存 填入对应的信息，然后点击保存 |image6|

在仪表版界面，点击 **Edit Dashboard**, 然后点击 **Actions** 中的
**邮件** 即可使用邮件分享仪表板 |image7|

在自动生成的邮件中填入收件人，然后点击发送 |image8|

收件人点击邮件中的链接，即可在浏览器中进入到相应的仪表板页面 |image9|

在SQL 实验室 进行自定义SQL查询
------------------------------

点击 **SQL 实验室- SQL编辑器** 即可进入自定义SQL查询 |image10|

选择对应的数据库和表，输入SQL，点击 **运行查询** 即可得到查询结果
|image11|

在查询结果处选择 **可视化**\ ，可对查询结果集进行可视化 |image12|

自定义维度/度量
---------------

在 **数据源- Kylin Cubes** 界面，点击编辑记录，对某个cube进行编辑
|image13|

在 **列名列表** 处点击加号，增加自定义维度, 编辑相应信息，点击保存
|image14|

然后在列名列表处将新增维度勾选为 **可分组** ，**可筛选** 即可，同理可以增加自定义度量 

修改权限
--------

在 **安全 - 角色列表** 中可以创建/编辑用户角色 |image19|

如复制了Alpha 角色，命名为Alpha\_no\_csv 角色，在Alpha\_no\_csv
角色中删除了 **can download on SliceModelView** 权限（导出CSV权限）
|image20|

在 **安全 - 用户列表** 中赋予ANALYST用户Alpha\_no\_csv 角色 |image21|
|image22|

更改后，ANALYST用户没有下载CSV的权限 |image23|

.. |image0| image:: ../images/user_manual_cn/01.png
.. |image1| image:: ../images/user_manual_cn/02.png
.. |image2| image:: ../images/user_manual_cn/03.png
.. |image3| image:: ../images/user_manual_cn/04.png
.. |image4| image:: ../images/user_manual_cn/05.png
.. |image5| image:: ../images/user_manual_cn/06.png
.. |image6| image:: ../images/user_manual_cn/07.png
.. |image7| image:: ../images/user_manual_cn/08.png
.. |image8| image:: ../images/user_manual_cn/09.png
.. |image9| image:: ../images/user_manual_cn/10.png
.. |image10| image:: ../images/user_manual_cn/11.png
.. |image11| image:: ../images/user_manual_cn/12.png
.. |image12| image:: ../images/user_manual_cn/13.png
.. |image13| image:: ../images/user_manual_cn/14.png
.. |image14| image:: ../images/user_manual_cn/15.png
.. |image17| image:: ../images/user_manual_cn/18.png
.. |image18| image:: ../images/user_manual_cn/19.png
.. |image19| image:: ../images/user_manual_cn/20.png
.. |image20| image:: ../images/user_manual_cn/21.png
.. |image21| image:: ../images/user_manual_cn/22.png
.. |image22| image:: ../images/user_manual_cn/23.png
.. |image23| image:: ../images/user_manual_cn/24.png
.. |image25| image:: ../images/user_manual_cn/25.png
.. |image26| image:: ../images/user_manual_cn/26.png
.. |image27| image:: ../images/user_manual_cn/27.png
.. |image28| image:: ../images/user_manual_cn/28.png
.. |image29| image:: ../images/user_manual_cn/29.png
.. |image30| image:: ../images/user_manual_cn/30.png
.. |image31| image:: ../images/user_manual_cn/31.png
.. |image32| image:: ../images/user_manual_cn/32.png