> Ref:
https://pleasestopnamingvulnerabilities.com/
https://github.com/ScottyBauer/Android_Kernel_CVE_POCs/tree/master/wifi

## CVE 列表

> https://source.android.com/security/bulletin/2017-11-01#qualcomm-components

| CVE            | References                  | **Type**   | **Severity** | **Component** |
| ----------     | ----------                  | ---------- | ----------   | ----------    |
| CVE-2017-11013 | A-64453535,QC-CR#2058261[2] | RCE        | Critical     | WLAN          |
| CVE-2017-11015 | A-64438728,QC-CR#2060959[2] | RCE        | Critical     | WLAN          |
| CVE-2017-11014 | A-64438727,QC-CR#2060959    | RCE        | Critical     | WLAN          |

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
