下载ipa，在局域网部署http服务器：
python -m SimpleHTTPServer 9090

http://192.168.0.102:9090/1.ipa

因为强制https，所以在github上传一个plist如：
```
https://github.com/v5est0r/TIPS/blob/master/test.plist
```
修改11行ipa地址。
点击raw得到地址：
```
https://raw.githubusercontent.com/v5est0r/TIPS/master/test.plist
```
Safari打开如下地址即可：
```
itms-services://?action=download-manifest&url=https://raw.githubusercontent.com/v5est0r/TIPS/master/test.plist
```
