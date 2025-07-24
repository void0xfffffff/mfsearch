a proof of concept about how a proper fs search engine must work on windows os.

- not privileged
- ultra fast
- low mem usage (but is variable and depends on many complexities)
- uses 2 cpu cores. usually low cpu usage but at peak the 2 cores will be maxed out, 1 for gui while gui changes and 1 for search operations
- optimized for old hard disks
- is only a single exe and writes only one single xml file for its own settings
- no indexing garbages, everything is realtime
- nice filters
- settings and inputs will be saved if be correct and used successfuly
- it uses os cache so speed up after first search can be presistent after exit while same data still exist in os cache. for max benefits increase os mem cache size and ntfs mem usage in registry

download: https://github.com/void0xfffffff/mfsearch/releases

some parts are not implemented yet but the core is ready for poc. for help use mouse hovering.

performance depends on many low level details so i do not believe in benchmarks just test it yourself. this tool is optimized for old hard disks which requires single threaded sequential access and max cache optimizations which are done but the optimization quality depends on many low level hardware and software details. and i am not using usual timers and intervals so the delay behaviour is different on different hardwares and has direct effects on performance, is optimized for 2011 era hardwares, in next major versions i will think about optimizaion for all hardwares.

hotkeys:
- enter: search if no entry is selected, if some entries are selected opens their dir but currently is buggy
- double click: on entries opens their dir but currently is buggy
- escape: while searching cancels the search otherwise if entry selected deselects otherwise exits the app
- ctrl+s: saves selected entries to file, or if not selected saves all of them
- ctrl+c: copy selected entries, or if not selected, all of them
- ctrl+r: for clearing/resetting the search results

the file type detection part is currently buggy and must be replaced due to license issues.
