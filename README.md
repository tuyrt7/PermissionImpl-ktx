# PermissionImpl
动态权限申请库kotlin版本，根据郭霖第三行代码修改，初版测试通过

### 后续会结合之前版本库进行完善功能

## 加入项目：

gradle依赖

```
// 根目录 gradle
repositories {
    ...
    maven { url 'https://jitpack.io' }
}

// 模块 gradle
dependencies {
	implementation 'com.tuyrt.permission:permissionimpl-ktx:1.0.0'
}

```

## 使用方式

```
  PermissionImpl.request(this, Manifest.permission.CALL_PHONE) { allGranted, deniedList ->
      if (allGranted) {
          call()
      } else {
          Toast.makeText(this,"You denied ${deniedList}",Toast.LENGTH_SHORT).show()
      }
  }
```

##### 有问题，可以提交issue交流。