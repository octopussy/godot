Requirements:
scons 3.0.1 (pip install scons==3.0.1)

1. vcproj gen:
scons p=windows vsproj=yes

2. android package:
scons platform=android target=release android_arch=armv7
scons platform=android target=release android_arch=arm64v8
scons platform=android target=release_debug android_arch=armv7
scons platform=android target=release_debug android_arch=arm64v8
cd platform/android/java
.\gradlew build

3. add to project.godot:
[android]
modules="org/godotengine/godot/GodotAdMob"
