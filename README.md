# Notes for the future

this could be done on pypi, but I don't have access to the current pages and cannot currently compile for windows in build scripts.

* 32bit windows 10 VM used
* 32bit same python version as electrum
* 32bit cmake
* 32bit 7zip
* Visual Studio 15 from https://go.microsoft.com/fwlink/?LinkId=615448 (need MSCV and git)

pip install wheel

x16r_hash git cloned from https://github.com/brian112358/x16r_hash/commit/d79211ee8b5d86a9709caefded79f318a1d9f3a8 and built with python setup.py bdist_wheel

x16rv2_hash git clone from https://github.com/RavenCommunity/x16rv2_hash/commit/f8a9ef9a185b4c900adea4628be9b08aaab343ba and built with python setup.py bdist_wheel

kawpow source downloaded from https://files.pythonhosted.org/packages/2f/43/985379652c61953f4206a8c7eae56e670e1db62b3e3a89ca2d24528be90e/kawpow-0.9.4.4.tar.gz because its different than the version on git, IDK. Compiling apprently includes DLLs that dont exist on all windows platforms because windows i guess.

need to patch kawpow to include mscvp140.dll. used https://github.com/adang1345/delvewheel and delvewheel repair --no-mangle-all --no-diagnostic

I confirmed the validity of resulting wheel by unziping, diffing files, auditing changes, and comparing the hash of mscvp140.dll with the one from windows
