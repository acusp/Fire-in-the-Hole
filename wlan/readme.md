
漏洞分析：https://pleasestopnamingvulnerabilities.com/

POC来源：https://github.com/ScottyBauer/Android_Kernel_CVE_POCs/tree/master/wifi


## 编译

```
make
```


## 网卡设置


运行 POC 之前需要将无线网卡设置为 moniter 模式：
```
sudo ifconfig <interface> down
sudo iwconfig <interface> mode moniter
sudo ifconfig <interface> up
```
其中 `<interface>` 代表网卡接口名称，如：wlan0


## 运行POC

```
sudo ./11013 -i <interface> <ssid>
```
其中 `<ssid>` 为设置的AP名称
