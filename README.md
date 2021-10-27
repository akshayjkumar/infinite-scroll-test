# Infinite Scroll Test

Shell script using ADB to test infinite scrolling of RecyclerView in Android.

```
echo "Infinite Scroller\n"
CMD_SCROLL_DOWN="adb shell input touchscreen swipe 1 1080 1 0 20"
SCROLL=0
while [ true ]
do
    let "SCROLL+=1"
    echo "Scrolling $SCROLL..."
    eval $CMD_SCROLL_DOWN
    # Uncomment below to wait for the scroll to settle (if required)
    sleep 0.4 
done
```

## Run the script
* Save the above to code with `.sh` extension
* Connect a device/ an emulator
* Open Terminal and run 
```
sh scroll.sh
```

https://user-images.githubusercontent.com/16755620/139049383-a5f19efe-53b2-41da-bb96-8a10c1860b18.mp4

## Read
To know about the above adb command https://github.com/akshayjkumar/adb-shell-cmds#adb-inputs
