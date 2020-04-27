# XPermission
#简单好用的Android权限申请库

# 添加方式

```
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
```
```
  dependencies {
	        implementation 'com.github.qingqingziyu:XPermission:Tag'
	}
```

# 使用方法

```
  XPermission.request(
                this,
                Manifest.permission.CALL_PHONE
            ) { b, list ->
                if (b) {//申请通过
                    call()
                } else {
                    Toast.makeText(this, "你未通过申请 $list", Toast.LENGTH_LONG).show()
                }
            }
```
