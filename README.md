![Logo](art/autosize_banner.jpg)

<p align="center">
   <a href="https://bintray.com/jessyancoding/maven/autosize/_latestVersion">
    <img src="https://img.shields.io/badge/Jcenter-v0.7.0-brightgreen.svg?style=flat-square" alt="Latest Stable Version" />
  </a>
  <a href="https://travis-ci.org/JessYanCoding/AndroidAutoSize">
    <img src="https://travis-ci.org/JessYanCoding/AndroidAutoSize.svg?branch=master" alt="Build Status" />
  </a>
  <a href="https://developer.android.com/about/versions/android-4.0.html">
    <img src="https://img.shields.io/badge/API-14%2B-blue.svg?style=flat-square" alt="Min Sdk Version" />
  </a>
  <a href="http://www.apache.org/licenses/LICENSE-2.0">
    <img src="http://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square" alt="License" />
  </a>
  <a href="https://www.jianshu.com/u/1d0c0bc634db">
    <img src="https://img.shields.io/badge/Author-JessYan-orange.svg?style=flat-square" alt="Author" />
  </a>
  <a href="https://shang.qq.com/wpa/qunwpa?idkey=1a5dc5e9b2e40a780522f46877ba243eeb64405d42398643d544d3eec6624917">
    <img src="https://img.shields.io/badge/QQ群-301733278-orange.svg?style=flat-square" alt="QQ Group" />
  </a>
</p>


## A low-cost Android screen adaptation solution (今日头条屏幕适配方案终极版，一个极低成本的 Android 屏幕适配方案).

[中文说明](README-zh.md)

## Overview
### Pixel 2 XL | 1440 x 2880 | 560dpi:
<p>
   <img src="art/1440x2880_width.png" width="30%" height="30%">
   <img src="art/1440x2880_height.png" width="30%" height="30%">
   <img src="art/1440x2880_external.png" width="30%" height="30%">
</p>

### Pixel XL | 1440 x 2560 | 560dpi:
<p>
   <img src="art/1440x2560_width.png" width="30%" height="30%">
   <img src="art/1440x2560_height.png" width="30%" height="30%">
   <img src="art/1440x2560_external.png" width="30%" height="30%">
</p>

### Nexus 5X | 1080 x 1920 | 420dpi:
<p>
   <img src="art/1080x1920_width.png" width="30%" height="30%">
   <img src="art/1080x1920_height.png" width="30%" height="30%">
   <img src="art/1080x1920_external.png" width="30%" height="30%">
</p>

### Nexus 4 | 768 x 1280 | 320dpi:
<p>
   <img src="art/768x1280_width.png" width="30%" height="30%">
   <img src="art/768x1280_height.png" width="30%" height="30%">
   <img src="art/768x1280_external.png" width="30%" height="30%">
</p>

### Nexus S | 480 x 800 | 240dpi:
<p>
   <img src="art/480x800_width.png" width="30%" height="30%">
   <img src="art/480x800_height.png" width="30%" height="30%">
   <img src="art/480x800_external.png" width="30%" height="30%">
</p>

## Notice
[Devices Info](https://material.io/tools/devices/)

[Analysis](https://juejin.im/post/5b7a29736fb9a019d53e7ee2)

## Download
``` gradle
 implementation 'me.jessyan:autosize:0.7.0'
```

## Usage (just one steps)
### Step 1 
* **Initialize in AndroidManifest:**
```xml
<manifest>
    <application>            
        <meta-data
            android:name="design_width_in_dp"
            android:value="360"/>
        <meta-data
            android:name="design_height_in_dp"
            android:value="640"/>           
     </application>           
</manifest>
```

## Advanced

* **Customize the adaptation parameters of the Activity:**
```java
public class CustomAdaptActivity extends AppCompatActivity implements CustomAdapt {

    @Override
    public boolean isBaseOnWidth() {
        return false;
    }

    @Override
    public float getSizeInDp() {
        return 667;
    }
}

```

* **Cancel the adaptation of the Activity:**
```java
public class CancelAdaptActivity extends AppCompatActivity implements CancelAdapt {

}

```

## ProGuard
```
 -keep class me.jessyan.autosize.** { *; }
 -keep interface me.jessyan.autosize.** { *; }
```


## Donate
![alipay](https://raw.githubusercontent.com/JessYanCoding/MVPArms/master/image/pay_alipay.jpg) ![](https://raw.githubusercontent.com/JessYanCoding/MVPArms/master/image/pay_wxpay.jpg)

## About Me
* **Email**: <jess.yan.effort@gmail.com>
* **Home**: <http://jessyan.me>
* **掘金**: <https://gold.xitu.io/user/57a9dbd9165abd0061714613>
* **简书**: <http://www.jianshu.com/u/1d0c0bc634db>

## License
```
 Copyright 2018, jessyan

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
