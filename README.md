> 应用退出前台自动生成coverage.ec文件

##  使用jacoco gradle插件生成报告
将coverage.ec文件拷贝到app/build/outputs/code-coverage/connected目录下
```
adb pull /sdcard/jacoco/coverage.ec `pwd`/app/build/outputs/code-coverage/connected/
```

```
gradle jacocoTestReport
```
报告的存放目录为项目根目录下的 build/reports/jacoco/jacocoTestReport目录下


## 使用macaca工具生成覆盖率报告
```
macaca coverage -r java -f `pwd`/new.ec -c `pwd`/app/build/intermediates/classes/debug -s `pwd`/app/src/main/java --html `pwd`/reporter
```