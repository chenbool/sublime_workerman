# sublime_workerman

> Sublime Text 语法提示插件，支持 Workerman 框架

## 功能特性

| 特性 | 说明 |
|------|------|
| 代码片段 | 50+ 个代码片段 |
| 完整覆盖 | 覆盖 Workerman 核心功能 |
| 智能提示 | 支持 Tab 键快速补全 |
| 服务器类型 | 支持 WebSocket/TCP/HTTP |

## 安装

### Sublime Text 安装

1. 打开 Sublime Text
2. 按 `Ctrl+Shift+P` 打开命令面板
3. 输入 `Package Control: Install Package`
4. 搜索 `workerman` 并安装

### 手动安装

将项目克隆到 Sublime Text 的 Packages 目录：

```bash
git clone https://github.com/chenbool/sublime_workerman.git
```

## 代码片段总览

| 分类 | 数量 | 说明 |
|------|------|------|
| Server | 25 | 服务器配置 |
| Worker | 4 | Worker进程 |
| Connection | 7 | 连接管理 |
| Async | 4 | 异步操作 |
| Timer | 4 | 定时器 |
| Client | 1 | 客户端 |

## 使用示例

```php
// WebSocket 服务器
$ws = new Worker('websocket://0.0.0.0:2346');
$ws->onMessage = function($connection, $data) {
    $connection->send($data);
};
Worker::runAll();

// TCP 服务器
$tcp = new Worker('tcp://0.0.0.0:2347');
$tcp->onMessage = function($connection, $data) {
    $connection->send($data);
};
Worker::runAll();

// 定时器
Timer::add(1, function() {
    echo "Hello\n";
});
```

## 相关项目

| 项目 | 仓库地址 |
|------|----------|
| sublime_swoole | https://github.com/chenbool/sublime_swoole |
| sublime_yaf | https://github.com/chenbool/sublime_yaf |
| sublime_thinkphp5 | https://github.com/chenbool/sublime_thinkphp5 |
| sublime_thinkphp6 | https://github.com/chenbool/sublime_thinkphp6 |
| sublime_thinkphp8 | https://github.com/chenbool/sublime_thinkphp8 |
| sublime_laravel | https://github.com/chenbool/sublime_laravel |
| sublime_workerman | https://github.com/chenbool/sublime_workerman |
| sublime_webman | https://github.com/chenbool/sublime_webman |
| sublime_fastadmin | https://github.com/chenbool/sublime_fastadmin |

## License

MIT License
