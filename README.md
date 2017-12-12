## Usage

This does not do anything yet.

## Development

You'll need to compile Bitcoin Core in the correct way. These instructions are
a start, but won't work pending [bitcoin/bitcoin#11720](https://github.com/bitcoin/bitcoin/issues/11720).

```sh
git clone git@github.com:bitcoin/bitcoin.git depends/bitcoin
cd depends/bitcoin
./autogen.sh
./configure --with-incompatible-bdb --without-gui --disable-tests --disable-bench
make
```