# mtk-watch #

### Setup build enviroment ###
```bash

sudo apt-get install git git-core git-lfs gnupg flex bison build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 libncurses5 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig
```

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/hsyncvlk23/manifest -b t-alps-q0.mp1-V9.122.1

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

$ python vendor/mediatek/proprietary/scripts/releasetools/split_build_helper.py full_k39tv1_64_bsp-userdebug

```

The above command will give you 3 commands that are customized for the product and eng/userdebug/user you specfied

Note: Atleast on mt6739 building with eng made the device almost unusable due to the lag.
