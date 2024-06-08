# Little Black Book
![Little Black Book](images/little_black_book.png)
## A small and perhaps growing, aging or rapidly deprecating Little Black Book of Spells

We've all done it - consulted the Root of All Knowledge (aka "Google") and long since forgotten the results. 
Do you find yourself searching for the same things repeatedly? I sure do. I've decided once I've done that three or four times it should end up here for ready reference.

## Minor Annoyances
- Client_loop: send disconnect: Broken pipe.: <br>
Annoyed by that persistent disconnect every time you step away for a beverage? A simple fix is found in /etc/ssh/sshd_config. Just a few sprays can provide a swift and lasting solution. The two configuration items of note are:<p>

- ClientAliveInterval and ClientAliveCountMax.<br> ClientAliveInterval is the period of inactivity after which the SSH server sends an alive message to the remote client that is connected to it. ClientAliveCountMax is the number of attempts that the server will make to send the alive message from the server to the client.<p>

Ubuntu 22.04 for example defaults these to 0 and 3 respectively so you'll find yourself "kicked out" fairly often. Increasing ClientAliveInterval to 300 will increase your timeouts to fifteen minutes.  If those fifteen minutes aren't enough, increase ClientAliveCountMax to 3.

## Linux
- sudo without password:<br>
Using visudo or editing /etc/sudoers will allow editing sudo configuration for local users. Allowing a user named "foo" to sudo without typing a password is accomplished with an entry such as:<p>
`foo ALL=(ALL:ALL) NOPASSWD: ALL`<br>
This example allows user foo to execute ALL commands without password. ALL can be replaced with the path to a specific executable for refined control.

## Ubuntu 22.04 LTS - Disable IPV6
`sudo nano /etc/default/grub`<br>
GRUB_CMDLINE_LINUX_DEFAULT="ipv6.disable=1 quiet splash"<br>
GRUB_CMDLINE_LINUX="ipv6.disable=1"<br>
`sudo update-grub`<br>
`sudo reboot`<br>

## Ansible Crib Notes
`ansible-inventory -i inventory.yaml --list`<br>
`ansible myhosts -m ping -i inventory.ini`<br>
`ansible-playbook -i inventory.yaml playbook.yaml`

## Random
- Revive Stale Bread: 
If you've got a loaf of bread that's gone a bit hard, sprinkle it with water and put it in the oven for a few minutes. It'll come out almost as good as fresh.
