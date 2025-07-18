a proof of concept about how a proper fs search engine must work on windows os.

- not privileged
- ultra fast, does 10 minute tasks of microsoft search tool under 5 seconds and while repeated task takes another 10 minutes with microsoft tool takes under 0.1 second with this
- searchs 1tb old hdd on 2010 era hw full of little garbages and fragmentations with around 50mb ram usage and low cpu usage
- a single exe and writes only one single xml file for normal settings
- no indexing garbage everything is realtime
- nice filters
- settings and inputs will be saved if be correct and used successfuly
- it uses os cache so speed up after first search can be presistent after exit while same info still exist in os cache. for max benefits increase ntfs cache size and mem usage in registry

some parts are not implemented but the core is ready for poc. for help use mouse hovering.

currently no source code is available not because the code is secret only because it's simple. you can reverse engineer it anyways, is not obfuscated is not even packed.

there are some secret hotkeys:
- enter: search if no entery is selected, if some enteries are selected opens their parent dir but currently is buggy
- double click: on enteries opens their parrent dir bit currently is buggy
- escape: while searching cancels the search otherwise exits the app
- ctrl+s: saves selected entries to file, or if not selected saves all of them
- ctrl+c: copy selected enteries, or if not selected, all of them
- ctrl+r: for resetting the searched enteries

the file type detection part uses a GPLv3 library and is not closd source or bsd compatible, i brlieve that nothing is closed source bin is already source code in another language but because of GPLv3 rules i won't fix it for release, currently crashs randomly only if not be used under debugger, is not intentional! only debugger changes mem layout and the lib's intrnal bug does not get triggered.
