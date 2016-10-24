# 显示“hello world”
在这个练习中，我们将使用VPL创建第一个应用程序来显示单词“hello world”
1. 首先，从“文件”菜单中选择“新建”创建一个新工程。然后从基本活动工具箱（Basic Activities）中双击或者拖拽一个Data活动，放入到当前的活动流程图中去，从下拉表中选择“string”，点击数据块的文本框并输入“hello world”。

    ![](/assets/images/chp2/p4.png)    
    ![](/assets/images/chp2/p3.png)
2. 在服务工具箱（Services）里拖拽一个Simple Dialog活动，把他放入到Diagram中。

    ![](/assets/images/chp2/p5.png)
3. 现在从Data块的输出连接端开始拖出一条线到Simple Dialog块，Connections对话框自动打开，在第一个列表中选择DataValue，第二个列表中选择AlertDialog。

    ![](/assets/images/chp2/p1.png)
4. 打开Data Connections对话框，在下拉列表中选择“value”，然后点击“OK”按钮。

    ![](/assets/images/chp2/p2.png)
5. 现在选择“start”命令，或者按F5键来运行你的程序。如果你还没有保存你的工程，此时，你将被要求保存，请把你的工程命名为“Exercise_01"

    ![](/assets/images/chp2/p6.png)
