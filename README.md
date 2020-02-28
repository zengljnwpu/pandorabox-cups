
echo "src-git cups https://github.com/zengljnwpu/pandorabox-cups.git" >> feeds.conf.default

./scripts/feeds update -a

./scripts/feeds install -a

make menuconfig (set Network->Printing->cups as "M")

make

copy /source/bin/packages/[PLATFORM]/cups/*.ipk to machine & opkg install 

# Version of cups
2.3.0
