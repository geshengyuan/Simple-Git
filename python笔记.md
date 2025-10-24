#第二节 变量和数据类型
    注释的分类和语法
        单行注释    #
        多行注释    “““   ”””/‘‘‘   ’’’

    定义变量
        变量=值

    标识符命名规则
        1，由数字，字母，下划线组成
        2，不能数字开头
        3，不能使用内置关键字
        4，严格区分大小写

    命名习惯
        1，见名知义
        2，大驼峰：每个单词首字母都大写    eg：MyName
        3，小驼峰：第二个（含）以后的单词首字母大写    eg：myName
        4，下划线：    eg：my_name

    Debug
        打断点
            位置：目标要调试的代码块的第一行代码即可，即一个断点即可
    
    认识数据类型
        数值
            int（整型）
            float（浮点型）
        布尔型（bool）
            True(真)
            False（假）
        str
            (字符串)    数据都要带引号
        list
            （列表）    【】
        tuple
            （元组）    （）
        set
            （集合）    {}
        dict
            （字典）    键值对    {‘XX’：‘XX’}

    检测数据类型--type(数据)
        print(type(变量))

    格式化输出
        格式符号
            %s    字符串
            %d    有符号的十进制整数
            %F    浮点数
            %C    字符
            %U    无符号的十进制整数

            %.xf     保留小数点后x位
            %0xd    表示输出的整数显示位数，不足则以0补全，超出当前位数则原样

            print('A,B' 5 (a,b))

    格式化字符串除了%s，还可以写    f'{表达式}'

    转义符号
        \n：换行    默认end=“\n”
        \t：制表符，一个 tab 键为四个空格    print(‘xxx’，end=“?”)

#第三节 数据转换类型和运算符
    输入
        input（‘提示信息’）

    特点
        1，遇到input，等待用户输入
        2，接收input存变量
        3，input接受到的数据类型都是字符串    （str）

    转换数据类型的函数
    int（x）
    float（x）
    str（x）
    eval（str）用来计算在字符串中的有效python表达式，并返回一个对象
    tuple（s）
    list（s）

    Pycharm交互式开发 （简单）
        python console

    运算符的分类
        算法
        赋值
        复合赋值
        比较
        逻辑

    算法运算符
        +，-，*，/
        //整除    9//4结果为2
         %取余    9%4结果为1
        **指数    2**4结果为16
        （）      小括号

    赋值运算符
        =
            多个变量赋值
                A,B,C=a,b,c
            多变量赋相同值
                a=b=?
        
    复合赋值运算符
        +=    加法赋值运算符
        -=    减法赋值运算符
        *=    乘法赋值运算符
        /=    除法赋值运算符
        //=   整除赋值运算符
        %=    取余赋值运算符
        **=   幂赋值运算符

    比较运算符
        ==    判断相等
        ！=    不等于
        >
        <
        >=
        <=

    逻辑运算符
        and与    (x)and(y)    都真才真
        or或    （x）or(y)    一真才真，都假才假
        not非    not(x)       取真

    拓展
        数字之间的逻辑运算
            and运算符，只要有一个值为0，则结果为0，否则结果为最后一个非0的数
            or运算符，只有所有值为0结果才为0，否则结果为第一个非0数字

第四节 if语法


    if语法
        '''if条件：
            ____条件成立执行的代码1
            ____条件成立执行的代码2
            ____......
        '''
        注：在if下方的没有加缩进的代码，不属于if语句块，即和条件成立与否无关

    if...else...
        条件成立执行if下方的代码；条件不成立执行else下方的代码

        如果某些条件成立执行了相关的代码，那么其他的情况的代码解释器根本不会执行

    多重判断
        if 条件1：
            xxxxx
            xxxxx
            ......
        elif 条件2：
            xxxxx
            xxxxx
            ......
        elif 条件3：
            xxxxx
            xxxxx
            ......
        ......
        else:
            以上条件都不成立执行的代码

    if嵌套
        if 条件1：
            条件1成立执行
            条件1成立执行

            if 条件2：
                条件2成立的代码
                条件2成立的代码

    应用：猜拳游戏
        随机做法
            1，导出random模块
            2，使用random模块中的随机整数功能
            random.randint(开始，结束)

    三目运算符
        条件成立执行的表达式   if   条件   else   条件不成立执行的表达式

