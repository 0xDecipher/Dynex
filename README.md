# Dynex (DNX) team uncovered: Sergey Kozlov and a group of Ukrainian & Russian crypto veterans

In the recent months, the new crypto project “Dynex” (DNX) has gained a lot of attention, mainly because of the claim to build a blockchain based “decentralised neuromorphic supercomputing platform”. There has been much speculation about the team behind the Dynex, reason enough for us to start digging and to reveal our findings. At least in crypto, peace and united collaboration between Ukraine and Russia seems to be possible.

According to their website, Dynex is the “World’s first neuromorphic supercomputing blockchain based on the DynexSolve chip algorithm,
a Proof-of-Useful-Work (PoUW) approach to solving real-world problems.”. The main-net started in September 2022 with a fair launch (100% public allocation, no ICO, no pre-mining) and has since showcased a Proof-of-Useful-Work (PoUW) mining algorithm which potentially could be a revolution for the industry. Dynex’ coin, DNX, is listed on Lbank, Txbit, Tradeogre and Xeggex. DNX has since gained 1,500% in price and reports new hash-rate records on a weekly basis. Their technology, as described in their white-paper as well as in their DynexSolve paper (their PoUW algorithm is called “DynexSolve”) seems to be very advanced and is based on an alternative computing paradigm. But who are the people behind Dynex?

A WHOIS record request of their main website does not reveal much information. The Dynex developers are using Domain protection to hide the information about the registrar. Another potential source of information could be the route through their name server settings:

The records show that all of *.dynexcoin.org domains are pointed to Cloudflare, a service to secure websites, APIs, and Internet applications. We consider this positive for Dynex, because state-of-the-art cyber protection is an important criteria for any successful project. Nevertheless did we go ahead and applied multiple penetration test tools to see if we can pierce through to gather additional intelligence. Consider this also to test the resilience of their computing infrastructure by simulating a real-world attack, without any of the associated risks. Such attacks are especially effective in defending an organisation against unknown or “zero-day” threats. We do not publish the results here, but we can disclose that no vulnerabilities where identified. An active OWASP Core Ruleset has been detected. Access to the Dynex Web wallet is protected by a leaked credentials check in addition.

As most of Dynex’ code is open source, we spent almost 12 hours and digged deep into all of the repositories which are publicly available — by using classical editors but also by parsing binaries for non-stripped information with our developer tools. And there we go:

```
Sergey Kozlov
```

#Who is Sergey Kozlov?

It doesn’t take long to circle the name to what we believe is the main person behind the Dynex project. Sergey Kozlov, who has a Ph.D. in Economics and is also a visiting Professor at Kiev School of Economics, is an innovator and renowned expert in crypto. As a pioneer of decentralised computing. some of his work has influenced projects like XMR (Monero), TRTL (TurtleCoin) or BCN (Bytecoin). Sergey has quite a number of publications around crypto-assets and blockchain, some of which are:

- New approach to crypto assets fair value calculation and natural monopolies in a decentralized world (2018)
- Competition of Money (2018)
- DeFi — тихая финансовая революция (2020)

His early work was dedicated to digital cash in a decentralised world, later his interest evolved to smart contracts and DeFi. Proof-of-Useful-Work, which Dynex is offering, seems to be the logical next iteration. It also becomes clear why CryptoNote has been chosen by the developers as the core for their blockchain.

#Who are the Dynex Developers?

It is apparent that he must have started Dynex with the help of seasoned developers. We analysed different developer forums as well as contributions on the various Github profiles over the timelines and found that @Biomonster, an experienced senior developer (previously HiveOS and various other crypto projects), as well as the @Chernov_brothers are actively involved in the Dynex project. The track record and experience of the team members we managed to disclose is quite impressive which makes us believe that Dynex is being built on a solid foundation from a team perspective.

We find it remarkable that developers from Ukraine and Russia are peacefully collaborating on a new blockchain paradigm. Maybe the world should take crypto as an example — at last in that respect.

# Dynex [DNX] - Next Generation Blockchain for Neuromorphic Computing

With the end of Moore’s law approaching and Dennard scaling ending, the computing community is increasingly looking at new technologies to enable continued performance improvements. A neuromorphic computer is a nonvon Neumann computer whose structure and function are inspired by biology and physics. Today, such systems can be built and operated using existing technology, even at scale, and are capable of outperforming current quantum computers.

