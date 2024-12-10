<h2 align="center">🔎 互联网诊断分析技术框架</h2>

 ### 使用说明 
- 适用用户：🙍‍♂️普通用户 | 👨‍💻专业用户 | 👨‍💼企业用户
- 适用场景：
  - 🏡家庭网络
  - 🏦企业网络
  - 🌏互联网
- 作用：快速诊断网络故障
- 注意： 本框架沿用**OSI 参考模型** 及 **TCP/IP 协议堆栈** 部分重要内容  

<table border="1.5">
    <tr>
        <th align="center">分层</th>   <!-- 左对齐 -->
        <th align="center">协议</th> <!-- 居中对其（默认）-->
        <th colspan="2" align="center">应用/服务</th>  <!-- 右对齐-->
        <th colspan="1" align="center">主机</th>  <!-- 右对齐-->
        <th colspan="6" align="center">网络设备及终端网络分析工具</th>  <!-- 右对齐-->
        <th colspan="1" align="center">终端</th>  <!-- 右对齐-->
         </tr>
    <tr>
        <td rowspan="2">应用层</td>
        <td>HTTPS</td>
        <td rowspan="1" colspan="2" align="center">Nging
         Apache</td> 
        <td rowspan="10" colspan="1" align="center">Server</td> 
        <td rowspan="1" colspan="5" align="center">Browser (POST/GET)</td>
        <td rowspan="8" colspan="1" align="center">Wireshark
            (Tcpdump)</td> 
        <td rowspan="10" colspan="1" align="center">PC</td> 
    </tr>
      <tr> 
        <td>DNS</td>
          <td colspan="2" align="center">Bind</td>
          <td rowspan="1" colspan="5" align="center">Nslookup</td> 
        </tr>   
    <tr>
        <td rowspan="3">传输层</td>
        <td colspan="1">TLS</td>
        <td rowspan="2" colspan="2" align="center">443</td>
        <td rowspan="8" align="center">Firewall</td>
        <td rowspan="3" align="center">Netcat</td>
        <td rowspan="3" align="center">Netstat</td>
        <td rowspan="3" align="center">Telnet</td>
        <td rowspan="6" align="center">Nmap</td> 
    </tr>
      <tr>
        <td>TCP</td>     
    </tr>
    <tr>
        <td>UDP</td>
        <td colspan="2" align="center">53</td>
         </tr>
    <tr>
        <td rowspan="3">网络层</td>
        <td>IP</td>
        <td rowspan="2" colspan="1" align="center">LAN Router</td>
        <td rowspan="3" colspan="1" align="center"> WAN</td> 
        <td rowspan="5" align="center">Router
            (Wi-Fi Router)</td>
        <td rowspan="5" align="center">L3 Switch</td>
        <td rowspan="1" align="center">ping</td>
    </tr>
    <tr>
    <td>ICMP</td>
    <td rowspan="1" align="center">tracert</td>
     </tr>
    <tr>
    <td>ARP</td>
    <td rowspan="1" colspan="1" align="center">LAN</td>
    <td rowspan="1" colspan="1" align="center">arp</td>
      </tr>
    <tr>
        <td rowspan="2">链路层</td>
        <td>Ethernet</td>
        <td rowspan="1" colspan="2" align="center">LAN</td>
        <td rowspan="2" align="center">L2 Switch
            (AP)
        </td>
        <td rowspan="2" colspan="2" align="center">Bridge
            (Wireless Bridge)
        </td>
           </tr>
     <tr>
        <td>Wi-Fi</td>
        <td rowspan="1" colspan="2" align="center">WLAN</td>
           </tr>
    <tr>
        <td rowspan="1">系统层</td>
        <td rowspan="1" colspan="3" align="center">OS/Firmware</td>
        <td colspan="3" align="center">CPU</td>
        <td colspan="3" align="center">Mem</td>
        <td colspan="3" align="center">Disk</td>
            </tr>
    <tr>
  <td rowspan="1">硬件层</td>
        <td rowspan="1" colspan="3" align="center">Network Adapter </td>
        <td colspan="3" align="center">NIC </td>
        <td colspan="3" align="center">RJ-45 </td>
        <td colspan="3" align="center">SFP </td>
    </tr>
  <td rowspan="1">电源</td>   
  <td colspan="12" align="center">ON / OFF (能源很重要⭐)</td>
</table>




遇到疑难杂症，多从系统中捕获的日志进行溯源分析，无论是网络、操作系统、应用程序都会生成日志信息，无法生成日志的技术产品注定是失败的！


















