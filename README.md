# TryHackMe-Intermediate-Nmap

```Intermediate Nmap | Can you combine your great nmap skills with other tools to log in to this machine?```

Tonight, I would like to share my writeup of TryHackMe room [Intermediate Nmap](https://tryhackme.com/room/intermediatenmap). `Difficulty is Easy`.

![Intro](https://github.com/r1skkam/TryHackMe-Intermediate-Nmap/blob/main/0.png)

Firstly, scanning by using [Nmap](https://nmap.org/) tool to know which ports are listening in the targeted machine.

![nmap -sV -O](https://github.com/r1skkam/TryHackMe-Intermediate-Nmap/blob/main/1.png)

According to the scanning result, high port (31337/tcp) is listening and we have to connect that port by using [Netcat](http://www.stearns.org/nc/) utility to get some information as per `Task 1` instruction.

![netcat](https://github.com/r1skkam/TryHackMe-Intermediate-Nmap/blob/main/2.png)

Oh! we got credential.
According to the `Task 1` instruction, we can now connect lower port remote access.

![ssh](https://github.com/r1skkam/TryHackMe-Intermediate-Nmap/blob/main/3.png)

We found 2 directories `(ubuntu and user)` under `home`.

`user` folder can be accessed by any user even it is owned by `root` user due to the folder permission.

Next step, let's check both directories.

![ls -lah](https://github.com/r1skkam/TryHackMe-Intermediate-Nmap/blob/main/4.png)

Yayy! we found `flag.txt` file under `user` directory and we can read it because of the file permission is **anyone** can read.

Then, fill the answer and submit it.

![30 points](https://github.com/r1skkam/TryHackMe-Intermediate-Nmap/blob/main/5.png)

### Thanks for reading and your time!