Dynex is a next-generation platform for neuromorphic computing based on a new flexible blockchain protocol. It is designed for the development of software applications and algorithms that utilize neuromorphic hardware and are capable of accelerating computation. To accomplish this goal, the platform connects hosts that are running clusters of neuromorphic chips with users and applications that utilize this next-generation hardware. On the Dynex platform, computation time is exchanged for the Dynex native token. 

Dynex has also developed a proprietary circuit design, the Dynex Neuromorphic Chip, that complements the Dynex ecosystem and turns any modern GPU into a simulated neuromorphic computing chip that can perform orders of magnitude more efficient than classical or quantum methodologies for a wide range of applications. Due to the dominance of ASICs in the proof-of-work token mining industry, there is a large amount of dormant GPU infrastructure available which can be converted into high performance next-generation neuromorphic computing clusters. The Dynex mainnet started on September 16th 2022.

For more information, read our [Dynex White Paper](https://github.com/dynexcoin/Dynex-Whitepaper)



## Using the Dynex Hosted Web Wallet to manage your DNX

Users who don't want to run a node or don't want to install anything can use the Dynex Mobile Web Wallet: 
https://dynexcoin.org/get-dnx/#wallets

## Using the Dynex-App to manage your DNX

Users who just want to use the Dynex wallet functionality to create wallets or send and receive DNX are recommended to use the convenient GUI based app. You can find it in the dedicated repository: https://github.com/dynexcoin/Dynex-Wallet-App 

## Mining DNX and managing DNX from the command line (precompiled binaries)

The easiest way to start mining DNX or to manage DNX wallet(s) from the command line in the terminal is by using our precompiled binaries. Download the version matching your operating system from our releases page:
https://github.com/dynexcoin/Dynex/releases

Please note that Linux and MacOS users are required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 

Linux:
```
sudo apt-get install libboost-all-dev 
```

MacOS:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew install boost
```

After downloading the precompiled binary, unzip the executable on your machine. To run a full Node in the Dynex blockchain, run the main service (=daemon) with the following command and wait until your node is fully synchronised with the network:
```
./dynexd
```

Please note that your node requires ports 17336 and SSL to be open.

![TuringX-Daemon](https://github.com/dynexcoin/Dynex/raw/main/turingxd.jpg)

From the command line, you can also create and manage your personal wallet to mine and transact your TRGX tokens (make sure you have the main service daemon running):

```
./simplewallet
```

![TuringX-Daemon](https://github.com/dynexcoin/Dynex/raw/main/simplewallet.jpg)

Then just follow the commands (use "O" to open an existing wallet or "G" to generate a new wallet for your TRGX).

## DynexSolve Mining Software

To run the Dynex Solve mining software, use the following command (check with your pool operator for the stratum details):

```
Linux based systems:
./dynexsolve -mining-address <WALLET ADDRESS> -no-cpu -stratum-url <POOL> -stratum-port <POOL> -stratum-password <POOL> (-multi-gpu)

Windows based systems:
dynexsolvevs -mining-address <WALLET ADDRESS> -no-cpu -stratum-url <POOL> -stratum-port <POOL> -stratum-password <POOL> (-multi-gpu)
```

Notes:
* DynexSolve binaries are currently available for Windows and Linux
* Currently supported GPUs: NVIDIA sm52 and better. AMD support coming soon
* You can also build DynexSolve from source: https://github.com/dynexcoin/DynexSolve

Note that the miner output shows computation speed, number of chips which are simulated, etc. Information about mining rewards can be observed in your wallet. When you start the DynexSolve miner, it will by default the GPU with device ID zero (the first installed one). You can specify another GPU if you like by using the command line parameter “-deviceid <ID”. To query the installed and available devices, you can use the command line option “-devices” which will output all available GPUs of your system and the associated IDs. A list of all available commands can be retrieved with the option “-h”. If you are running on Linux, DynexSolve will also generate a json file with the most recent statistics. These can be used with any mining farm management tool. Here is an overview of all DynexSolve command line options:

```
usage: dynexsolve -mining-address <WALLET ADDR> [options]

-mining-address <WALLET ADDR>    wallet address to receive the rewards
-daemon-host <HOST>              RPC host address of dynexd (default: localhost)
-daemon-port <PORT>              RPC port of dynexd (default: 18333)
-stratum-url <HOST>              host of the stratum pool
-stratum-port <PORT>             port of the stratum pool
-stratum-paymentid <PAYMENT ID>  payment ID to add to wallet address
-stratum-password <PASSWORD>     stratum password (f.e. child@worker1)
-stratum-diff <DIFFICULTY>       stratum difficulty
-no-cpu                          run no Dynex chips on CPU
-no-gpu                          run no Dynex chips on GPU (WARNING: MINING NOT POSSIBLE)
-mallob-endpoint <IP>            set the endpoint for the Dynex Malleable Load Balancer
-devices                         show GPU devices on this system
-deviceid <GPU ID>               which GPU to use (default: 0 = first one) when using 1 GPU
-multi-gpu                       uses all GPUs in the system (default: off)
-disable-gpu <ID,ID,ID>          disable certain GPUs (check -devices for IDs) when using multi-gpu
-maximum-chips <JOBS>            set maximum number of parallel Dynex Chips to be run on GPU (default: INT_MAX)
-steps-per-batch <STEPS>         set number of steps per batch (default: 10000, min 10000)
-start-from-job <JOB_NUM>        set the starting job number (default: 0)
-cpu-chips <INT>                 set number of CPU Dynex-Chips to run (default: 4)
-alpha <DOUBLE>                  set alpha value of ODE
-beta <DOUBLE>                   set beta value of ODE
-gamma <DOUBLE>                  set gamma value of ODE
-delta <DOUBLE>                  set detla value of ODE
-epsilon <DOUBLE>                set epsilon value of ODE
-zeta <DOUBLE>                   set zeta value of ODE
-init_dt <DOUBLE>                set initial dt value of ODE
-debug                           enable debugging output
-test <INPUTFILE>                test Dynex Chips locally
-mallob-debug                    enables debugging of MPI
-adj <DOUBLE>                    adjust used mem amount (default: 1.5)
-sync                            use cuda streams sync (reduce cpu usage)
-skip                            skip GPU state (.BIN) save/restore
-h                               show help
```

## Build Daemon, Simplewallet & WalletD from source

You can also entirely build all binaries from the source. First, clone the repository:
```
git clone https://github.com/dynexcoin/Dynex.git
```

### Linux

It is required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) and libcurl installed: 
```
sudo apt-get install libboost-all-dev (Ubuntu)
sudo apt-get -y install libcurl4-openssl-dev (libcurl Ubuntu)
```

To compile and build:
```
mkdir build 
cd build
cmake ..
make
```

### MacOS

It is required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew install boost
```

To compile and build:
```
mkdir build 
cd build
cmake ..
make
```

### Windows

1. It is required to have the [Boost library](https://www.boost.org) (Version 1.74.0 or better) installed: 
https://www.boost.org/users/download/

2. It is required to have [cmake](https://cmake.org/) for windows installed.
3. You also need [Microsoft Visual Studio](https://visualstudio.microsoft.com) (2017 or later) installed for the build process.

To compile and build:
```
mkdir build 
cd build
cmake ..
```
Then open Visual Studio: 
a) Make sure you have set Solution->Configuration to "Release". 
b) You also need to add "bcrypt.lib" to P2P->Properties->Configuration Properties->Librarian->Additional Dependencies. This is necessary to build boost's cryptographic randomizer functions. 
c) Add the LibCurl include files to CryptoNoteCore:
VC++ Directories -> Include Directories -> YOUR_CURL_PATH\libcurl-vc-x64-release-dll-ssl-dll-zlib-dll-ipv6-sspi\include
d) Add the LibCurl library directories to CryptoNoteCore:
VC++ Directories -> Library Directories -> YOUR_CURL_PATH\libcurl-vc-x64-release-dll-ssl-dll-zlib-dll-ipv6-sspi\lib
and
VC++ Directories -> Library Directories -> YOUR_ZLIB_PATH\zlib\lib

Once these settings are done, proceed a full build to generate your binaries.



