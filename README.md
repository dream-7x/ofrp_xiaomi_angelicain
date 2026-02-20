# Device Tree for building OFRP for POCO C31 (angelicain)

1.Getting Started
---------------
**Initialize local repo**
```
mkdir ~/OrangeFox_sync
cd ~/OrangeFox_sync
git clone https://gitlab.com/OrangeFox/sync.git
```
**Sync up with this command:**
```bash
cd ~/OrangeFox_sync/sync/
./orangefox_sync.sh --branch 12.1 --path ~/fox_12.1
```

2.Preparing device for building
---------------
**Clone this repo**
```bash
cd ~/fox_12.1
git clone https://github.com/dream-7x/ofrp_xiaomi_angelicain.git device/xiaomi/angelicain
```

3.Build
---------------
**Set up environment**
```bash
. build/envsetup.sh
```
**Build the recovery**
```bash
lunch twrp_angelicain-eng
mka recoveryimage
```

* If also that is successful, congratulation!
* Go to `out/target/product/angelicain/` and you will find your recovery.img