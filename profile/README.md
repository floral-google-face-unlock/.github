```console
sudo apt install -y git python-is-python3
git clone https://github.com/akhilnarang/scripts; cd scripts; sudo bash setup/android_build_env.sh; cd ..; mkdir lineage; cd lineage
repo init -u https://github.com/LineageOS/android.git -b lineage-21.0 --git-lfs
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

git clone https://github.com/floral-google-face-unlock/.github -b lineage-21.0 .repo/local_manifests
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

source build/envsetup.sh; breakfast flame; croot; brunch flame
```
