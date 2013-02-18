iOS_command_compile
===================

iOS命令行编译相关

环境
----
Mac OSX 10.8.2
Xcode Version 4.6 (4H127)

1、命令行编译
=============

命令
----

xcodebuild -target Yourapp clean

xcodebuild -target PROVISIONING_PROFILE="your_mobile_provision_file_name" CODE_SIGN_IDENTITY="your_identity"

xcrun -sdk iphoneos PackageApplication -v build/Release-iphoneos/your_app.app -o /your/file/path/

以上命令就是用命令行编译的方法

细节
----

1.PROVISIONING_PROFILE 的值

    从app_store中下载回来的*.mobileprovision文件的文件名
    （需要在/Users/yourname/Library/MobileDevice/Provisioning\ Profiles/ 下,在Xcode的Organizer->Provisioning Profiles中也可以看到 ）

2.CODE_SIGN_IDENTITY 的值

    apple提供的cer文件中提供的信息，安装后，可以在system preference -> keychain access中的My Certificates tab中看到
    （Name为iPhone Distribution:your_info），这个name就是CODE_SIGN_IDENTITY的值

设定好这两个值，就可以编译和打包出可以直接上传到appstore的ipa包了

