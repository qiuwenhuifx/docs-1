# ALTER VIEW<a name="ZH-CN_TOPIC_0242370548"></a>

## 功能描述<a name="zh-cn_topic_0237122084_zh-cn_topic_0059778428_section1274412112511"></a>

ALTER VIEW更改视图的各种辅助属性。（如果用户是更改视图的查询定义，要使用CREATE OR REPLACE VIEW。）

## 注意事项<a name="zh-cn_topic_0237122084_zh-cn_topic_0059778428_s5a554e8d15974449b7ffffee772b46f2"></a>

-   用户必须是视图的所有者才可以使用ALTER VIEW。
-   要改变视图的模式，用户必须要有新模式的CREATE权限。
-   要改变视图的所有者，用户必须是新所属角色的直接或者间接的成员，并且此角色必须有视图模式的CREATE权限。
-   管理员用户可以更改任何视图的所属关系。

## 语法格式<a name="zh-cn_topic_0237122084_zh-cn_topic_0059778428_s7a58ab6578844d1d826f43cf0be946f9"></a>

-   设置视图列的默认值。

    ```
    ALTER VIEW [ IF EXISTS ] view_name
        ALTER [ COLUMN ] column_name SET DEFAULT expression;
    ```

-   取消列视图列的默认值。

    ```
    ALTER VIEW [ IF EXISTS ] view_name
        ALTER [ COLUMN ] column_name DROP DEFAULT;
    ```

-   修改视图的所有者。

    ```
    ALTER VIEW [ IF EXISTS ] view_name 
        OWNER TO new_owner;
    ```

-   重命名视图。

    ```
    ALTER VIEW [ IF EXISTS ] view_name 
        RENAME TO new_name;
    ```

-   设置视图的所属模式。

    ```
    ALTER VIEW [ IF EXISTS ] view_name 
        SET SCHEMA new_schema;
    ```

-   设置视图的选项。

    ```
    ALTER VIEW [ IF EXISTS ] view_name
        SET ( { view_option_name [ = view_option_value ] } [, ... ] );
    ```

-   重置视图的选项。

    ```
    ALTER VIEW [ IF EXISTS ] view_name
        RESET ( view_option_name [, ... ] );
    ```


## 参数说明<a name="zh-cn_topic_0237122084_zh-cn_topic_0059778428_sf6542f9e45da4efcad90878c3159a286"></a>

-   **IF EXISTS**

    使用这个选项，如果视图不存在时不会产生错误，仅有会有一个提示信息。

-   **view\_name**

    视图名称，可以用模式修饰。

    取值范围：字符串，符合标识符命名规范。

-   **column\_name**

    可选的名称列表，视图的字段名。如果没有给出，字段名取自查询中的字段名。

    取值范围：字符串，符合标识符命名规范。

-   **SET/DROP DEFAULT**

    设置或删除一个列的缺省值，该参数暂无实际意义。

-   **new\_owner**

    视图新所有者的用户名称。

-   **new\_name**

    视图的新名称。

-   **new\_schema**

    视图的新模式。

-   **view\_option\_name \[ = view\_option\_value \]**

    该子句为视图指定一个可选的参数。

    目前view\_option\_name支持的参数仅有security\_barrier，当VIEW试图提供行级安全时，应使用该参数。

    取值范围：Boolean类型，TRUE、FALSE。


## 示例<a name="zh-cn_topic_0237122084_zh-cn_topic_0059778428_s3d5088f2366242cf9ef14a91c2081248"></a>

```
--创建一个由c_customer_sk小于150的内容组成的视图。
postgres=# CREATE VIEW tpcds.customer_details_view_v1 AS
    SELECT * FROM tpcds.customer
    WHERE c_customer_sk < 150;

--修改视图名称。
postgres=# ALTER VIEW tpcds.customer_details_view_v1 RENAME TO customer_details_view_v2;

--修改视图所属schema。
postgres=# ALTER VIEW tpcds.customer_details_view_v2 SET schema public;

--删除视图。
postgres=# DROP VIEW public.customer_details_view_v2;
```

## 相关链接<a name="zh-cn_topic_0237122084_zh-cn_topic_0059778428_s0c3f488fdb90433797e7d1561d9a074d"></a>

[CREATE VIEW](CREATE-VIEW.md)，[DROP VIEW](DROP-VIEW.md)

