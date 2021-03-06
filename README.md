# moodle38-plugins
## Debian Config
```bash
wget https://raw.githubusercontent.com/AdrianoRuseler/moodle-update-script/master/DebianSystemConfig.sh -O DebianSystemConfig.sh
chmod u+x DebianSystemConfig.sh
sudo ./DebianSystemConfig.sh | tee DebianSystemConfig.log
```

## Script for Moodle Update
```bash
wget https://raw.githubusercontent.com/AdrianoRuseler/moodle-update-script/master/Moodle38update.sh -O Moodle38update.sh
chmod u+x Moodle38update.sh

sudo ./Moodle38update.sh | tee Moodle38update.log
```
## Downloads
- https://download.moodle.org/download.php/direct/stable38/moodle-latest-38.tgz
- https://download.moodle.org/download.php/direct/stable38/moodle-latest-38.tgz.md5

## Upgrade Submodules
```bash
git submodule update --remote
```
## Disable Notifications

```php
 // Moodle configuration file
 
// Use the following flag to completely disable the installation of plugins
// (new plugins, available updates and missing dependencies) and related
// features (such as cancelling the plugin installation or upgrade) via the
// server administration web interface.
$CFG->disableupdateautodeploy = true;
// Disabling update notifications
$CFG->disableupdatenotifications = true;
```

## TODO
- https://moodle.org/plugins/qtype_formulas
- https://gitlab.com/moodlenet/moodle-core-plugins/mod_moodlenet
- https://moodle.org/plugins/mod_turnitintooltwo
- https://github.com/moodleou/moodle-block_workflow

## Plugins List

```bash
mkdir moodle
cd moodle
```

- https://github.com/danmarsden/moodle-mod_attendance/
```bash
git submodule add -b master https://github.com/danmarsden/moodle-mod_attendance.git mod/attendance
```

- https://github.com/h5p/h5p-moodle-plugin
```bash
git submodule add -b stable https://github.com/h5p/h5p-moodle-plugin.git mod/hvp
cd mod/hvp
git submodule update --init
```

- https://github.com/blindsidenetworks/moodle-mod_bigbluebuttonbn
```bash
git submodule add -b v2.3-stable https://github.com/blindsidenetworks/moodle-mod_bigbluebuttonbn.git mod/bigbluebuttonbn
```

- https://github.com/trampgeek/moodle-qtype_coderunner
```bash
git submodule add -b master https://github.com/trampgeek/moodle-qtype_coderunner.git question/type/coderunner
git submodule add -b master https://github.com/trampgeek/moodle-qbehaviour_adaptive_adapted_for_coderunner.git question/behaviour/adaptive_adapted_for_coderunner
```

- https://github.com/dthies/moodle-atto_cloze
```bash
git submodule add -b master https://github.com/dthies/moodle-atto_cloze.git lib/editor/atto/plugins/cloze
```

- https://github.com/dthies/moodle-atto_fullscreen
```bash
git submodule add -b master https://github.com/dthies/moodle-atto_fullscreen.git lib/editor/atto/plugins/fullscreen
```
- https://github.com/FMCorz/moodle-block_xp
```bash
git submodule add -b master https://github.com/FMCorz/moodle-block_xp.git blocks/xp
```

- https://github.com/markn86/moodle-mod_customcert
Use of subplugins.php has been deprecated. Please update your '/var/www/html/moodle38/mod/customcert' plugin to provide a subplugins.json file instead.
```bash
git submodule add -b MOODLE_38_STABLE https://github.com/markn86/moodle-mod_customcert.git mod/customcert
```
- https://github.com/bynare/moodle-enrol_auto
```bash
git submodule add -b master https://github.com/bynare/moodle-enrol_auto.git enrol/auto
```

- https://github.com/moodleou/moodle-qtype_oumultiresponse
```bash
git submodule add -b master https://github.com/moodleou/moodle-qtype_oumultiresponse.git question/type/oumultiresponse
```

- https://github.com/bostelm/moodle-mod_scheduler
```bash
 git submodule add -b master https://github.com/bostelm/moodle-mod_scheduler.git mod/scheduler
```
- https://github.com/deraadt/moodle-block_completion_progress
```bash
git submodule add -b master https://github.com/deraadt/moodle-block_completion_progress.git blocks/completion_progress
```

- https://github.com/catalyst/moodle-tool_webanalytics

```bash
git submodule add -b master https://github.com/catalyst/moodle-tool_webanalytics.git admin/tool/webanalytics
```
- https://gitlab.com/jezhops/moodle-theme_adaptable
```bash
git submodule add -b master https://gitlab.com/jezhops/moodle-theme_adaptable.git theme/adaptable
```

## Remove
```bash
git submodule deinit <path_to_submodule>
git rm <path_to_submodule>
git commit -m "Removed submodule "
rm -rf .git/modules/<path_to_submodule>
```

- https://github.com/jleyva/moodle-block_configurablereports/tree/MOODLE_36_STABLE
```bash
 git submodule add -b MOODLE_36_STABLE https://github.com/jleyva/moodle-block_configurablereports.git blocks/configurable_reports
```

- https://github.com/dasistwas/moodle-mod_booking

```bash
git submodule add -b master https://github.com/dasistwas/moodle-mod_booking.git  mod/booking
```
- https://moodle.org/plugins/mod_questionnaire

```bash
git submodule add -b MOODLE_37_STABLE https://github.com/PoetOS/moodle-mod_questionnaire.git mod/questionnaire
```

