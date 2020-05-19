# Description
A remote user can create a specially crafted M3U file, media playlist file that when loaded by the target user, will trigger a memory leak, whereby Amarok 2.8.0 continue to waste memory over time, eventually consuming all RAM resources.

# Impact
Attacker might be able to launch a DOS (denial of service) attack by crashing the application or take advantage of other unexpected program behavior resulting from a low memory condition.

# Steps Followed
1. Craft M3U media playlist file, used
