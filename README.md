# moodle38-plugins
## Script for Moodle Update
```bash
wget https://raw.githubusercontent.com/AdrianoRuseler/moodle-update-script/master/Moodle38update.sh -O Moodle38update.sh
chmod u+x Moodle38update.sh

sudo ./Moodle38update.sh | tee Moodle38update.log
```
## Downloads
- https://download.moodle.org/download.php/direct/moodle/moodle-latest.tgz
- https://download.moodle.org/download.php/direct/moodle/moodle-latest.tgz.md5

## Plugins List

```bash
mkdir moodle
cd moodle
```

- https://github.com/danmarsden/moodle-mod_attendance/tree/MOODLE_37_STABLE

```bash
git submodule add -b MOODLE_37_STABLE https://github.com/danmarsden/moodle-mod_attendance.git mod/attendance
```

- https://github.com/h5p/h5p-moodle-plugin

```bash
git submodule add -b stable https://github.com/h5p/h5p-moodle-plugin.git mod/hvp
cd mod/hvp
git submodule update --init
```



## Remove
```bash
git submodule deinit <path_to_submodule>
git rm <path_to_submodule>
git commit -m "Removed submodule "
rm -rf .git/modules/<path_to_submodule>
```



