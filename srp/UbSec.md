# 扫描报告
## 实例信息获取
### 主机名：shengdans-MacBook-Air.local
### 实例IP：192.168.8.113
### 系统版本：Darwin-18.6.0-x86_64-i386-64bit
### 扫描时间：2019-06-05 15:13:56

## 检测系统初始化扫描

 [1]alias检查                          [ OK  ]

## 开始文件类安全扫描

 [1]系统重要文件hash对比               [ OK  ]

  [2]系统可执行文件安全扫描            [ OK  ]

  [3]系统临时目录安全扫描              [ OK  ]

  [4]各用户目录安全扫描                [ OK  ]

  [5]可疑隐藏文件扫描                  [ OK  ]

## 开始主机历史操作类安全扫描
  [1]所有历史操作的可疑记录             [ OK  ]

## 开始进程类安全扫描

 [1]CUP和内存类异常进程排查            [ OK  ]

 [2]隐藏进程安全扫描                   [ OK  ]

 [3]反弹shell类进程扫描                [ OK  ]

 [4]恶意进程信息安全扫描               [ OK  ]

 [5]exe程序安全扫描                    [ OK  ]

### 开始网络链接类安全扫描

 [1]当前网络对外连接扫描               [ OK  ]

 [2]恶意特征类链接扫描                 [ OK  ]
 [3]网卡混杂模式扫描                    [ 警告  ]
------------------------------
## 网络链接类安全检测
{"进程PID": "", "手工排查确认": "ifconfig | grep PROMISC | grep RUNNING", "异常时间": "", "异常文件": "", "风险名称": "网卡混杂模式检测", "处理方案": "ifconfig eth0 -promisc #关闭网卡混杂模式", "异常信息": "网卡开启混杂模式", "检测项": "## 网络链接类安全检测", "风险级别": "可疑", "所属用户": ""}
## 开始后门类安全扫描

 [1]LD_PRELOAD 后门检测                [ OK  ]

  [2]LD_AOUT_PRELOAD 后门检测          [ OK  ]

  [3]LD_ELF_PRELOAD 后门检测           [ OK  ]

  [4]LD_LIBRARY_PATH 后门检测          [ OK  ]

  [5]ld.so.preload 后门检测            [ OK  ]

  [6]PROMPT_COMMAND 后门检测           [ OK  ]

  [7]cron定时任务后门检测              [ OK  ]

  [8]未知环境变量 后门检测             [ OK  ]

  [9]ssh 后门检测                      [ OK  ]

  [10]SSH wrapper 后门检测             [ OK  ]

  [11]inetd.conf 后门检测              [ OK  ]

  [12]xinetd.conf 后门检测             [ OK  ]

  [13]setuid 后门检测                  [ 警告  ]

  [14]系统启动项后门检测               [ OK  ]
------------------------------
常规后门检测
{"进程PID": "", "手工排查确认": "[1]ls -l /System/Library/CoreServices/RemoteManagement/ARDAgent.app/Contents/MacOS/ARDAgent", "异常时间": "2019-05-04 13:28:56", "异常文件": "/System/Library/CoreServices/RemoteManagement/ARDAgent.app/Contents/MacOS/ARDAgent", "风险名称": "setuid 后门", "处理方案": "chmod u-s /System/Library/CoreServices/RemoteManagement/ARDAgent.app/Contents/MacOS/ARDAgent #去掉setuid曲线", "异常信息": "文件/System/Library/CoreServices/RemoteManagement/ARDAgent.app/Contents/MacOS/ARDAgent 被设置setuid属性，通常此类被设置权限的文件执行后会给予普通用户root权限", "检测项": "常规后门检测", "风险级别": "风险", "所属用户": "root"}

## 开始账户类安全扫描

 [1]root权限账户安全扫描               [ OK  ]

 [2]空口令账户安全扫描                 [ OK  ]

 [3]sudoers权限安全扫描                [ OK  ]

 [4]账户免密码证书安全扫描             [ OK  ]

 [5]账户密码文件扫描                   [ OK  ]

