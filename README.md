a proof of concept about how a proper fs search engine must work on windows os.

- not privileged
- ultra fast
- low mem usage around 40mb (variable)
- uses 2 cpu cores. usually low cpu usage but at peak the 2 cores will be maxed out, 1 for gui while gui changes and 1 for search operations
- optimized for old hard disks
- is only a single exe and writes only one single xml file for normal settings
- no indexing garbage, everything is realtime
- nice filters
- settings and inputs will be saved if be correct and used successfuly
- it uses os cache so speed up after first search can be presistent after exit while same data still exist in os cache. for max benefits increase os mem cache size and ntfs mem usage in registry

download: https://github.com/void0xfffffff/mfsearch/releases

some parts are not implemented yet but the core is ready for poc. for help use mouse hovering.

currently no source code is available for you not because the code is secret only because it's simple. you can reverse engineer it anyways, is not obfuscated is not even packed.

there are some secret hotkeys:
- enter: search if no entery is selected, if some enteries are selected opens their parent dir but currently is buggy
- double click: on enteries opens their parrent dir bit currently is buggy
- escape: while searching cancels the search otherwise exits the app
- ctrl+s: saves selected entries to file, or if not selected saves all of them
- ctrl+c: copy selected enteries, or if not selected, all of them
- ctrl+r: for clearing/resetting the search results

the file type detection part uses a GPLv3 library and is not compatible with closed source or bsd, i believe that nothing is closed source bin is already source code in another language but because of GPLv3 rules i won't fix it for release, only works under debugger but is not intentional
