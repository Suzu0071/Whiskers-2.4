# Beacon Configuration
__________________________________________________
SSH into the pi and run:
```
cd ~
git clone https://github.com/beacon3d/beacon_klipper.git
./beacon_klipper/install.sh
```
Could take up to 10 minutes...
_______________________________________________
Add to moonraker.conf:
```
[update_manager beacon]
type: git_repo
channel: dev
path: ~/beacon_klipper
origin: https://github.com/beacon3d/beacon_klipper.git
env: ~/klippy-env/bin/python
requirements: requirements.txt
install_script: install.sh
is_system_service: False
managed_services: klipper
info_tags:
  desc=Beacon Surface Scanner
```
___________________________________________
Check safe_z, remove [probe] section and restart the printer
