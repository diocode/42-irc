![banners-15](https://github.com/user-attachments/assets/c6a26c37-4d6d-49b0-b2d8-7e660ea9adc0)

<p align="center">
	<img src="https://img.shields.io/badge/status-finished-success?color=%2312bab9&style=flat-square"/>
	<img src="https://img.shields.io/badge/evaluated-05%20%2F%2012%20%2F%202024-success?color=%2312bab9&style=flat-square"/>
	<img src="https://img.shields.io/badge/score-100%20%2F%20100-success?color=%2312bab9&style=flat-square"/>
	<img src="https://img.shields.io/github/last-commit/diocode/42-Minishell?color=%2312bab9&style=flat-square"/>
	<a href='https://www.linkedin.com/in/diogo-gsilva' target="_blank"><img alt='Linkedin' src='https://img.shields.io/badge/LinkedIn-100000?style=flat-square&logo=Linkedin&logoColor=white&labelColor=0A66C2&color=0A66C2'/></a>
</p>

<p align="center">
	<a href="#about">About</a> •
	<a href="#how-to-use">How to use</a>
</p>

## ABOUT ([Subject](/.github/en.subject.pdf))

ft_irc is a C++ 98 IRC server that enables multiple clients to connect via TCP/IP, supporting real-time messaging in public channels and private conversations. Clients authenticate with a port and password, set a nickname and username, and communicate using standard IRC commands. The server forwards messages to all clients in a channel and enforces operator privileges, allowing actions like KICK, INVITE, TOPIC, and MODE to manage users and access settings.

The server must be non-blocking, handling all connections with a single poll() (or equivalent) for efficiency, ensuring it never hangs or crashes. Built strictly to C++ 98 standards, it forbids external libraries like Boost and must compile without errors. This project strengthens network programming skills, focusing on socket communication, event-driven architecture, and protocol implementation. The group for this project was myself, and [martimpinto](https://github.com/MartimPinto), and [filipepinholiveira](https://github.com/filipepinholiveira).

<a href="/.github/en.subject.pdf">Click here</a> for the subject of this project.

<p align="center">
  <img src="https://github.com/user-attachments/assets/53e5faa5-0f94-45b3-a62f-93fac40d08a0" alt="demo">
</p>

<br>

## HOW TO USE
#### COMPILATION AND EXECUTION
#### 1º - Clone the repository
```bash
$ ./git clone git@github.com:diocode/42-irc.git
```

#### 2º - Enter the project folder and run `make`
```bash
$ ./cd 42-irc
$ ./make
```

#### 3º - Launch the program
```bash
$ ./ircserv <port number> <password>
```

The server is running now and the there's 2 ways to connect to the server:
`nc` command through the terminal
`Hexchat` an IRC client application

To connect using the `nc` command:

```shell
nc localhost <port number>
```

<br>

**- Available Commands -**

*User Commands:*

`PASS` : Authenticate with the server before using other commands.
>Usage: PASS <password>

<br>

`NICK` : Set or change your nickname.
>Usage: NICK <nickname>

<br>

`USER` : Register with a username and real name.
>Usage: USER <username> 0 * <realname>

<br>

`JOIN` : Join or create a channel (becoming an operator if created).
>Usage: JOIN <#channel> [key]

<br>

`PRIVMSG` : Send a private or channel message.
>Usage: PRIVMSG <target>{,<target>} <message>

<br>

`PART` : Leave a channel. If empty, the channel is removed.
>Usage: PART <#channel>

<br>

`QUIT` : Disconnect from the server cleanly.
> Usage: QUIT

<br>

<br>

*Operator Commands:*

`KICK` : Remove a user from a channel.
>Usage: KICK <#channel> <user> [<reason>]

<br>

`INVITE` : Invite a user to a channel.
>Usage: INVITE <nickname> <channel>

<br>

`TOPIC` : View or change a channel’s topic.
>Usage: TOPIC <#channel> [<topic>]

<br>

`MODE` : Modify channel settings (+ to enable, - to disable).
	<br>`i` : Invite-only mode
        <br>`t` : Topic change restricted to operators
        <br>`k` : Set/remove channel password
        <br>`o` : Grant/revoke operator privilege
        <br>`l` : Set/remove user limit
 >Usage: MODE <#channel> <modestring> [args]

<br>
<br>

When using HexChat, PASS, NICK, and USER run automatically. In nc, they must be entered manually.

<br>

#### MAKEFILE COMMANDS
`make` or `make all` - Compile program **mandatory** files.

`make clean` - Delete all .o (object files) files.

`make fclean` - Delete all .o (object file) and .a (executable) files.

`make re` - Use rules `fclean` + `all`.
