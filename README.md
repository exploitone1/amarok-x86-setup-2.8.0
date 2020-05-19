# Description
A remote user can create a specially crafted M3U file, media playlist file that when loaded by the target user, will trigger a memory leak, whereby Amarok 2.8.0 continue to waste memory over time, eventually consuming all RAM resources.

# Impact
Attacker might be able to launch a DOS (denial of service) attack by crashing the application or take advantage of other unexpected program behavior resulting from a low memory condition.

# Steps Followed
1. Craft M3U media playlist file, used -> https://github.com/exploitone1/amarok-x86-setup-2.8.0/blob/master/test_big.m3u
2. Open Amarok -> Play Media, and select crafted m3u file.
3. Application start hogging processor to 100%.

![](images/Screen%20Shot%202020-05-15%20at%206.02.09%20PM.png)

4. PID is attched to WinDbg.

![](images/Screen%20Shot%202020-05-15%20at%206.02.14%20PM.png)

