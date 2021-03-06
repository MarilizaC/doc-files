# Run Subutai PeerOS with Vagrant
The easiest and quickest way to get a Subutai peer running on any platform is to use Vagrant with VirtualBox. Learn how to do a basic setup on Debian Stretch by following the instructions in this guide. 

## Before you start
Download the required software from their respective websites:
- Debian Stretch - 9.x
- Vagrant - 2.0.1 or higher
- VirtualBox - 5.0.1 or higher
    
    :small_red_triangle: **```Important```** | Do not use package managers to avoid installing versions that might be out of date. 
    
## Install and run Subutai PeerOS
With all the prerequisites installed and set up, you can start creating a Subutai peer VM on Debian Stretch:

1. Create an initial Vagrantfile (minimal Vagrantfile, in this case) on the Debian Stretch box:
    ```
    ~$ vagrant init --minimal subutai/stretch
2. Install the subutai and vbguest Vagrant plugins:
    ```
    ~$ vagrant plugin install vagrant-subutai
    ~$ vagrant plugin install vagrant-vbguest
3. Create and start the Subutai peer VM:
    ```
    ~$ vagrant up
    ```
    At one point, you will be prompted to select which bridge interface you want to use. 
    The first option provided by Vagrant is usually the right network interface that is actively being used to connect to the Internet.

### You’re done!
Congratulations, you now have a peer! Towards the end of the output stream, you should see a message similar to the following:
``` 
 default: SUCCESS: Your peer is up. Welcome to the Horde!
 default: -----------------------------------------------
 default:
 default: Next steps …
 default: Make sure Subutai's E2E Extension/Plugin is installed in your browser
 default: Search for 'Subutai' in your browser's extension/plugin store to find it and install.
 default:
 default: Console URL: https://172.16.1.121:8443
 default: Default u/p: 'admin' / 'secret'
 default:
 default: Vagrant ssh and change the default 'subutai'/'ubuntai' user password!
 default: If you forget the url, just take a look in .vagrant/generated.yml
```
### What’s Next?
Complete the post-installation procedures to install the companion software: Subutai E2E browser plugin, P2P daemon, and Control Center.	For more information, see the PeerOS and Companion software sections at [Getting Started](https://subutai.io/getting-started.html#E2E).

After creating your peer and completing post-installation, you can log in to the peer’s management Console through your own IP-based address or URL indicated in the output stream. Use the default credentials (`u/p` - username/password) that you can find below the URL. Refer to the sample URL and credentials taken from the output stream above:
```
default: Console URL: https://172.16.1.121:8443
default: Default u/p: 'admin' / 'secret'
```
Once logged in to the Console, you can go ahead and register your peer with Subutai Bazaar. By doing so, you can rent it out or share it with other users. For more information, see [How to Use the Subutai Console](https://docs.subutai.io/Products/PeerOS/05_How_to_use_the_Subutai_Console.html).

