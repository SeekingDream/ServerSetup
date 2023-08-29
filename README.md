# Setting Up Environment on UTD GPU Server

Welcome to the guide for setting up your development environment on the UTD GPU server. This document will walk you through the necessary steps to establish the connection and configure the required environment for your projects.



## Connecting to the Remote Server

To begin, you'll need to establish a connection to the remote server using the SSH tool.

1. Start by ensuring that you have connected to the UTD VPN. If you haven't done this yet, follow the instructions provided in the link to set up the UTD VPN.

2. Once your VPN connection is active, you can proceed to connect to the remote server using an SSH tool.
   1. For Windows users, we recommend using Putty.
   2. Linux and Mac users can directly use the default command line tool.
     
4. Launch your SSH tool and enter the following command: ``ssh user_name@10.176.168.23``. Replace user_name with your username and then enter the password when prompted. If you're unsure about your username or password, please contact Simin for assistance.


## Setting Up the Python Virtual Environment

After successfully connecting to the remote server, the next step involves creating and configuring a Python virtual environment.

1. Begin by creating a new Conda environment with Python 3.10. Run the following command:
   `conda create -n your_env_name python=3.10`.
   Be sure to replace your_env_name with a name of your choice. Using Python 3.10 is recommended for compatibility.

2. With the environment created, install the necessary library dependencies based on the requirements of your projects.

## Managing Project and Dataset Paths
To ensure an organized structure for your projects and datasets, follow these guidelines:

1. All your projects should reside within the ~/Project directory. Create a project root under this directory, e.g., ~/Project/your_project_name. This is where your project's implementation code will be stored.

2. Store all your datasets within the ~/Dataset directory. For example, if you're working with the CIFAR dataset, place it in ~/Dataset/CIFAR. You can then create a symbolic link to connect this dataset to your project's directory.

3. To create the symbolic link, use the following command: `ln -s ~/Dataset/CIFAR ~/Project/your_project_name/dataset/CIFAR`.
   This will link the CIFAR dataset from the ~/Dataset directory to the dataset/CIFAR directory within your project.

By following these steps, you'll have a well-organized development environment on the UTD GPU server, allowing you to work efficiently on your projects. Should you need further assistance or encounter any issues, don't hesitate to reach out to our support team. Happy coding!

