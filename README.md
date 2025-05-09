# yysls辅助采集

## 项目简介

本项目是一个用于yysls的辅助采集工具。工具通过识别游戏窗口定点定采集物进行采集，拟按键操作，实现自动化采集功能，提升游戏体验。

## 功能

- 自动识别游戏窗口并启动采集流程
- 支持自定义采集物品、点赞操作模式及推送设置
- 提供图形用户界面（GUI），方便查看采集统计和配置参数
- 自动记录采集数据及日志，便于问题排查
-  增加自动服药（螺蛳肉，酱炒田螺）（测试阶段，仅在gui界面可以使用）
- 【注意】推送功能当前目前只支持bark，相关代码待完善

## 安装

1. 克隆项目到本地：
    ```bash
    git clone https://github.com/yourusername/yysls_collection_helper.git
    ```
2. 安装依赖：
    ```bash
    pip install -r requirements.txt
    ```

## 使用方法

1. 修改项目根目录下的 `config.ini` 文件，配置如下参数：
   - `collectible_name`：要采集的物品名称
   - `goods_name_1` 和 `goods_name_2`：采集成功后统计的物品名称
   - `need_push`：是否需要推送采集结果（1表示需要，但当前推送功能尚未实现）
   - `push_url`：推送接口地址
2. 运行主程序启动自动采集：
    ```bash
    python main.py
    ```
3. 或启动图形用户界面进行配置和监控：
    ```bash
    python gui.py
    ```

## 注意事项

- 本项目仅为代码交流，严禁非法使用。
- 严禁利用本工具进行任何违规、作弊、恶意或破坏游戏公平性的操作。  
  任何通过本工具进行的违规操作均与项目开发者无关，使用者应自行承担全部责任。
- 请务必遵守游戏运营方的相关规定和国家法律法规，切勿利用自动化功能损害游戏生态。
- 工具仅供学习和研究，如在正式游戏环境中使用，请确保获得合法授权，避免侵犯他人权益。

## 贡献

欢迎提交问题（issues）和合并请求（pull requests）来改进本项目，但请确保改动符合相关法律法规要求。

## 许可证

本项目采用 GPL 协议，详情请参阅 LICENSE 文件。

## 免责声明

本 yysls_collection_helper 程序（以下简称“程序”）由用户编写，仅供学习和研究目的使用。在使用本程序前，请仔细阅读以下免责声明：

**使用风险**  
使用本程序的风险由用户自行承担。程序的开发者不对因使用或无法使用本程序而产生的任何直接或间接损失承担任何责任。

**合法性**  
用户在使用本程序时应遵守相关法律法规及服务提供商的使用条款。程序的开发者不对用户因使用本程序而违反任何法律法规或服务条款承担责任。

**责任限制**  
在适用法律允许的最大范围内，程序的开发者不对因使用或无法使用本程序而导致的任何损害承担责任，包括但不限于利润损失、数据丢失或业务中断等。

通过下载、安装或使用本程序，用户即表示已阅读、理解并同意本免责声明的所有条款。如果用户不同意本免责声明中的任何条款，请不要使用本程序。

## 框架与依赖说明

本项目主要依赖以下框架和第三方库：
- **Flet**：用于构建跨平台图形用户界面 (GUI)。
- **OpenCV (cv2)**：用于图像处理与截图。
- **MSS**：用于屏幕截图。
- **EasyOCR**：用于图像文字识别。
- **Keyboard**：用于模拟键盘操作。
- **pyuac**：用于管理员权限判断与请求。
- **psutil**、**pygetwindow**、**pywin32**：用于系统与窗口操作。