#第五节 While循环
     一，循环简介
        1.1 循环的作用
            让代码更高效的重复执行

        1.2 循环的分类
            while和for
        
    二，while的语法
         while 条件:
            条件成立重复执行的代码1
            条件成立重复执行的代码2
            ...... 

            ```
            i = 0
            while i < 5:
                print('xxx')
                i += 1
                print
            ```
            注意缩进

    三， while的应用
        应用一：计算1到100累加和
            ```
            i=1
            result = 0
            while i<= 100:
                result = result + i
                i += 1
            print (result)

        应用二：计算1到100偶数累加和
            方法1
            ```
            i = 1
            result = 0
            while i <= 100
                if i % 2 == 0:
                    result += i
                i += 1
            print(result)

            方法2
            ```
            i = 0
            result = 0
            while i <= 100:
                result += i
                i += 2
            print(result)

    四，break和continue
        4，1 理解
            break：终止此循环
            continue： 推出当前一次循环继而执行下一次循环代码
        4，1，1 情况一： break
            ```
            i = 1
            while i <= 5:
                if i == 4:
                    print('吃饱了，不吃了’)
                    break
                print(f'吃了第{i}个苹果')
                i += 1
            ```  

        4，1，2 情况二：continue
            ```
            i = 1
            while 1 <= 5:
                if i == 3:
                    print('吃出一个大虫子，这个苹果不吃了')
                    #如果使用continue，在continue之前一定要修改计数器，否则陷入死循环
                    i += 1
                    continue
                print(f'吃了第{i}个苹果)    
                i += 1

    五，while循环嵌套
        5，1 语法
            while 条件1：
                条件1 成立执行的代码
                ......
                while 条件2：
                    条件2成立执行的代码
                    ......

    六，while循环嵌套应用
        6，1 应用1：打印星号（正方形）
        #重复打印5行星星
        ```
        j = 0
        while j <= 4:
            #一行星星的打印
            1 = 0
            while i <=4:
                #一行内的星星不能换行，取消print默认结束符\n
                print('*'，end='')
                i += 1
            #每行结束要换行，这里借助一个空的print，利用print默认结束符换行
            print()
            j += 1
        ```

        6，2 应用2：打印星号（三角形）
        #重复打印5行星星
        #j表示行号
        j = 0
        while j <= 4:
            #一行星星的打印
            i = 0
            #i表示每行里面星星的个数，这个数字要和行号相等所以i要和j联动
            while i <= j:
                print('*',end='')
                i += 1
            print()
            j += 1

        6，3 九九乘法表
            ```
            j = 1
            while j <= 9
                i = 1
                while i <= j:
                    print(f'{i} * {j} = {i*j} * x',end='\t')
                    i += 1
                print()
                j += 1

#第六节，for循环
    7,1 语法
        ```
        for 临时变量 in 序列：
        重复执行的代码1
        重复执行的代码2
        ......
        ```
    7,2 快速体验
        ```
        str1 = 'abc'
        for i in str1:
            print(i)
        ```
    7,3 break
    ```
    str1 = 'abc'
    for i = in str1:
        if i == 'b':
            print('遇到b不打印')
            break
        print(i)
        ```

    7,4 continue
        ```
        str1 = 'abc'
        for 1 in str1:
            if 1 == 'b':
                print('遇到b不打印)
                continue
            print(i)

八， else
    循环可以和else配合使用，else下方缩进的代码指的是当循环正常结束之后要执行的代码
    8，1 while... else
        ```
        while 条件：
            条件成立重复执行的代码
        else：
            循环正常结束之后要执行的代码

    8，1，3 退出循环的方式
        break
        ```
        i = 1
        while i <= 5:
            if i == 3:
                break
            print('xxx')
            i += 1
        else:
            print('xxx')
        ```
        *else值得是循环正常结束之后要执行的代码，如果是break种植循环的情况，else下方缩进的代码将不执行*

        continue
        ```
        i = 1
        while i <= 5:
            if i == 3:
                i += 1
                break
            print('xxx')
            i += 1
        else:
            print('xxx')
        ```              
        *continue是退出当前一次循环，继续下一次循环，所以该循环在continue控制下是可以正常结束的，当循环结束后，则执行了else缩进的代码*

    8，2 for...else
        8，2，1 语法
            for 临时变量 in 序列：
                重复执行的代码
                ...
            else：
                循环正常结束之后要执行的代码
        8，2，2 示例
            str = 'abc'
            for i in str:
                print(i)
            else:
                print('循环正常结束之后执行的代码')

        8，2，3 退出循环的方式
            1，break终止循环
            ```
            str1 = 'abc'
            for i in str1:
                if 1 == 'b':
                    print('遇到b不打印')
                    break
                print(i)
            else:
                print('循环正常结束之后执行的代码')



#课程：字符串
    一，认识字符串
        字符串是python中最常用的数据类型。我们一般使用i引号来创建字符串。创建字符串很简单，只要为变量分配一个值即可

        注意：控制台显示结果为<class'str'>，即数据类型为str（字符串）。

        1，1 字符串特征
            *一对引号字符串
                'x'或者"x"
            *三引号字符串
                '''x'''
                """x"""
                
                





        

                
        
        
        
        
           

    
        
            





