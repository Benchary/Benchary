<h2 align="center">👋 嗨 我是 Benchary</h2>
  
### 😎 关于我:

- 🔭 专业学科：计算机网络
- 💼 工作岗位：系统运维
  
### 😀 兴趣

- 💻 Wireshark/tcpdump 分析网络包
- 👨‍💻 裁剪知识库，仅掌握有价值的知识
- 💪 徒手健身

以下是我整理的的一个网络故障分析模板，具备以下功能

- 快速定位网络问题的前提，首先需要确定故障范围，对于企业网络环境，可以参考以下框架快速分析网络问题 。   
- 此框架结合了 **OSI 参考模型** 及 **TCP/IP 协议堆栈** 部分重要内容  ，应用层协议太多了，DHCP\iSCSI\FTP 等等，所以只列举了以下两个日常工作生活都会涉及的互联网协议 HTTP 及 DNS。  
- 框架中只罗列了常用的 **Windows 终端网络分析工具** ，当无法登录目标设备的情况下，可在本地终端使用这些工具快速分析网络问题

当 Client(电脑) 发起对 Server 服务的请求，期间发生任何网络问题都可以参考以下框架进行快速故障分析

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
        <td rowspan="3">应用层</td>
        <td>TLS</td>
        <td rowspan="2" colspan="2" align="center">Nginx / Apache</td> 
        <td rowspan="10" colspan="1" align="center">Server</td> 
        <td rowspan="2" colspan="2" align="center">Browser</td>
        <td rowspan="2" colspan="2" align="center">Fiddler</td>
        <td rowspan="2" colspan="1" align="center">curl</td>
        <td rowspan="8" colspan="1" align="center">Wireshark
            (tcpdump)</td> 
        <td rowspan="10" colspan="1" align="center">PC</td> 
    </tr>
    <tr>
        <td>HTTP</td>
      </tr>
      <tr> 
        <td>DNS</td>
          <td colspan="2" align="center">Bind</td>
          <td rowspan="1" colspan="5" align="center">Nslookup</td> 
        </tr>   
    <tr>
        <td rowspan="2">传输层</td>
        <td>TCP</td>
        <td colspan="1" align="center">80 </td>
        <td colspan="1" align="center">443 </td>
        <td rowspan="7" align="center">Firewall</td>
        <td rowspan="2" align="center">Netcat</td>
        <td rowspan="2" align="center">Netstat</td>
        <td rowspan="2" align="center">Telnet</td>
        <td rowspan="5" align="center">Nmap</td> 
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


