## 开始日志类安全扫描

 [1]secure日志安全扫描                 [ OK  ]

 [2]wtmp日志日志安全扫描               [ OK  ]

 [3]utmp日志日志安全扫描               [ OK  ]

 [4]lastlog日志日志安全扫描            [ OK  ]

## 开始配置类安全扫描

 [1]DNS设置扫描                        [ 警告  ]

 [2]防火墙设置扫描                     [ OK  ]

 [3]hosts设置扫描                      [ OK  ]
------------------------------
配置类安全检测
{"进程PID": "", "手工排查确认": "[1]cat /etc/resolv.conf", "异常时间": "2019-06-04 08:41:46", "异常文件": "/etc/resolv.conf", "风险名称": "DNS安全配置", "处理方案": "vi /etc/resolv.conf #删除或者更改DNS境外配置", "异常信息": "DNS设置为境外IP: 114.114.114.114", "检测项": "配置类安全检测", "风险级别": "可疑", "所属用户": "root"}
{"进程PID": "", "手工排查确认": "[1]cat /etc/resolv.conf", "异常时间": "2019-06-04 08:41:46", "异常文件": "/etc/resolv.conf", "风险名称": "DNS安全配置", "处理方案": "vi /etc/resolv.conf #删除或者更改DNS境外配置", "异常信息": "DNS设置为境外IP: 180.76.76.76", "检测项": "配置类安全检测", "风险级别": "可疑", "所属用户": "root"}

