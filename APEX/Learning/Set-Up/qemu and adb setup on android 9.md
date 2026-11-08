
cd ~/android9
./up.sh      # boots and waits for adb; don't run it while a guest is already running (it kills it first)
./down.sh    # stops the guest

adb -s 127.0.0.1:5555 root          # userdebug build; adbd restarts as root, then reconnect
adb connect 127.0.0.1:5555
adb -s 127.0.0.1:5555 shell id

#before-shutting-down-the-lp
adb -s 127.0.0.1:5555 shell sync; ./down.sh
#to-run- 
cd ~/android9
./up.sh
adb -s 127.0.0.1:5555 root; sleep 2; adb connect 127.0.0.1:5555