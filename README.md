![296512556-a7d89350-81ee-4159-9d51-d0212461784a](https://github.com/diocode/42-Minishell/assets/107859177/b934a795-bd43-4029-9adf-f868d3825754)


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

![demo](https://github.com/user-attachments/assets/53e5faa5-0f94-45b3-a62f-93fac40d08a0)


<br>

## HOW TO USE
#### COMPILATION AND EXECUTION
#### 1º - Clone the repository
```bash
$ ./git clone git@github.com:diocode/42-Minishell.git
```

#### 2º - Enter the project folder and run `make`
```bash
$ ./cd 42-Minishell
$ ./make
```

#### 3º - Launch the program
```bash
$ ./minishell
```

> (optional) Launch the program using valgrind
```bash
valgrind -s --suppressions=readline_leaks.txt --leak-check=full --show-leak-kinds=all ./minishell
```

<br>

#### MAKEFILE COMMANDS
`make` or `make all` - Compile program **mandatory** files.

`make clean` - Delete all .o (object files) files.

`make fclean` - Delete all .o (object file) and .a (executable) files.

`make re` - Use rules `fclean` + `all`.
