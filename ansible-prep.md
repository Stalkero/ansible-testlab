# Setting up the connection
1. Generate the ssh keys on ansible host `ssh-keygen`
2. Copy the public key to the worker node `ssh-copy-id@192.168.1.111`
3. Test the ssh connection from the host to worker node `ssh worker@192.168.1.111`
4. Do the updates on host server `apt-get update ; apt-get upgrade`
5. Add required repos for ansible `sudo apt install software-properties-common -y ; sudo add-apt-repository --yes --update ppa:ansible/ansible`
6. Install ansible `sudo apt install ansible -y`
7. Check if ansible installed correctly `ansible --version`
8. Test with the provided workspace folder if ansible 'pings' the worker/workers `ansible all -i ~/workspace/inventory/hosts -m ping`
