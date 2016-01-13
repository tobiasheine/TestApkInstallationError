# TestApkInstallationError
Example project to reproduce a bug while installing a test apk on a specific device

To reproduce run 
```
./gradlew connectedAndroidTest
```

Expected Error
```
Unable to install /Users/tobi/Documents/dev/repos/TestApkInstallationError/app/build/outputs/apk/app-debug.apk
com.android.ddmlib.InstallException: Unable to upload some APKs
	at com.android.ddmlib.Device.installPackages(Device.java:956)
	at com.android.builder.testing.ConnectedDevice.installPackages(ConnectedDevice.java:113)
	at com.android.builder.internal.testing.SimpleTestCallable.call(SimpleTestCallable.java:121)
	at com.android.builder.internal.testing.SimpleTestCallable.call(SimpleTestCallable.java:48)
	at java.util.concurrent.FutureTask.run(FutureTask.java:262)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:471)
	at java.util.concurrent.FutureTask.run(FutureTask.java:262)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1145)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:615)
	at java.lang.Thread.run(Thread.java:745)

com.android.builder.testing.ConnectedDevice > runTests[P17AA - 5.1] FAILED 
	com.android.builder.testing.api.DeviceException: com.android.ddmlib.InstallException: Unable to upload some APKs
		at com.android.builder.testing.ConnectedDevice.installPackages(ConnectedDevice.java:117)
null
com.android.builder.testing.api.DeviceException: com.android.ddmlib.InstallException: Unable to upload some APKs
	at com.android.builder.testing.ConnectedDevice.installPackages(ConnectedDevice.java:117)
	at com.android.builder.internal.testing.SimpleTestCallable.call(SimpleTestCallable.java:121)
	at com.android.builder.internal.testing.SimpleTestCallable.call(SimpleTestCallable.java:48)
	at java.util.concurrent.FutureTask.run(FutureTask.java:262)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:471)
	at java.util.concurrent.FutureTask.run(FutureTask.java:262)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1145)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:615)
	at java.lang.Thread.run(Thread.java:745)
Caused by: com.android.ddmlib.InstallException: Unable to upload some APKs
	at com.android.ddmlib.Device.installPackages(Device.java:956)
	at com.android.builder.testing.ConnectedDevice.installPackages(ConnectedDevice.java:113)
	... 8 more
:app:connectedDebugAndroidTest FAILED
```
