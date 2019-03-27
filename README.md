![image](http://catalanscoin.com/wp-content/uploads/2019/03/cropped-CatalansCoin.png)

CatalansCoin és una criptomoneda orientada per A la comunitat catalana amb un objectiu molt ambiciós, i que fins a dia d’avui, no ha estat aconseguit.

### Principis

- Llibertat.
  * Privadesa i valor. CatalansCoin és una moneda fungible i no rastrejable.
  * Tothom pot fer servir CatalansCoin sense cap limitació.
- Descentralització real.
  * La moneda és de la comunitat, no dels desenvolupadors. 0% de preminat.
  * Continuant amb l'anterior punt, l'algoritme de prova de treball serà eficient en qualsevol equip domèstic, destacant les CPU. També es combatrà activament el desenvolupament d'ASICs. La moneda és de la comunitat i no de les grans granges.
- Facilitat d'ús.
  * Es treballarà en millorar la usabilitat, la llibertat i l'aconseguiment una moneda centrada en les necessitats dels catalans.
  
### Especificacions
Algoritme Cryptonight Turtle V2.
Temps de bloc de 3 minuts i mig (per evitar network forks).
S'emetran 75000000000.00 monedes amb una corba d'emissió lenta, similar a la de la bitcoin. En 6 anys s'emetrà el 50% de les monedes, en 20 el 90%.

### Fast roadmap
Regalar monedes de forma gratuïta entre els membres de la comunitat. Com que és una moneda sense preminado, requerirà un gran esforç per la nostra part.

Incentivar la creació de nodes, treballar per crear una blockchain segura i descentralitzada.
Creació d'una organització externa no lucrativa i transparent, fundada per la comunitat. Aquesta organització governada per la comunitat, tindrà objectius diversos, com ara:
- Augmentar la freqüència de airdrops. Creació d'esdeveniments físics per donar a conèixer la moneda.
- Incentivar el desenvolupament d'eines desitjades per la comunitat.
- Donar suport al moviment independentista de Catalunya i la llibertat.
- Desenvolupament de carteres amb interfície gràfica per a qualsevol tipus de dispositiu.
- Producció d'un nou lloc web, rediseny del roadmap i creació d'un whitepaper.
- Canviar l'algoritme de minat a Cryptonight Catalans, per a millorar la resistència a equips de minat específics.
- Reduir el temps de bloc a 10 segons. Proposta molt agressiva i que només podrà ser duta a poc a poc segons augmenta el nombre de nodes.
- Estudiar la creació d'un nou algoritme de consens per repartir les monedes entre els catalans (Proof of Location).Implementar les propostes de la comunitat.

### Installing

We offer binary images of the latest releases here: http://latest.catalanscoin.com

If you would like to compile yourself, read on.

### How To Compile

#### Linux

##### Prerequisites

You will need the following packages: boost, cmake (3.8 or higher), make, and git.

You will also need either GCC/G++, or Clang.

If you are using GCC, you will need GCC-7.0 or higher.

If you are using Clang, you will need Clang 6.0 or higher. You will also need libstdc++\-6.0 or higher.

##### Ubuntu, using GCC

- `sudo add-apt-repository ppa:ubuntu-toolchain-r/test -y`
- `sudo apt-get update`
- `sudo apt-get install aptitude -y`
- `sudo aptitude install -y build-essential g++-8 gcc-8 git libboost-all-dev python-pip`
- `sudo pip install cmake`
- `export CC=gcc-8`
- `export CXX=g++-8`
- `git clone -b master --single-branch https://github.com/catalanscoin/catalanscoin`
- `cd catalanscoin`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./CatalansCoind --version`

##### Ubuntu, using Clang

- `sudo add-apt-repository ppa:ubuntu-toolchain-r/test -y`
- `wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | sudo apt-key add -`

You need to modify the below command for your version of ubuntu - see https://apt.llvm.org/

* Ubuntu 14.04 (Trusty)
- `sudo add-apt-repository "deb https://apt.llvm.org/trusty/ llvm-toolchain-trusty 6.0 main"`

* Ubuntu 16.04 (Xenial)
- `sudo add-apt-repository "deb https://apt.llvm.org/xenial/ llvm-toolchain-xenial 6.0 main"`

* Ubuntu 18.04 (Bionic)
- `sudo add-apt-repository "deb https://apt.llvm.org/bionic/ llvm-toolchain-bionic 6.0 main"`

- `sudo apt-get update`
- `sudo apt-get install aptitude -y`
- `sudo aptitude install -y -o Aptitude::ProblemResolver::SolutionCost='100*canceled-actions,200*removals' build-essential clang-6.0 libstdc++-7-dev git libboost-all-dev python-pip`
- `sudo pip install cmake`
- `export CC=clang-6.0`
- `export CXX=clang++-6.0`
- `git clone -b master --single-branch https://github.com/catalanscoin/catalanscoin`
- `cd catalanscoin`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./CatalansCoind --version`

##### Generic Linux

Ensure you have the dependencies listed above.

If you want to use clang, ensure you set the environment variables `CC` and `CXX`.
See the ubuntu instructions for an example.

- `git clone -b master --single-branch https://github.com/catalanscoin/catalanscoin`
- `cd catalanscoin`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./CatalansCoind --version`

#### OSX/Apple, using GCC

##### Prerequisites

- Install XCode and Developer Tools.

##### Building

- `which brew || /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- `brew install --force cmake boost llvm gcc@8`
- `export CC=gcc-8`
- `export CXX=g++-8`
- `git clone -b master --single-branch https://github.com/catalanscoin/catalanscoin`
- `cd catalanscoin`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./CatalansCoind --version`

#### OSX/Apple, using Clang

##### Prerequisites

- Install XCode and Developer Tools.

##### Building

- `which brew || /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- `brew install --force cmake boost llvm`
- `export CC=/usr/local/opt/llvm/bin/clang`
- `export CXX=/usr/local/opt/llvm/bin/clang++`
- `git clone -b master --single-branch https://github.com/catalanscoin/catalanscoin`
- `cd catalanscoin`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./CatalansCoind --version`


#### Windows

##### Prerequisites

- Install [Visual Studio 2017 Community Edition](https://www.visualstudio.com/thank-you-downloading-visual-studio/?sku=Community&rel=15&page=inlineinstall)
- When installing Visual Studio, it is **required** that you install **Desktop development with C++**
- Install the latest version of [Boost](https://bintray.com/boostorg/release/download_file?file_path=1.68.0%2Fbinaries%2Fboost_1_68_0-msvc-14.1-64.exe) - Currently Boost 1.68.

##### Building

- From the start menu, open 'x64 Native Tools Command Prompt for vs2017'.
- `cd <your_catalanscoin_directory>`
- `mkdir build`
- `cd build`
- `set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%`
- `cmake -G "Visual Studio 15 2017 Win64" .. -DBOOST_ROOT=C:/local/boost_1_68_0`

If you have errors on this step about not being able to find the following static libraries, you may need to update your cmake. Open 'Visual Studio Installer' and click 'Update'.

- `MSBuild catalanscoin.sln /p:Configuration=Release /m`

The binaries will be in the `src/Release` folder when you are complete.

- `cd src`
- `cd Release`
- `CatalansCoind.exe --version`

#### Raspberry Pi 3 B+ (AARCH64/ARM64)
The following images are known to work. Your operation system image **MUST** be 64 bit.

##### Known working images

- https://github.com/Crazyhead90/pi64/releases
- https://fedoraproject.org/wiki/Architectures/ARM/Raspberry_Pi#aarch64_supported_images_for_Raspberry_Pi_3
- https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-3

Once you have a 64 bit image installed, setup proceeds the same as any Linux distribution. Ensure you have at least 2GB of ram, or the build is likely to fail. You may need to setup swap space.

##### Building

- `git clone -b master --single-branch https://github.com/catalanscoin/catalanscoin`
- `cd catalanscoin`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make`

The binaries will be in the `src` folder when you are complete.

- `cd src`
- `./CatalansCoind --version`

#### Thanks
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, TurtleCoin Community, CatalansCoin Community

