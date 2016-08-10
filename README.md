# AndroidDependencies
Android 常用库集

## 使用
* 在项目根节点的```build.gradle```文件开头加上一句：
```gradle
apply from: 'https://raw.githubusercontent.com/donglua/AndroidDependencies/master/dependencies.gradle'
```

* 于是，我们在子模块的依赖中就可以写成这样：
```gradle

dependencies {
  def dependencies = rootProject.ext.dependencies

  // support
  compile dependencies.supportAppCompat
  compile dependencies.supportDesign
  compile dependencies.supportRecyclerview
  compile dependencies.supportAnnotations

  // http
  compile dependencies.retrofit
  compile dependencies.retrofitGsonConverter
  compile dependencies.retrofitRxjavaAdapter
  compile dependencies.okhttp3
  compile dependencies.okhttpLoggingInterceptor

  // Rx
  compile dependencies.rxJava
  compile dependencies.rxAndroid

  // dagger
  compile dependencies.dagger
  apt dependencies.daggerCompiler
  provided dependencies.javaxAnnotation
  ...
}
```
