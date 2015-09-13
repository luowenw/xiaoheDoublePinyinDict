# xiaoheDoublePinyinDict
This project is aimed for xiaohe-pinyin which is a Chinese input method. I suppose this project only could be helpful to you if you can read Chinese.

## 如果你用没越狱的iPhone，用小鹤双拼，用百度拼音输入法：
如果你想用鹤形，那么你需要把鹤形的自定义短语挂接到手机百度输入法中。  
截至目前，我在Mac、PC版本的百度输入法上，都没能把自定义短语通过百度账号同步到手机百度输入法中。2015.09.13  
后来发现百度手机输入法可以把自定义短语何用户词存在iCloud上面，所以可以直接改。  
### 文件说明
iclouldCache/phrase.hexing 这个文件里面是鹤形的挂接码，已经转成相应格式  
iclouldCache/Ue3.top5k 这个文件里面是词频最高的5000个英文单词，来自http://www.wordfrequency.info
### 如果你用Mac
如果你手机和Mac的iCloud都设置好了，那么把这两个文件拼接上去就可以了：
* 首先，在手机百度输入法-》输入设置-》词库设置里面，关闭iCloud云同步选项  
* 然后，打开一个terminal:
```shell
cat ~/Downloads/xiaoheDoublePinyinDict-master/icloudCache/phrase.hexing >> \
~/Library/Mobile\ Documents/iCloud~com~baidu~baiduInput/BaiduInputMethod/phrase
cat ~/Downloads/xiaoheDoublePinyinDict-master/icloudCache/Ue3.top5k >> \
~/Library/Mobile\ Documents/iCloud~com~baidu~baiduInput/BaiduInputMethod/Ue3
```
* 然后等一两分钟，这两个文件应该就同步到iCloud上了  
* 最后在手机上打开iCloud云同步选项  
试一试aaod是不是可以打出「腌」在第一个候选位置。  
### 如果你用Windows
如果Windows也可以配置iCloud的话，照Mac的道理做一遍应该也可以，没试过
