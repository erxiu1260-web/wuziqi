# ♟️ 云端五子棋

两人实时五子棋网页应用。第一个进入房间的人执黑，第二个人执白，再进来的人可以观战。

> 小游戏「小猫去找小鱼」已经搬到单独的仓库：https://github.com/erxiu1260-web/xiaoyu
> 这里的 `xiaoyu/` 文件夹只放了跳转页，让以前发出去的旧链接还能打开。

## 文件

| 文件 | 是什么 |
|---|---|
| `server.js` | 服务器程序 |
| `public/` | 网页（棋盘界面） |
| `package.json` | 依赖和启动命令 |
| `start.bat` | Windows 上双击就能启动 |
| `xiaoyu/` | 小鱼游戏的旧链接跳转页，不用管 |

## 本机启动

在本目录运行：

```powershell
npm install
npm start
```

或者在 Windows 上直接双击 `start.bat`。第一次运行之前要先执行一次 `npm install`。

然后访问 [http://localhost:3000](http://localhost:3000)。点击"复制邀请链接"，把链接发给朋友，朋友就能加入同一个房间。

## 局域网联机

朋友需要和你连同一个 Wi-Fi 或局域网。把链接里的 `localhost:3000` 换成你电脑的局域网 IP，例如：

```text
http://192.168.1.20:3000/?room=ABC123
```

你电脑的局域网 IP 可以在终端运行 `ipconfig` 查看。如果 Windows 弹出防火墙提示，请允许 Node.js 使用专用网络。

## 公网线上联机

把整个文件夹上传到任何支持 Node.js 的托管平台，例如 Render、Railway 或者自己的云服务器，启动命令设为 `npm start`。平台分配的 HTTPS 地址就是在线地址，可以直接分享给朋友。程序会自动给每个新链接创建一个独立房间。

部署平台需要提供 `PORT` 环境变量，程序会自动读取它。
