# Pre-compiled Cpuminer for Userland:
This is a WIP repo for pre-compiled Flex (v2.0) binaries based on cpuminer(v24.3) made with Userland(v24.04.03), (Ubuntu v22.04.4 LTS), and GCC(v13.1.0).

# **`Disclaimer: I accept no warranties or liabilities on this repo. Do it at your own risk!!!`**

# **`This is for ARMv8 & ARMv9 usually modern smartphones but can work with aarch64 single board computers and other devices within Ubuntu`**

# Installation:
1. Download & install latest .apk from Apkmirror or Google Play Store [Userland](https://www.apkmirror.com/apk/userland-technologies-incorporated/userland/userland-24-04-03-release/userland-linux-on-android-24-04-03-2-android-apk-download):
```
https://www.apkmirror.com
```
2. Open Userland app and install Ubuntu accept permissions, we will use minimal environment and terminal or CLI this can take a couple minutes...
3. Get Ubuntu ready this can take a while:
- Type `y` then enter key in any prompts!
```
sudo apt update -y
sudo apt upgrade -y
sudo apt install git nano libcurl4-openssl-dev libjansson-dev -y
```
4. Download cpuminer, config, start:
```
git clone --single-branch -b flex https://github.com/Darktron/cpuminer.git
cd cpuminer
chmod +x start.sh cpuminer cpuminer-armv8 cpuminer-armv8-aes cpuminer-armv8-aes-sha2 cpuminer-armv8-crypto cpuminer-armv8-sha2 cpuminer-armv8.4-aes-sha3 cpuminer-armv8.5-aes-sha3-sve2 cpuminer-armv9-aes-sha3 cpuminer-armv9-aes-sha3-sve2
```
# Usage:

1. Edit your pool, address, worker name:
```
nano ~/cpuminer/config.json
```
2. Start cpuminer with:
```
~/cpuminer/start.sh
```
3. Close cpuminer with:
```
CTRL + c
```
4. View more cpuminer commands with:
```
~/cpuminer/cpuminer -h
```
5. (Optional) Change the miner name with desired one then benchmark the miner for example:
```
~/cpuminer/cpuminer -a flex --benchmark
```
6. (Optional) Change the miner name in the start.sh file to your desired one with:
```
nano ~/cpuminer/start.sh
```
# Tips & Tricks:
- If having issues consider starting from scratch force close Userland then clear cache & data.
- Disable battery manager, battery optimization for Userland app.
- If you long press anywhere within Termux then click `More` there is an option to `Keep screen on`.
- Alternatively you can pull down the notification drawer and expand Userland notification to `Acquire wakelock` this will enable you to mine with the screen off **(NOTE! not all devices obey this rule is a hit or miss)**
- Use a pool with low latency to your location/internet.
- Give the miner/stratum time to stabilize hashrate(~30m-1h).
