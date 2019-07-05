## Usage

This does not do anything yet.

## Development

You'll need to compile Bitcoin Core in the correct way. These instructions are
a start. They depend on a pending pull request [bitcoin/bitcoin#12557](https://github.com/bitcoin/bitcoin/pull/12557).

```sh
git clone  --single-branch --branch 2018/02/depends-openssl-aarch64-apple-darwin1 git@github.com:sjors/bitcoin.git BitcoinCore/bitcoin
cd BitcoinCore/bitcoin
./autogen.sh
cd depends
ln -s /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs SDKs
make HOST=aarch64-apple-darwin14 NO_WALLET=1 NO_QT=1 NO_UPNP=1
cd ..
./configure --prefix=`pwd`/depends/aarch64-apple-darwin14 --disable-tests --disable-bench
make
```
