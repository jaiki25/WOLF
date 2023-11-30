# WOLF
Installing the Cairo one compiler
If you're installing Cairo for the first time:

git clone https://github.com/starkware-libs/cairo/
cd cairo
git checkout 9c190561ce1e8323665857f1a77082925c817b4c
cargo build --all --release
If you already have Cairo installed:

cd cairo
git fetch && git pull
git checkout 9c190561ce1e8323665857f1a77082925c817b4c
cargo build --all --release
At this point you have Cairo installed in this repository.

Installing Cairo-lang
Go back to the root folder of the repo

cd ..
Set up a python virtual environment

python3.9 -m venv ~/cairo_venv_v11
source ~/cairo_venv_v11/bin/activate
If you had cairo-lang installed previously, uninstall it

pip3 uninstall cairo-lang
Install Cairo lang

pip3 install ecdsa fastecdsa sympy
pip3 install cairo-lang
Check that you have it installed correctly

starknet --version
Compile your contract using Cairo
You can use this smol demo contract to complete this test. It's a very basic event logger.

From your terminal, in the folder you installed Cairo in

cd cairo
cargo run --bin starknet-compile -- ../hello_starknet.cairo ../hello_starknet.json --replace-ids	

Congratulations, you have compiled your contracts from Cairo to Sierra!
