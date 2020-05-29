# SET TRANSACTION<a name="ZH-CN_TOPIC_0242370654"></a>

## 功能描述<a name="zh-cn_topic_0237122190_zh-cn_topic_0059778135_se7890b9b6c9749168d76cd4ce38ee49f"></a>

为当前事务设置特性。它对后面的事务没有影响。事务特性包括事务隔离级别、事务访问模式\(读/写或者只读\)。

## 注意事项<a name="zh-cn_topic_0237122190_zh-cn_topic_0059778135_s91c8bf3e55a0490299ef9c0cd59f44f6"></a>

无。

## 语法格式<a name="zh-cn_topic_0237122190_zh-cn_topic_0059778135_sce3e49e1f5894684861d1df6677d12c8"></a>

设置事务的隔离级别、读写模式。

```
{ SET [ LOCAL ] TRANSACTION|SET SESSION CHARACTERISTICS AS TRANSACTION }
  { ISOLATION LEVEL { READ COMMITTED | READ UNCOMMITTED | SERIALIZABLE | REPEATABLE READ }
  | { READ WRITE | READ ONLY } } [, ...]
```

## 参数说明<a name="zh-cn_topic_0237122190_zh-cn_topic_0059778135_sedb5d46e1cef47ad953116db260be4ad"></a>

-   **LOCAL**

    声明该命令只在当前事务中有效。

-   **SESSION**

    声明这个命令只对当前会话起作用。

    取值范围：字符串，要符合标识符的命名规范。

-   **ISOLATION\_LEVEL\_CLAUSE**

    指定事务隔离级别，该参数决定当一个事务中存在其他并发运行事务时能够看到什么数据。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   在事务中第一个数据修改语句（INSERT，DELETE，UPDATE，FETCH，COPY）执行之后，事务隔离级别就不能再次设置。  

    取值范围：

    -   READ COMMITTED：读已提交隔离级别，只能读到已经提交的数据，而不会读到未提交的数据。这是缺省值。
    -   READ UNCOMMITTED：读未提交隔离级别，可能会读到未提交的数据。建议这种隔离级别下仅作只读操作，避免造成数据不一致。
    -   REPEATABLE READ：可重复读隔离级别，仅仅能看到事务开始之前提交的数据，不能看到未提交的数据，以及在事务执行期间由其它并发事务提交的修改。
    -   SERIALIZABLE：openGauss目前功能上不支持此隔离级别，等价于REPEATABLE READ。

-   **READ WRITE | READ ONLY**

    指定事务访问模式（读/写或者只读）。


## 示例<a name="zh-cn_topic_0237122190_zh-cn_topic_0059778135_sf3622c31002245c482e236cade222456"></a>

```
--开启一个事务，设置事务的隔离级别为READ COMMITTED，访问模式为READ ONLY。
postgres=# START TRANSACTION;
postgres=# SET LOCAL TRANSACTION ISOLATION LEVEL READ COMMITTED READ ONLY;
postgres=# COMMIT;
```
