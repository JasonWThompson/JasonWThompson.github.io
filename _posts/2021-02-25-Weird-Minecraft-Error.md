Because I found this nowhere else on the Internet... If you attempt to load up Oculus Minecraft and it gives you the following error

```
minecraft://Mode?Oculus=true

File system error (-2147219196)
```

Then the way you fix it is by modifying some settings in the registry. First go to the following registry path:

```
Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Khronos\OpenXR\1
```

Then rename the `ActiveRuntime` key to `ActiveRuntime_backup`. Why? Because it might be important later on. Mine was set to some stort of steam path.

Now add a new "String Value" by right clicking in the blank area of the registry, clicking `New`, and then click on `String Value`. Set the `Name` to `ActiveRuntime`. Set the value to `C:\Program Files\Oculus\Support\oculus-runtime\oculus_openxr_64.json`. If Oculus is installed somewhere else, this file might be elsewhere.

Now the game should work!
