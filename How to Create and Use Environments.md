# How to Create and Use Environments ![Environments icon](https://github.com/MarilizaC/icons/blob/master/Icon-Environments.png) 

An environment requires at least one online peer, with resources that match your needs, on which to run. You can rent another user’s peer or you can use your own peer. 

The instructions in this guide show you how to create an environment within Subutai Bazaar. Prior to creating an environment, be sure that you are logged in to the Bazaar with your account credentials, and with the PGP key configured in the Account settings. To help manage your keys, you may use the E2E Plugin for your specific browser. For more information about this plugin, see the companion software section at [Getting Started](https://subutai.io/getting-started.html#E2E).

To create an environment:
1. On the Environment page, click **Create Environment**.
2. On the Select Peers screen, check the box for the peer that suits your environment, and then click **Next**.

    :bulb: **``Tip``** | If none of the peers are suitable, click the “Search for other peers” link to select one from the Peers list.
  
3. On the Select Templates screen, select one from the Templates list on the right side.
Containers are assigned to templates starting from the top left, in a clockwise direction. 

   :pencil: **``Note``** | If you have your own template, upload it to the CDN tool first before you can select it here. For more information, see [Subutai CDN](https://docs.subutai.io/Products/Bazaar/10_CDN.html?highlight=cdn). If you are going to install a blueprint on the environment, refer to the [Writing Subutai Blueprints](https://github.com/subutai-blueprints/hackathon/wiki/Writing-Subutai-Blueprints) article for information about using custom templates.
  
4. Click the **+** icon for each container to configure the following properties:
    - **Size** - Select the size: Tiny, Small, Medium, Huge. For information about container sizes, see [What is GoodWill](https://github.com/subutai-blueprints/hackathon/wiki/What-is-%22GoodWill%22).
    - **Name** - Enter the container name.
5. Click **Save** to close the container properties, and then click **Apply**.
6. On the Save Environment popup, enter the name of the environment, and then click **Build**.

    You can monitor the progress through the status bar at the top of the page. 
    ![Status](https://github.com/MarilizaC/icons/blob/master/Screenshot%20-%20EnvContainer.png)
    
    When the build reaches the Ready stage, the state changes from **Under Modification** to **Healthy**.
    Congratulations! You have successfully created your environment.
    
### Keep Going! 
You can further customize the environment to suit your requirements. If, for example, you want to access the container using a domain name, configure the settings on the Container Port Mapping tab. On this tab, click **Add New Port** to display the popup where you can select or enter the following details, depending on your setup: Protocol, Port (Internal or External), Domain, Proxy peer, and Containers. Do not forget to save your settings. 

The settings for the container and its mapping state are displayed in the table, as shown in the screenshot below. 

![Container](https://github.com/MarilizaC/icons/blob/master/Screenshot%20-%20EnvContainer.png)

When you click the domain name link, you will be redirected to the container’s site (Apache, in this example).

![Sample](https://github.com/MarilizaC/icons/blob/master/Screenshot%20-%20EnvSample.png)

### What’s Next? 
You can to access the environment straight from your desktop, in four steps.

*First*, be sure to have the Subutai P2P daemon and Control Center installed and set up. These two working together provides access to your environment via SSH or Remote Desktop. To download these applications, go to the Companion software section of [Getting Started](https://subutai.io/getting-started.html#companion).

*Second*, in the Control Center, deploy an SSH key to the environment by accessing SSH-keys management from the menu.

![Control Center SSH](https://github.com/MarilizaC/icons/blob/master/Screenshot%20-%20EnvSSHKey.png)

*Third*, go to Environment from the menu, and then click the environment name to open it.

![Control Center Environment](https://github.com/MarilizaC/icons/blob/master/Screenshot%20-%20EnvCCStatus.png)

*Fourth*, under Remote Access, click **SSH** to open a terminal and access your container such as in the screenshot below.

![Control Center Shell](https://github.com/MarilizaC/icons/blob/master/Screenshot%20-%20EnvCCShell.png)

For more information about the Control Center and P2P daemon, see [How to Use Control Center and P2P](https://docs.subutai.io/Products/PeerOS/06_How_to_use_Control_Center_and_P2P.html).

Feel free to leave your questions or comments in our [Slack Community](https://slack.subutai.io/).
