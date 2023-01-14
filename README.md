# Android_Gradle_DSL_7.4.0

2023-01-14

环境:

```
plugins {
    id 'com.android.application' version '7.4.0' apply false
    id 'com.android.library' version '7.4.0' apply false
    id 'org.jetbrains.kotlin.android' version '1.7.21' apply false
}

distributionUrl=https\://services.gradle.org/distributions/gradle-7.5-all.zip
```

请注意`gradle-7.5-bin.zip`是不包含源码的, 需要使用`gradle-7.5-all.zip`

# 导入源码

## 导入`Gradle源码`

```
android {
    ...

    sourceSets {
        def base = "/Users/angcyo/.gradle/wrapper/dists/gradle-7.5-all/6qsw290k5lz422uaf8jf6m7co/gradle-7.5/src"
        main.java.srcDirs += [
                "${base}/core",
                "${base}/core-api",
                "${base}/base-services",
                "${base}/base-services-groovy",
                "${base}/logging",
                "${base}/plugins",
                "${base}/diagnostics",
                "${base}/ide-native",
        ]
    }

    //输出gradle版本
    println(gradle.gradleVersion)
}
```

## 导入`AGP源码`

```
dependencies {
    ...
    
    def gradle = "/Users/angcyo/.gradle/caches/modules-2/files-2.1/com.android.tools.build/gradle/7.4.0"
    implementation fileTree(dir: gradle, include: ["*.jar", "*\\*.jar"])

    def gradleApi = "/Users/angcyo/.gradle/caches/modules-2/files-2.1/com.android.tools.build/gradle-api/7.4.0"
    implementation fileTree(dir: gradleApi, include: ["*.jar", "*\\*.jar"])
}
```

# 其他版本

[Android_Gradle_DSL_7.4.0](https://github.com/angcyo/Android_Gradle_DSL_7.4.0)

[Android_Gradle_DSL_7.2.1](https://github.com/angcyo/Android_Gradle_DSL_7.2.1)

[Android_Gradle_DSL_7.0.0](https://github.com/angcyo/Android_Gradle_DSL_7.0.0)

[Android_Gradle_DSL_4.1.0](https://github.com/angcyo/Android_Gradle_DSL_4.1.0)

[Android_Gradle_DSL_4.0.1](https://github.com/angcyo/Android_Gradle_DSL_4.0.1)

[Android_Gradle_DSL_4.0](https://github.com/angcyo/Android_Gradle_DSL_4.0)

[Android_Gradle_DSL_3.5](https://github.com/angcyo/Android_Gradle_DSL_3.5)

[Android_Gradle_DSL_3.3](https://github.com/angcyo/Android_Gradle_DSL_3.3)

[Android_Gradle_DSL_3.2](https://github.com/angcyo/Android_Gradle_DSL_3.2)