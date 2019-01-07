# Factorio Init Script
A factorio init script for linux

# Dependencies
 Among others:
 - wget
 - cURL
 - xz-utils
 - tar
 - git

# Important
Every command listed here should be run as a non-root user.
My suggestion is to do the following:

 ```bash
 $ printf "Creating user factorio...\n"    #First time only
 $ adduser factorio
 $ usermod -aG factorio factorio
 $ printf "Logging in as factorio user:\n" #Every time you need to make changes
 $ su factorio
 ```

# Script Installation
Create a directory where you want to store this script along with configuration. (either copy-paste the files or clone from github):

 ```bash
 $ cd '~'
 $ git clone https://github.com/EssGeeEich/factorio-init.git finit
 ```

## Notes for users with an OS that has a older glibc version:

The config has options for declaring a alternate glibc root. The user millisa over on the factorio forums has created a wonderful guide to follow on creating this alternate glibc root ( side by side ) here:
https://forums.factorio.com/viewtopic.php?t=54654#p324493

## Setup
First things first, you should create a directory for your new instance, whose name ends with the port the server will be running on.

 ```bash
 $ mkdir factorio-34197                                           # Create the new instance directory
 $ cd factorio-34197                                              # Enter it in order to manage this instance
 $ ~/finit/factorio install                                       # Create the new instance
 $ cp data/server-settings.example.json data/server-settings.json # Copy the sample settings file
 $ nano data/server-settings.json                                 # Edit the settings file to your liking
```

The installation routine creates Factorio's `config.ini` automatically.

## Manage an instance
By entering an instance directory, you can manage it.
In the next example, you can see how to start an instance.
Run `~/finit/factorio help` to see what else you can do.

```bash
 $ cd ~/factorio-34197    # Enter it in order to manage this instance
 $ ~/finit/factorio start # Start it
 ```

# Thank You
- To all who find this script useful in one way or the other
- A big thank you to [Wube](https://www.factorio.com/team) for making [Factorio](https://www.factorio.com/)
- A special thanks to NoPantsMcDance, Oxyd, HanziQ, TheFactorioCube and all other frequent users of the [#factorio](irc://irc.esper.net/#factorio) channel @ esper.net
- Thank you to Salzig for pointing me in the right direction when it comes to input redirection
- At last, but not least; Thank you to all [contributors](https://github.com/Bisa/factorio-init/graphs/contributors) and users posting [issues](https://github.com/Bisa/factorio-init/issues) in my [github](https://github.com/Bisa/factorio-init/) project or on the [factorio forums](https://forums.factorio.com/viewtopic.php?f=133&t=13874)

You are all a great source of motivation, thank you.

# License
This code is realeased with the MIT license, see the LICENSE file.
