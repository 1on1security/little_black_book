# Little Black Book
![Little Black Book](images/little_black_book.png)
## A small and perhaps growing, aging or rapidly depecating Little Black Book of Secrets

We've all done it - consulted the Root of All Knowledge (aka "Google") and long since forgotten the results. 
Do you find yourself searching for the same things repeatedly? I sure do. 
I've decided once I've done that three or four times it should end up here for ready reference.

## Minor Annoyances
- Client_loop: send disconnect: Broken pipe.: Annoyed by that persistent disconnect every time you step away for a beverage? A simple fix is found in /etc/ssh/sshd_config. Just a few sprays can provide a swift and lasting solution. The two configuration items of note are ClientAliveInterval and ClientAliveCountMax.  ClientAliveInterval is the period of inactivity after which the SSH server sends an alive message to the remote client that is connected to it, while ClientAliveCountMax is the number of attempts that the server will make to send the alive message from the server to the client. Ubuntu 22.04 for example defaults these to 0 and 3 respectively so you'll find yourself "kicked out" fairly often. Increasing ClientAliveInterval to 300 will increase your timeouts to fifteen minutes.

## Linux
- sudo without password: Using visudo or editing /etc/sudoers will allow editing sudo configuration for local users. Allowing a user named "foo" to sudo without typing a password is accomplished with an entry such as:
foo ALL=(ALL:ALL) NOPASSWD: ALL
This example allows user foo to execute ALL commands without password. ALL can be replaced with the path to a specific executable for refined control.

## Random
- Revive Stale Bread: 
If you've got a loaf of bread that's gone a bit hard, sprinkle it with water and put it in the oven for a few minutes. It'll come out almost as good as fresh.