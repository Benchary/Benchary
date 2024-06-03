<h2 align="center">👋 嗨 我是卞辰阳 | Benchary</h2>
<p align="center">
  🌐<a href="https://kaokit.com/">技术指南</a> | 
  😀<a href="https://github.com/Benchary">GitHub</a> 
</p>
  
<!--
**beercrab/beercrab** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
-->

### 😀 关于我:

- 🔭 专业计算机网络技术
- 💼 我目前从事计算机系统运维


### 🧰 专业技能

- 🌐 构建基于 TCP/IP 网络堆栈的基础设施服务
- 🔎 擅长分析数据包进行 L2-L7 的网络故障排除
- ☁️ 公(私)云服务的落地实践

根据个人对网络基础概念的理解，我建立了针对 IPv4 的 6 层网络故障排除模型，每层对应的 TCP/IP 堆栈协议

> (OSPF/BGP) 属于单独的 TPC/IP 动态路由协议暂未详细说明，因为这两个协议本身不属于 TCP/IP 核心堆栈，主要是用于动态管理路由选路的协议

```
+-------------+
| Application | ---Protocol--- [HTTP、FTP、TLS...]
+-------------+
| Transport   | ---Protocol--- [TCP]
+-------------+
| Internet    | ---Protocol--- [IP、ICMP]
+-------------+
| Mapping     | ---Protocol--- [ARP]
+-------------+ 
| Link        | ---Protocol--- [Ethernet II、802.3 、 802.11(WLAN)、802.1q] 
+-------------+
| Interface   | ---Protocol--- [网线、光纤、电磁波、网卡]
+-------------+                            
```























