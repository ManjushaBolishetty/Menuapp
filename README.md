Following are the steps to execute and run this project.

1. Download all the files to your local machine.
2. On the command line navigate to your project folder.
3. I have used a vagrant machine and hence execute the command "vagrant up". Once you do this the port mentioned is vagrantfile is active and reserved for the project.
4. Sometime we error, when we do a vagrant up, something like the port mentioned in the vagrantfile has already been used for some other project. In this case you will have to modify the host and guest in the following line in the Vagrantfile in the same folder.
"config.vm.network "forwarded_port", guest: 5010, host: 5010"
5. Also at time you might get a warning to update vagrant. Follow the instructions and execute the commands in the instruction.
6. Next once you receive a confirmation that vagrant up was a success, execute "vagrant ssh" to ensure you get securely access to the vagrant machine to access the shell.
7. Next do a "cd /vagrant"
8. If now you do "ls -ltr" you should be able to see database_setup.py, lotsofmenu.py, project.py along with other files.
9. Next execute the following commands in sequence.
python database_setup.py
python lotsofmenu.py - On successful execution outputs "added menu items!"
python project.py  - On successful execution outputs the below mentioned lines
* Running on http://0.0.0.0:5001/ (Press CTRL+C to quit)
* Restarting with stat
Since we are using the port 5001 in this project, it shows a message that the port is up and running.

10. Next when you visit http://localhost:5001/ shows the restaurant catalogue. The user can view the list of Restaurants, view the menu for each restaurant. But to add, delete , modify restaurant or menu for a restaurant the user needs to login.

11. Once the user clicks on the "click here to login", user is given with the choice of logging in through google plus or facebook". Once the user logins in, he can do any update , modify , create activities on the items created by him.

12. User will not have access to modify/ delete an entry created by some other user.

13. Once a user is done viewing the site and decides to leave the site, he can just logout by clicking the Logout link on the upper right corner.

14. This completes the process.
