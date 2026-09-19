# meoewmeow

A personal Android 16 ROM for the Nothing Phone (1) "Spacewar", built on crDroid 12.12.

## Where features come from

- **crDroid** — the base ROM (12.12, Android 16), itself built on LineageOS
- **AxionOS** — keyguard clocks, lockscreen widgets, QS and media UI, window blur, QuickLook providers
- **Own work** — cuttlefish x86_64 bring-up on Ivy Bridge hosts, build system fixes, and whatever didn't exist yet

## How it's organized

- `android_manifests` — repo local manifests (private)
- Each fork carries a `16.0-rime` branch with our commits on top of crDroid 16.0

## Building

```bash
repo init -u https://github.com/crdroidandroid/android -b 16.0
git clone git@github.com:meoewmeow/android_manifests .repo/local_manifests
repo sync
. build/envsetup.sh
lunch lineage_Spacewar-bp4a-userdebug
m bacon
```
