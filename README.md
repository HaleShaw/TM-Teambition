# TM-Teambition

Tampermonkey-Beautify the Teambition.

油猴插件-美化Teambition

## 设置页面

![设置](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/setting.png)

## 功能

### 一、企业

#### 1.1 通用

1. 左侧边栏添加“工时”按钮，一键直达企业工时统计页面

    **需在设置页面进行设置**

    > **URL获取方式：**
    >
    > 1. 在左侧边栏上，点击“更多”按钮 -> “全部应用” -> “工时”
    >
    > 2. 页面加载完成后，按`F12`进入开发者模式，找到第一个`iframe`的地址，即是工时应用的地址
    >
    > 3. 通常以`https://appshell.teambition.com/api/v1/organization/`开头
    >
    > 4. 也可通过“一键获取”按钮获取
    >
    >    `document.querySelectorAll('iframe')[0].src`

    ![工时按钮](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/1.WorktimeButton.png)

#### 1.2 工时应用

1. 紧凑工时应用页面，使其能在一页能展示完两周内容

2. 添加项目组过滤按钮，按项目组单独展示成员工时

    **需在设置页面进行设置**

    ```JSON
    {
      'button name':['username','username'],
      'button name':['username','username']
    }
    ```

3. 添加企业成员选择框，按企业成员单独展示工时

4. 管理人员通常数据为0，但又无法在表格中剔除自己，故可以在设置页面配置，将不必要人员从表格中移除。

5. 默认选中“计划工时”，表格中将实际工时和计划工时一起展示

    ```JSON
    ['username','username'];
    ```

6. 以不同颜色标记异常的计划工时

    ![工时应用](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/2.Worktime.png)

### 二、项目

#### 2.1 通用

1. 添加“LoadAll”按钮，表格视图下，可一键加载所有数据

    ![LoadAll](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/3.LoadAllButton.png)

#### 2.2 任务面板

1. 看板视图下，左移任务卡上的任务ID，防止鼠标悬浮时“…”按钮遮挡

    ![TaskID](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/4.TaskID.png)

2. 看板视图下，隐藏分组标题尾部的“…”按钮

    ![GroupAfter](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/5.GroupAfter.png)

3. 看板视图下，隐藏最后分组后面的新增按钮，减小页面宽度

    ![GroupNew](https://github.com/HaleShaw/TM-Teambition/raw/main/screenshots/6.GroupNew.png)
