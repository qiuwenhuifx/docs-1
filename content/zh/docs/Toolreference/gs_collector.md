# gs\_collector<a name="ZH-CN_TOPIC_0242223666"></a>

## 背景信息<a name="zh-cn_topic_0237152334_zh-cn_topic_0059778085_section1813744893314"></a>

当openGauss发生故障时，使用此工具收集OS信息、日志信息以及配置文件等信息，来定位问题。可以使用-C参数，指定收集不同的信息内容，具体支持收集的内容信息如[表1](#zh-cn_topic_0237152334_table18101312318)所示。

**表 1**  gs\_collector内容收集对照表

<a name="zh-cn_topic_0237152334_table18101312318"></a>
<table><thead align="left"><tr id="zh-cn_topic_0237152334_row21012382317"><th class="cellrowborder" valign="top" width="15.6%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0237152334_p171112382318"><a name="zh-cn_topic_0237152334_p171112382318"></a><a name="zh-cn_topic_0237152334_p171112382318"></a>TypeName</p>
</th>
<th class="cellrowborder" valign="top" width="20.849999999999998%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0237152334_p21183192318"><a name="zh-cn_topic_0237152334_p21183192318"></a><a name="zh-cn_topic_0237152334_p21183192318"></a>Content</p>
</th>
<th class="cellrowborder" valign="top" width="38.550000000000004%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0237152334_p21116316232"><a name="zh-cn_topic_0237152334_p21116316232"></a><a name="zh-cn_topic_0237152334_p21116316232"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0237152334_p12111832231"><a name="zh-cn_topic_0237152334_p12111832231"></a><a name="zh-cn_topic_0237152334_p12111832231"></a>是否默认收集</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0237152334_row17118322316"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p121114320238"><a name="zh-cn_topic_0237152334_p121114320238"></a><a name="zh-cn_topic_0237152334_p121114320238"></a>System</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p9173483258"><a name="zh-cn_topic_0237152334_p9173483258"></a><a name="zh-cn_topic_0237152334_p9173483258"></a>HardWareInfo</p>
<p id="zh-cn_topic_0237152334_p6181348172513"><a name="zh-cn_topic_0237152334_p6181348172513"></a><a name="zh-cn_topic_0237152334_p6181348172513"></a>RunTimeInfo</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><div class="p" id="zh-cn_topic_0237152334_p698955702519"><a name="zh-cn_topic_0237152334_p698955702519"></a><a name="zh-cn_topic_0237152334_p698955702519"></a>收集现在操作系统的状态信息：<a name="zh-cn_topic_0237152334_ul9921101417234"></a><a name="zh-cn_topic_0237152334_ul9921101417234"></a><ul id="zh-cn_topic_0237152334_ul9921101417234"><li>HardWareInfo</li><li>Cpu（cat /proc/cpuinfo）</li><li>内存（cat /proc/meminfo）</li><li>磁盘（df -h）</li><li>RunTimeInfo：</li><li>topStatus（ps ux）</li><li>ioStat（iostat -xm 2 3）</li><li>网络状态（cat /proc/net/dev）</li><li>内存使用情况（free -m）</li></ul>
</div>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p11283122310"><a name="zh-cn_topic_0237152334_p11283122310"></a><a name="zh-cn_topic_0237152334_p11283122310"></a>是</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row61219372311"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p111263102314"><a name="zh-cn_topic_0237152334_p111263102314"></a><a name="zh-cn_topic_0237152334_p111263102314"></a>Database</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p103186476250"><a name="zh-cn_topic_0237152334_p103186476250"></a><a name="zh-cn_topic_0237152334_p103186476250"></a>具体列表见<a href="gs_collector工具支持收集的系统表和视图列表.md#zh-cn_topic_0237637502_table15624104912196">表1</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0237152334_p127501419122615"><a name="zh-cn_topic_0237152334_p127501419122615"></a><a name="zh-cn_topic_0237152334_p127501419122615"></a>收集系统视图或者系统表的内容。</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p022210297269"><a name="zh-cn_topic_0237152334_p022210297269"></a><a name="zh-cn_topic_0237152334_p022210297269"></a>是，默认收集pg_locks，pg_stat_activity和 pg_thread_wait_status三个视图的信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row101318382316"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p6133313233"><a name="zh-cn_topic_0237152334_p6133313233"></a><a name="zh-cn_topic_0237152334_p6133313233"></a>Log</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p8657174819262"><a name="zh-cn_topic_0237152334_p8657174819262"></a><a name="zh-cn_topic_0237152334_p8657174819262"></a><span id="ph135301241151111"><a name="ph135301241151111"></a><a name="ph135301241151111"></a>DBnode</span></p>
<p id="zh-cn_topic_0237152334_p1565711483268"><a name="zh-cn_topic_0237152334_p1565711483268"></a><a name="zh-cn_topic_0237152334_p1565711483268"></a>Gtm</p>
<p id="zh-cn_topic_0237152334_p46574483267"><a name="zh-cn_topic_0237152334_p46574483267"></a><a name="zh-cn_topic_0237152334_p46574483267"></a>ClusterManager</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><a name="zh-cn_topic_0237152334_ul122531334158"></a><a name="zh-cn_topic_0237152334_ul122531334158"></a><ul id="zh-cn_topic_0237152334_ul122531334158"><li>收集<span id="ph281904381112"><a name="ph281904381112"></a><a name="ph281904381112"></a>DBnode</span>的pg_log和gs_profile</li><li>收集Gtm下的pg_log</li><li>收集ClusterManager的日志信息包括：<a name="zh-cn_topic_0237152334_ul19311954111513"></a><a name="zh-cn_topic_0237152334_ul19311954111513"></a><ul id="zh-cn_topic_0237152334_ul19311954111513"><li>cm_agent</li><li>om</li><li>cm_ctl</li><li>gs_clean</li><li>gs_ctl</li><li>gs_guc</li><li>gs_initcm</li><li>gs_initdb</li><li>gs_initgtm</li><li>gtm_ctl</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p1014133162314"><a name="zh-cn_topic_0237152334_p1014133162314"></a><a name="zh-cn_topic_0237152334_p1014133162314"></a>是</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row71412352318"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p1514135239"><a name="zh-cn_topic_0237152334_p1514135239"></a><a name="zh-cn_topic_0237152334_p1514135239"></a>Config</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p20995135132817"><a name="zh-cn_topic_0237152334_p20995135132817"></a><a name="zh-cn_topic_0237152334_p20995135132817"></a><span id="ph01581049161115"><a name="ph01581049161115"></a><a name="ph01581049161115"></a>DBnode</span></p>
<p id="zh-cn_topic_0237152334_p109951951162817"><a name="zh-cn_topic_0237152334_p109951951162817"></a><a name="zh-cn_topic_0237152334_p109951951162817"></a>Gtm</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><a name="zh-cn_topic_0237152334_ul498532372610"></a><a name="zh-cn_topic_0237152334_ul498532372610"></a><ul id="zh-cn_topic_0237152334_ul498532372610"><li>收集<span id="ph691485017118"><a name="ph691485017118"></a><a name="ph691485017118"></a>DBnode</span>的配置信息:<a name="zh-cn_topic_0237152334_ul1741811415273"></a><a name="zh-cn_topic_0237152334_ul1741811415273"></a><ul id="zh-cn_topic_0237152334_ul1741811415273"><li>postgresql.conf</li><li>gaussdb.state</li><li>pg_hba.conf</li><li>pg_control</li><li>pg_replslot</li><li>pg_ident.conf</li></ul>
</li><li>收集Gtm配置信息:<a name="zh-cn_topic_0237152334_ul03351418192614"></a><a name="zh-cn_topic_0237152334_ul03351418192614"></a><ul id="zh-cn_topic_0237152334_ul03351418192614"><li>gtm.conf</li><li>gtm.control</li><li>gtm.sequence</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p515933239"><a name="zh-cn_topic_0237152334_p515933239"></a><a name="zh-cn_topic_0237152334_p515933239"></a>是</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row181513312235"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p81518317232"><a name="zh-cn_topic_0237152334_p81518317232"></a><a name="zh-cn_topic_0237152334_p81518317232"></a>Gstack</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p979113464295"><a name="zh-cn_topic_0237152334_p979113464295"></a><a name="zh-cn_topic_0237152334_p979113464295"></a><span id="ph2051915528115"><a name="ph2051915528115"></a><a name="ph2051915528115"></a>DBnode</span></p>
<p id="zh-cn_topic_0237152334_p779214612913"><a name="zh-cn_topic_0237152334_p779214612913"></a><a name="zh-cn_topic_0237152334_p779214612913"></a>Gtm</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0237152334_p41510310234"><a name="zh-cn_topic_0237152334_p41510310234"></a><a name="zh-cn_topic_0237152334_p41510310234"></a>利用gstack命令得到<span id="ph151395421112"><a name="ph151395421112"></a><a name="ph151395421112"></a>DBnode</span>，GTM的当前堆栈信息。</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p12151316239"><a name="zh-cn_topic_0237152334_p12151316239"></a><a name="zh-cn_topic_0237152334_p12151316239"></a>否</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row1715638237"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p2151038237"><a name="zh-cn_topic_0237152334_p2151038237"></a><a name="zh-cn_topic_0237152334_p2151038237"></a>CoreDump</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p86827507318"><a name="zh-cn_topic_0237152334_p86827507318"></a><a name="zh-cn_topic_0237152334_p86827507318"></a>gaussdb</p>
<p id="zh-cn_topic_0237152334_p148532053173114"><a name="zh-cn_topic_0237152334_p148532053173114"></a><a name="zh-cn_topic_0237152334_p148532053173114"></a>gs_gtm</p>
<p id="zh-cn_topic_0237152334_p94925568313"><a name="zh-cn_topic_0237152334_p94925568313"></a><a name="zh-cn_topic_0237152334_p94925568313"></a>gs_rewind</p>
<p id="zh-cn_topic_0237152334_p65861858113113"><a name="zh-cn_topic_0237152334_p65861858113113"></a><a name="zh-cn_topic_0237152334_p65861858113113"></a>cm_server</p>
<p id="zh-cn_topic_0237152334_p2242151103216"><a name="zh-cn_topic_0237152334_p2242151103216"></a><a name="zh-cn_topic_0237152334_p2242151103216"></a>cm_agent</p>
<p id="zh-cn_topic_0237152334_p16196104803113"><a name="zh-cn_topic_0237152334_p16196104803113"></a><a name="zh-cn_topic_0237152334_p16196104803113"></a>gs_ctl</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0237152334_p5229047123010"><a name="zh-cn_topic_0237152334_p5229047123010"></a><a name="zh-cn_topic_0237152334_p5229047123010"></a>通过时间筛选gaussdb进程和gtm进程的core文件。</p>
<div class="caution" id="zh-cn_topic_0237152334_note1316119421297"><a name="zh-cn_topic_0237152334_note1316119421297"></a><a name="zh-cn_topic_0237152334_note1316119421297"></a><span class="cautiontitle"> 注意： </span><div class="cautionbody"><p id="zh-cn_topic_0237152334_p016104214295"><a name="zh-cn_topic_0237152334_p016104214295"></a><a name="zh-cn_topic_0237152334_p016104214295"></a>关于Core的配置和方式请按照如下要求：在/proc/sys/opengauss/core_pattern文件中添加core文件的格式：core-%e-%p-%t。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p181614310230"><a name="zh-cn_topic_0237152334_p181614310230"></a><a name="zh-cn_topic_0237152334_p181614310230"></a>否</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row41613192315"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p71613318234"><a name="zh-cn_topic_0237152334_p71613318234"></a><a name="zh-cn_topic_0237152334_p71613318234"></a>XLog</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p566195453213"><a name="zh-cn_topic_0237152334_p566195453213"></a><a name="zh-cn_topic_0237152334_p566195453213"></a><span id="ph84941255161117"><a name="ph84941255161117"></a><a name="ph84941255161117"></a>DBnode</span></p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0237152334_p0174312313"><a name="zh-cn_topic_0237152334_p0174312313"></a><a name="zh-cn_topic_0237152334_p0174312313"></a>通过时间筛选收集xlog。</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p16174392310"><a name="zh-cn_topic_0237152334_p16174392310"></a><a name="zh-cn_topic_0237152334_p16174392310"></a>否</p>
</td>
</tr>
<tr id="zh-cn_topic_0237152334_row6136229183317"><td class="cellrowborder" valign="top" width="15.6%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0237152334_p9138429193316"><a name="zh-cn_topic_0237152334_p9138429193316"></a><a name="zh-cn_topic_0237152334_p9138429193316"></a>Plan</p>
</td>
<td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0237152334_p713892916335"><a name="zh-cn_topic_0237152334_p713892916335"></a><a name="zh-cn_topic_0237152334_p713892916335"></a>*</p>
</td>
<td class="cellrowborder" valign="top" width="38.550000000000004%" headers="mcps1.2.5.1.3 "><div class="p" id="zh-cn_topic_0237152334_p45021115203417"><a name="zh-cn_topic_0237152334_p45021115203417"></a><a name="zh-cn_topic_0237152334_p45021115203417"></a>收集计划复现信息：<a name="zh-cn_topic_0237152334_ul16465440162515"></a><a name="zh-cn_topic_0237152334_ul16465440162515"></a><ul id="zh-cn_topic_0237152334_ul16465440162515"><li>用户输入*表示收集所有数据库上的计划复现信息。</li><li>用户输入具体的数据库名称表示收集指定数据库上的计划复现信息。</li></ul>
</div>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0237152334_p8138132953313"><a name="zh-cn_topic_0237152334_p8138132953313"></a><a name="zh-cn_topic_0237152334_p8138132953313"></a>否</p>
</td>
</tr>
</tbody>
</table>

## 前提条件<a name="zh-cn_topic_0237152334_zh-cn_topic_0059778085_s7bffe8e9bdec4735885781573a71fb91"></a>

日志收集工具依赖操作系统工具，例如gstack为其中一种，如果未安装该工具，则提示错误后，跳过该收集项。

## 语法<a name="zh-cn_topic_0237152334_zh-cn_topic_0059778085_s95ba74a509904128ac0326c58acd840c"></a>

-   日志收集（非root用户）

    ```
    gs_collector --begin-time="BEGINTIME" --end-time="ENDTIME" [-h HOSTNAME | -f HOSTFILE] [--keyword=KEYWORD] [--speed-limit=SPEED] [-o OUTPUT] [-l LOGFILE] [-C CONFIGFILE]
    ```

-   显示帮助信息

    ```
    gs_collector -? | --help
    ```

-   显示版本号信息

    ```
    gs_collector -V | --version
    ```


## 参数说明<a name="zh-cn_topic_0237152334_zh-cn_topic_0059778085_s7ac81eecbbdd4ae28db3ffe0efb5a947"></a>

-   -h

    收集信息的主机名称。

    取值范围：主机名称，只能指定一个主机名称。

    如果不指定则默认收集所有主机的信息。

-   -f

    主机名称列表文件。该文件为纯文本格式。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-f和-h参数不能同时使用。  

    取值范围：主机名称列表。

-   -o

    将收集日志以压缩包形式输出到指定的文件夹。

    不指定则将检查结果以压缩包形式输出到配置文件中tmpMppdbPath选项所指定的目录中。

    若配置文件中未配置tmpMppdbPath选项，则默认将检查结果以压缩包形式输出到“/tmp/用户名\_mppdb/”目录中。

-   -l

    指定的日志文件以及存放路径。

-   -C

    指定待收集内容的配置文件，利用TypeName指定需要收集的信息类型，利用Content指定每一类信息的具体内容，利用Count指定此类信息收集的次数，利用Interval指定收集间隔，单位为秒。

    TypeName和Content不允许缺失或者内容为空。

    Interval和Count可以不指定，如果没有指定Count，则默认收集一次。如果没有指定Interval则表示间隔为0秒，Interval和Count的值不能小于0。

    如果不指定则使用默认的配置文件。

    配置文件格式采用json格式，模板如下：

    ```
    {
        "Collect":
        [
            {"TypeName": "name", "Content":"value","Interval":"seconds", "Count":"count"}
        ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >默认配置文件内容如下：  
    >\{  
    >"Collect":  
    >\[  
    >\{"TypeName": "System", "Content":"RunTimeInfo, HardWareInfo","Interval":"0", "Count":"1"\},  
    >\{"TypeName": "Log", "Content" : "DBnode,Gtm,ClusterManager", "Interval":"0", "Count":"1"\},  
    >\{"TypeName": "Database", "Content": "pg\_locks,pg\_stat\_activity,pg\_thread\_wait\_status","Interval":"0", "Count":"1"\},  
    >\{"TypeName": "Config", "Content": "DBnode,Gtm", "Interval":"0", "Count":"1"\}  
    >\]  
    >\}  
    >TypeName和对应的Content取值范围见表1gs\_collector内容收集对照表。  
    >对于Log，CoreDump，Config，XLog三种类型，Interval和Count参数不生效。  

-   --keyword=KEYWORD

    包含关键字KEYWORD的日志文件。

    若关键字KEYWORD中含有空格，需要使用双引号包围。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >性能日志为二进制日志，关键字搜集功能不支持该日志的搜集。  

-   --begin-time

    日志的开始时间。输入格式为“yyyymmdd hh:mm”。

-   --end-time

    日志的结束时间。输入格式为“yyyymmdd hh:mm”。

-   --speed-limit

    日志收集时的收集速率，输入格式为非负整数，单位为MB/s。

    该参数主要是为了防止日志收集过程中产生过高的磁盘或网络IO，导致数据库节点故障（如果它们与$GAUSSLOG/$PGHOST部署在同一个磁盘上）。该值应当不超过openGauss内上述磁盘IO与网络IO速率的最小值的1/3。

-   -?, --help

    显示帮助信息。

-   -V, --version

    显示版本号信息。


## 示例<a name="zh-cn_topic_0237152334_zh-cn_topic_0059778085_sc5fc8de2cfd140fcb92d4f3d1b100ace"></a>

执行如下命令收集OS信息和日志信息。

```
gs_collector --begin-time="20180131 23:00" --end-time="20180201 20:00" -h plat1 
Successfully parsed the configuration file.
Collecting OS information.
Successfully collected OS information.
Collecting catalog statistics.
Successfully collected catalog statistics.
Collecting log files.
Successfully collected log files.
Collecting configuration files and process stack information.
Successfully collected configuration files and processed stack information.
Collecting files.
Successfully collected files.
All results are stored in $PGHOST/collector_20180201_144951.tar.gz.
```

查看收集到的统计信息。

```
tar -zxvf $PGHOST/collector_20180201_144951.tar.gz
collector_20180201_144951/
collector_20180201_144951/plat1.tar.gz
cd collector_20180201_144951
tar -zxvf plat1.tar.gz
plat1/
plat1/OS_information.txt
plat1/conffiles/
plat1/conffiles/dn_6006/
plat1/conffiles/dn_6006/pg_hba.conf
plat1/conffiles/dn_6006/postgresql.conf
plat1/conffiles/dn_6001/
plat1/conffiles/dn_6001/pg_hba.conf
plat1/conffiles/dn_6001/postgresql.conf
plat1/conffiles/dn_3003/
plat1/conffiles/dn_3003/pg_hba.conf
plat1/conffiles/dn_3003/postgresql.conf
plat1/Catalog_statistics.txt
plat1/logfiles/
plat1/logfiles/log_20180201_144957.tar
cd plat1/logfiles/
tar -xvf log_20180201_144957.tar
./
./om/
./om/gs_local-2018-01-30_165832.log
./om/gs_collector-2018-02-01_144951.log
./bin/
./bin/gs_clean/
./bin/gs_clean/gs_clean-2018-01-30_170147-current.log
./pg_log/
./pg_log/dn_6006/
./pg_log/dn_6006/postgresql-2018-01-31_000000.log
./pg_log/dn_6006/postgresql-2018-02-01_000000.log
./pg_log/cn_5001/
./pg_log/cn_5001/postgresql-2018-01-31_000000.log
./pg_log/cn_5001/postgresql-2018-02-01_000000.log
./pg_log/dn_6001/
./pg_log/dn_6001/postgresql-2018-01-31_000000.log
./pg_log/dn_6001/postgresql-2018-02-01_000000.log
./pg_log/dn_3003/
./pg_log/dn_3003/postgresql-2018-01-31_000000.log
./pg_log/dn_3003/postgresql-2018-02-01_000000.log
./gs_profile/
./gs_profile/dn_6001_6002/
./gs_profile/dn_6001_6002/postgresql-2018-02-01_000000.prf
./gs_profile/postgresql-2018-01-31_000000.prf
./gs_profile/dn_6003_3003/
./gs_profile/dn_6003_3003/postgresql-2018-02-01_000000.prf
./gs_profile/dn_6005_6006/
./gs_profile/dn_6005_6006/postgresql-2018-02-01_000000.prf
./gs_profile/postgresql-2018-02-01_000000.prf
```
