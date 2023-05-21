# XDDOS: An Advanced Minecraft Server Stress Tester

<p>
  XDDOS is a powerful tool that you can use to test your server's resilience
  against bots. It has many advanced features that make it a must-have for
  anyone who wants to ensure the stability and performance of their Minecraft
  server.
</p>

## Features

XDDOS has the following features:

- 54 different attack methods to choose from.
- Supports all versions of Minecraft.
- A proxy scraper that gets the latest proxies from a URL before each attack (just put the links to scrape proxy from in `urls.txt` file).
- A user-friendly command-line interface (CLI) that eliminates the need for difficult-to-remember startup commands
- Startup commands
- Auto IP resolver, which means that you can use the server IP or domain
- ANSI color support for better visuals in terminal

## System Requirements

- XDDOS is compiled using Java 17, which means that you can use Java 17 or above to run it.
- If running on linux kernel then it must have must epoll support or XDDOS will crash.

## How to run XDDOS

1. Download the XDDOS jar from [here](https://github.com/AnAverageBeing/XDDOS/raw/master/XDDOS.jar).
2. Create a folder to store XDDOS.jar in it.
3. In that folder, create a text file and name it `urls.txt`.
4. Put the links to scrape socks4 proxies from in that file. If you don't have any links, here are some just put these in `url.txt`:
   ```
   https://raw.githubusercontent.com/TheSpeedX/PROXY-List/master/socks4.txt
   https://raw.githubusercontent.com/ShiftyTR/Proxy-List/master/socks4.txt
   https://raw.githubusercontent.com/monosans/proxy-list/main/proxies/socks4.txt
   https://raw.githubusercontent.com/jetkai/proxy-list/main/online-proxies/txt/proxies-socks4.txt
   ```
5. To open the terminal, first navigate to the folder where the XDDOS jar file is stored. You can do this by using the `cd` command in the terminal and specifying the folder path. For example, if the XDDOS jar file is stored in the Downloads folder, you can navigate to it by typing `cd Downloads` in the terminal. Alternatively, you can open the folder where the XDDOS.jar file is stored in file explorer, and then type `cmd` in the address bar at the top of the window. This will open a terminal window in that folder.
6. Use one of the commands given [here](https://github.com/AnAverageBeing/XDDOS#startup-command) to start XDDOS.

### Things to know

- To get protocol number see [this page](https://wiki.vg/Protocol_version_numbers)
- **"Netty threads"** are a type of threads that *Netty*, a networking framework, uses in its *"event loop group"*. This group of threads is responsible for sending request to the server. To determine the optimal number of Netty threads to use, you can simply take the total number of threads available on your system and divide it by two.
- **"loop threads"** are used to make as many connection to server as possible. If you're not sure how many loop threads you should use, you can start with one or two and adjust as needed. What i found was value `1` and `2` works the best with mid specs vps.

### Startup Command:

- For user-friendly CLI/auto mode with colors:

```
java -jar XDDOS.jar
```

- For user friendly CLI/auto mode without colors:

```
java -jar XDDOS.jar -noansi
```

- for manual startup with colors:

```
java -jar XDDOS.jar [ip] [protocol] [method] [time] [netty threads] [loop threads] [y/n]
```

- for manual startup without colors:

```
java -jar XDDOS.jar [ip] [protocol] [method] [time] [netty threads] [loop threads] [y/n] -noansi
```

#### NOTE! :-

**`y/n`** is optional. Use **`y`** if you want to scrape proxy from links in urls.txt and **`n`** to use your own proxies from `proxies.txt` file.

## Example Attack Commands

- To run botjoiner for 10 seconds with 3 netty threads and 1 loop thread and use auto proxy generator:

```
java -jar XDDOS.jar localhost:25565 47 botjoiner 10 3 1 y
```

- To run botjoiner for 10 seconds with 3 netty threads and 1 loop thread and use your own proxy:

```
java -jar XDDOS.jar localhost:25565 47 botjoiner 10 3 1 n
```

- To run botjoiner for 10 seconds with 10 netty threads and 2 loop threads and use auto proxy generator:

```
java -jar XDDOS.jar localhost:25565 47 botjoiner 10 10 2 y
```

## Methods avilable

- BigHandshake
- BigPacket
- BotJoiner
- BotRaid
- BungeeDowner
- ChatSpam
- ColorCrasher
- CpuDowner
- DoubleJoin
- EmptyNames
- EmptyPacket
- ExtremeJoin
- ExtremeKiller
- Handshake
- InstantDowner
- InvalidData
- InvalidNames
- InvalidSpoof
- IpSpooffFlood
- Join
- LegacyPing
- LegitnameJoin
- LocalHost
- LongHost
- LongNames
- Memory
- MOTD
- nAntiBot
- NettyDowner
- Network
- NewNullping
- NullPing
- Ping
- PingJoin
- Query
- Queue
- QuitExceptions
- RAM
- RandomExceptions
- RandomPacket
- ServerFucker
- Slapper
- SmartBot
- Spoof
- TCPBypass
- TCPHit
- UltimateKiller
- UltimateSmasher
- UnexpectedPacket
- uuidCrash
- WaterfallBypass
- XDJoin
- XDSpam

## FAQ:

### The colours are bugged

Use `-noansi` flag at the end of the command or try using another terminal.

### XDDOS has a discord?

Yes. You can join [here](https://dsc.gg/TEAMXD).
