   
    --// 存储过程，自定义功能 ----------
    -- 定义
    存储存储过程 是一段代码（过程），存储在数据库中的sql组成。
    一个存储过程通常用于完成一段业务逻辑，例如报名，交班费，订单入库等。
    而一个函数通常专注与某个功能，视为其他程序服务的，需要在其他语句中调用函数才可以，而存储过程不能被其他调用，是自己执行 通过call执行。
    
    -- 创建
    CREATE PROCEDURE sp_name (参数列表)
        过程体
    
    参数列表：不同于函数的参数列表，需要指明参数类型
    IN，表示输入型
    OUT，表示输出型
    INOUT，表示混合型
    
    注意，没有返回值。
    
    
    /* 存储过程 */ ------------------
    存储过程是一段可执行性代码的集合。相比函数，更偏向于业务逻辑。
    调用：CALL 过程名
    -- 注意
    - 没有返回值。
    - 只能单独调用，不可夹杂在其他语句中
    
    -- 参数
    IN|OUT|INOUT 参数名 数据类型
    IN        输入：在调用过程中，将数据输入到过程体内部的参数
    OUT        输出：在调用过程中，将过程体处理完的结果返回到客户端
    INOUT    输入输出：既可输入，也可输出
    
    -- 语法
    CREATE PROCEDURE 过程名 (参数列表)
    BEGIN
        过程体
    END
    