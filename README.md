# •#使用Heroku部署Xray高性能代理服務，（WebSocket tls、vmess、vless、木馬、shadowsocks和socks等）
> 

### Server

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://dashboard.heroku.com/new?template=https://github.com/hearbe/xravledo) 

3、账号填写的格式：
 服务器地址：自选ip
* 端口：443
* UUID： (UUID码)
* 加密：none
* 传输协议：ws
* 伪装类型：none
* 伪装host：****.workes.dev
* path路径：/自定义UUID码-vless 或 /自定义UUID码-vmess    (注意：前有斜杠/)
* vmess额外id（alterid）：0
* 底层传输安全：tls
* 跳过证书验证：false
* SNI地址：****.workes.dev

<details>
<summary>V2rayN(Xray, V2ray)</summary>

```bash
* Client download：https://github.com/2dust/v2rayN/releases
* Proxy protocol：vless or vmess
* Address：xxx.herokuapp.com
* Port：443
* Default UUID：24b4b1e1-7a89-45f6-858c-242cf53b5bdb
* vmess alter ID：0
* encryption：none
* transmission protocol：ws
* camouflage type：none
* camouflage domain name：xxx.workers.dev ((CF Workers url)
* path：/24b4b1e1-7a89-45f6-858c-242cf53b5bdb-vless // default - vless (/custom UUID-vless), if you wanna use vmess (/custom UUID-vmess)
* Underlying transmission security：tls
* allow inscure：false
```
</details>

<details>
<summary>Trojan-Go</summary>

```bash
* Client download: https://github.com/p4gefau1t/trojan-go/releases
{
    "run_type": "client",
    "local_addr": "127.0.0.1",
    "local_port": 1080,
    "remote_addr": "xxx.herokuapp.com",
    "remote_port": 443,
    "password": [
        "24b4b1e1-7a89-45f6-858c-242cf53b5bdb"
    ],
    "websocket": {
        "enabled": true,
        "path": "/24b4b1e1-7a89-45f6-858c-242cf53b5bdb-trojan",
        "host": "xxx.herokuapp.com"
    }
}
```
</details>

<details>
<summary>Shadowsocks</summary>

```bash
* Client download：https://github.com/shadowsocks/shadowsocks-windows/releases/
* Server address: xxx.herokuapp.com
* Port: 443
* Password：24b4b1e1-7a89-45f6-858c-242cf53b5bdb
* Encryption：chacha20-ietf-poly1305
* Plug-in：xray-plugin_windows_amd64.exe  //You need to download and unzip the plugin - https://github.com/shadowsocks/xray-plugin/releases and place it in the same directory
* Plugin options: tls; host= xxx.herokuapp.com; path= /24b4b1e1-7a89-45f6-858c-242cf53b5bdb-ss // (/custom UUID-ss)
```
</details>



