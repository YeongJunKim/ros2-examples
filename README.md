ROS 2 examples
==============

To see some of these examples in use, visit the ROS 2 Tutorials page: https://docs.ros.org/en/foxy/Tutorials.html



Notes
=====
ubuntu 20.04

Setup 은 아래 링크
https://keep-steady.tistory.com/45

공식 문서
https://docs.ros.org/en/foxy/Tutorials/Advanced/Simulators/Webots/Installation-Windows.html


To add **compile_commands.json** with colcon build 
``` bash
$ colcon build --cmake-args=-DCMAKE_EXPORT_COMPILE_COMMANDS:BOOL=ON
```


**.vscode/settings.json**
``` json
{
    "C_Cpp.default.compileCommands": "${workspaceFolder}/build/compile_commands.json",
}
```
빌드 옵션,
``` bash
$ colcon build --symlink-install # 심볼릭 파일 생성, 패키지를 수정할때 자동으로 반영된다 함
$ colcon build --packages-up-to ${PACKAGE_NAME} # 특정 패키지 + 의존성
$ colcon build --packages-select ${PACKAGE_NAME} # 특정 패키지
```