## 开始Rootkit类安全扫描

  [1]55808 Variant A                   [ OK  ]

  [2]Adore Rootkit                     [ OK  ]

  [3]AjaKit Rootkit                    [ OK  ]

  [4]aPa Kit Rootkit                   [ OK  ]

  [5]Apache Worm                       [ OK  ]

  [6]Ambient Rootkit                   [ OK  ]

  [7]Balaur Rootkit                    [ OK  ]

  [8]Beastkit Rootkit                  [ OK  ]

  [9]beX2 Rootkit                      [ OK  ]

  [10]BOBkit Rootkit                   [ OK  ]

  [11]OSX Boonana-A Trojan             [ OK  ]

  [12]cb Rootkit                       [ OK  ]

  [13]CiNIK Worm                       [ OK  ]

  [14]CX Rootkit                       [ OK  ]

  [15]Abuse Kit                        [ OK  ]

  [16]Devil Rootkit                    [ OK  ]

  [17]Diamorphine LKM                  [ OK  ]

  [18]Dica-Kit Rootkit                 [ OK  ]

  [19]Dreams Rootkit                   [ OK  ]

  [20]Duarawkz Rootkit                 [ OK  ]

  [21]Ebury sshd backdoor              [ OK  ]

  [22]ENYE LKM                         [ OK  ]

  [23]Flea Rootkit                     [ OK  ]

  [24]FreeBSD Rootkit                  [ OK  ]

  [25]Fu Rootkit                       [ OK  ]

  [26]Fuckit Rootkit                   [ OK  ]

  [27]GasKit Rootkit                   [ OK  ]

  [28]Heroin LKM                       [ OK  ]

  [29]HjC Kit Rootkit                  [ OK  ]

  [30]ignoKit Rootkit                  [ OK  ]

  [31]iLLogiC Rootkit                  [ OK  ]

  [32]OSX Inqtana Variant A            [ OK  ]

  [33]OSX Inqtana Variant B            [ OK  ]

  [34]OSX Inqtana Variant C            [ OK  ]

  [35]IntoXonia-NG Rootkit             [ OK  ]

  [36]Irix Rootkit                     [ OK  ]

  [37]Jynx Rootkit                     [ OK  ]

  [38]Jynx2 Rootkit                    [ OK  ]

  [39]KBeast Rootkit                   [ OK  ]

  [40]OSX Keydnap backdoor             [ OK  ]

  [41]Kitko Rootkit                    [ OK  ]

  [42]Knark Rootkit                    [ OK  ]

  [43]OSX Komplex Trojan               [ OK  ]

  [44]ld-linuxv rootkit                [ OK  ]

  [45]Lion Worm                        [ OK  ]

  [46]Lockit Rootkit                   [ OK  ]

  [47]Mokes backdoor                   [ OK  ]

  [48]MRK RootKit                      [ OK  ]

  [49]Mood-NT Rootkit                  [ OK  ]

  [50]Ni0 Rootkit                      [ OK  ]

  [51]Ohhara Rootkit                   [ OK  ]

  [52]Optic Kit Rootkit                [ OK  ]

  [53]OSXRK                            [ OK  ]

  [54]Oz Rootkit                       [ OK  ]

  [55]Phalanx Rootkit                  [ OK  ]

  [56]Phalanx2 Rootkit                 [ OK  ]

  [57]Portacelo Rootkit                [ OK  ]

  [58]OSX Proton backdoor              [ OK  ]

  [59]R3dstorm Toolkit                 [ OK  ]

  [60]RH-Sharpe Rootkit                [ OK  ]

  [61]RSHA Rootkit                     [ OK  ]

  [62]Shutdown Rootkit                 [ OK  ]

  [63]Scalper Worm                     [ OK  ]

  [64]SHV4 Rootkit                     [ OK  ]

  [65]SHV5 Rootkit                     [ OK  ]

  [66]Sin Rootkit                      [ OK  ]

  [67]Slapper Worm                     [ OK  ]

  [68]Sneakin Rootkit                  [ OK  ]

  [69]Solaris Wanuk backdoor           [ OK  ]

  [70]Solaris Wanuk Worm               [ OK  ]

  [71]Spanish Rootkit                  [ OK  ]

  [72]Suckit Rootkit                   [ OK  ]

  [73]NSDAP Rootkit                    [ OK  ]

  [74]SunOS Rootkit                    [ OK  ]

  [75]Superkit Rootkit                 [ OK  ]

  [76]TBD(Telnet Backdoor)             [ OK  ]

  [77]TeLeKiT Rootkit                  [ OK  ]

  [78]OSX Togroot Rootkit              [ OK  ]

  [79]T0rn Rootkit                     [ OK  ]

  [80]trNkit Rootkit                   [ OK  ]

  [81]Trojanit Kit Rootkit             [ OK  ]

  [82]Turtle Rootkit                   [ OK  ]

  [83]Tuxtendo Rootkit                 [ OK  ]

  [84]Universal Rootkit                [ OK  ]

  [85]VcKit Rootkit                    [ OK  ]

  [86]Vampire Rootkit                  [ OK  ]

  [87]Volc Rootkit                     [ OK  ]

  [88]weaponX                          [ OK  ]

  [89]Xzibit Rootkit                   [ OK  ]

  [90]X-Org SunOS Rootkit              [ OK  ]

  [91]zaRwT.KiT Rootkit                [ OK  ]

  [92]ZK Rootkit                       [ OK  ]

  [93]Miscellaneous login backdoors    [ OK  ]

  [94]Sniffer log                      [ OK  ]

  [95]Suspicious dir                   [ OK  ]

  [96]Apache backdoor                  [ OK  ]

 [97]检测LKM内核模块                   [ OK  ]
## 开始Webshell安全扫描
#### [1]Webshell安全扫描               [ 跳过  ]
------------------------------
## 根据系统分析的情况，溯源后的攻击行动轨迹为：
[2][风险] 黑客在2019-05-04 13:28:56时间，进行了setuid 后门植入,文件/System/Library/CoreServices/RemoteManagement/ARDAgent.app/Contents/MacOS/ARDAgent 被设置setuid属性，通常此类被设置权限的文件执行后会给予普通用户root权限
