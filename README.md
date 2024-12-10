<h2 align="center">🔎 网络诊断分析框架</h2>
  

简单易用的网络故障分析框架，具备以下功能

- 适用目标：
  - 普通用户
  - 专业用户
  - 企业用户 
- 此框架结合了 **OSI 参考模型** 及 **TCP/IP 协议堆栈** 部分重要内容  ，应用层协议太多了，DHCP\iSCSI\FTP 等等，所以只列举了以下两个日常工作生活都会涉及的互联网协议 HTTP 及 DNS。  
- 框架中只罗列了常用的 **网络分析工具** ，当无法登录目标设备的情况下，可在本地终端使用这些工具快速分析网络问题

当 Client(电脑) 发起对 Server 服务的请求，期间发生任何网络问题都可以参考以下框架进行快速诊断

<table border="1.5">
    <tr>
        <th align="center">分层</th>   <!-- 左对齐 -->
        <th align="center">协议</th> <!-- 居中对其（默认）-->
        <th colspan="2" align="center">应用/服务</th>  <!-- 右对齐-->
        <th colspan="1" align="center">主机</th>  <!-- 右对齐-->
        <th colspan="7" align="center">网络设备及终端网络分析工具</th>  <!-- 右对齐-->
        <th colspan="1" align="center">终端</th>  <!-- 右对齐-->
         </tr>
    <tr>
        <td rowspan="3">应用层</td>
        <td>TLS</td>
        <td rowspan="2" colspan="2" align="center">Nginx / Apache</td> 
        <td rowspan="10" colspan="1" align="center">Server</td> 
        <td rowspan="2" colspan="6" align="center">Browser(POST/GET)</td> 
        <td rowspan="10" colspan="1" align="center">Wireshark
          Tcpdump |
          CSNAS
          (Microsoft Network Monitor) 
          </td> 
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


















