# ALTER SCHEMA<a name="ZH-CN_TOPIC_0242370534"></a>

## 功能描述<a name="zh-cn_topic_0237122070_zh-cn_topic_0059779037_s806d414edb004fa89cd50a1166d1136e"></a>

修改模式属性。

## 注意事项<a name="zh-cn_topic_0237122070_zh-cn_topic_0059779037_sfccb497f01564edb804ecee58fe2698c"></a>

只有模式的所有者有权限执行ALTER SCHEMA命令，系统管理员默认拥有此权限。

## 语法格式<a name="zh-cn_topic_0237122070_zh-cn_topic_0059779037_s794bdb8d97844eb7aa7d1d6cdf896ac9"></a>

-   修改模式的名称。

    ```
    ALTER SCHEMA schema_name 
        RENAME TO new_name;
    ```

-   修改模式的所有者。

    ```
    ALTER SCHEMA schema_name 
        OWNER TO new_owner;
    ```


## 参数说明<a name="zh-cn_topic_0237122070_zh-cn_topic_0059779037_s8277cc73aecc4f20845d2ddf456a20e7"></a>

-   **schema\_name**

    现有模式的名称。

    取值范围：已存在的模式名。

-   **RENAME TO new\_name**

    修改模式的名称。

    new\_name：模式的新名称。

    取值范围：字符串，要符合标识符命名规范。

-   **OWNER TO new\_owner**

    修改模式的所有者。非系统管理员要改变模式的所有者，该用户还必须是新的所有角色的直接或间接成员， 并且该成员必须在此数据库上有CREATE权限。

    new\_owner：模式的新所有者。

    取值范围：已存在的用户名/角色名。


## 示例<a name="zh-cn_topic_0237122070_zh-cn_topic_0059779037_sd7a0dca78f6844d79a0ec70fb4213769"></a>

```
--创建模式ds。
postgres=# CREATE SCHEMA ds;

--将当前模式ds更名为ds_new。
postgres=# ALTER SCHEMA ds RENAME TO ds_new;

--创建用户jack。
postgres=# CREATE USER jack PASSWORD 'Bigdata@123';

--将DS_NEW的所有者修改为jack。
postgres=# ALTER SCHEMA ds_new OWNER TO jack;

--删除用户jack和模式ds_new。
postgres=# DROP SCHEMA ds_new;
postgres=# DROP USER jack;
```

## 相关链接<a name="zh-cn_topic_0237122070_zh-cn_topic_0059779037_seadab16e00ee41c383d8cba1759ed7c8"></a>

[CREATE SCHEMA](CREATE-SCHEMA.md)，[DROP SCHEMA](DROP-SCHEMA.md)

