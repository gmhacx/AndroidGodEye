# CHANGELOG

## 3.2.1

### Changed

- Add release notes to github release
- Change gradle script and repository url
- Readme
- Debug dashboard Thread add thread group
- View canary ui change(always show border)
- Thread module output threadInfo instead of Thread
- Thread module replace threadRunningProcess to threadTag
- Cpu/Fps/Heap/Pss/Ram/ThreadDump/Traffic will output last info when event send before being observed
- add return value to module install method, return true if install success.
- Module config remove application, use GodEye.instance().getApplication()
- Block module change function name:addBlockInterceptor -> setBlockListener

### Added

- Unit test
- Thread module add config ThreadTagger to tag for thread
- Unit test
- Unit test
- Add Unit test

### Deprecated

- GodEyeMonitor.setClassPrefixOfAppProcess
- GodEyeMonitor.setThreadRunningProcessClassifier

### Removed

- remove some function in ReflectUtil class
- IoUtil\GsonUtil\GsonSerializer

### Fixed

- Build error
- Unit test failed
- Crash failed unit test


## 3.2.0

### Added

- Block module config can be cached when change in debug monitor dashboard
- Add some unitTests
- Add unit test coverage

### Deprecated

- GodEyeHelper.inspectView, you do not need to call this function

### Changed

- ViewCanary: auto detect view issue, overdraw and depth
- ImageCanary: change detect time
- Modules config class path changed, eg. GodEyeConfig.AppSizeConfig -> cn.hikyson.godeye.core.internal.modules.appsize.AppSizeConfig
- Debug monitor dashboard's layout has been slightly adjusted, pageload has its own row
- Add attention note text to Android Studio plugin

### Removed

- Module config classes named xxxContext have been removed, just use xxxConfig, eg. AppSizeContext has been removed and just use AppSizeConfig instead
- Remove some unused util class:DeviceUtils\FileUtil\NumberUtil\Preconditions\ShellUtil etc.

## 3.1.12

### Added

- Add ALL_MODULES field to GodEye class
- Add ChoreographerInjecor for unit test

### Fixed

- Error when Battery is shutting down if receiver is not registered

## 3.1.11

### Changed

- ImageCanary support "ImageView is visible or not"

## 3.1.10

### Changed

- Android Studio plugin and shell/bat script of AndroidGodEye updated and can auto identify ports

### Fixed

- Long text of MethodCanary's method tree display not complete
- Main thread color of MethodCanary should be black

## 3.1.9

### Fixed

- MethodCanary method tree show wrong

### Changed

- ImageCanary support preview

## 3.1.8

### Fixed

- Crash when ImageCanary install in not main thread

### Changed

- Refactor thread util

## 3.1.7

### Fixed

- GodEyeHelper.stopMethodCanaryRecording error

## 3.1.6

### Changed

- Keep imageIssue class impl serializable

## 3.1.5

### Added

- GodEyeHelper class add some helper methods:inspectView、methodCanaryStart/StopMonitor

### Changed

- Removed ImageCanary config(ImageCanaryConfigProvider):BitmapInfoAnalyzer
- ImageCanary will not be output issues which have been output before

## 3.1.4

### Added

- Image Canary

## 3.1.3

### Added

- ImageCanary

### Changed

- Migrate to androidx
- Split android-godeye-toolbox to android-godeye-okhttp and android-godeye-xcrash
- Crash output CrashInfo list instead of Map

