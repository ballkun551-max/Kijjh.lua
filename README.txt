BALLKUN RIDER FARM DATA COLLECTOR v0.2.8
===========================================

Added:
- Script Activity Monitor module (24_script_activity_metadata.txt)
- Lists client-visible Script, LocalScript, and ModuleScript metadata:
  name, class, path, Enabled/Disabled, RunContext, and discovery source.
- Checks getscripts() and getloadedmodules() when supported.

Important limitations:
- This module does NOT extract source code from third-party executor payloads.
- Scripts executed directly by an executor may not exist as Roblox Instances
  and therefore may not appear in this report.
- Roblox source access protections are not bypassed.
- For source analysis, use code you own or are authorized to inspect.

Usage:
1. Upload the .lua file to the root of your GitHub repository.
2. Run it in an authorized test experience.
3. Enable "Script Activity Monitor (ชื่อ/Path เท่านั้น)" in the UI.
4. Press START/SNAPSHOT.
5. Find 24_script_activity_metadata.txt in the output folder.


v0.2.8 changes:
- Output folder is BALL_KUN_Dump/<map>_<PlaceId>/ under the executor file workspace (writefile/makefolder support required).
- Logs and on-screen notifications report each successfully saved dump file, failed items, and a final count.
