![8272-Stevens-logo](https://user-images.githubusercontent.com/112715031/215599379-08253fee-1a1b-40b8-bf1e-6b9886d92b06.svg)
![Alt Text](https://media.giphy.com/media/Y0zTJ7VrKo9P2/giphy.gif)

# CPE-322-A: Meet Monday 10:00-11:50 AM in Babbio 104
## Engineering Design 6
### Justin Frederickson - Project Group 7

<sub>In this class, I want to better my coding and technical skills. I am excited to partake in projects during this course and learn from my peers and hopefully teach them something as well.</sub>

[Assignment Canvas Page](https://sit.instructure.com/courses/64902/assignments)
- [x] Assignment 0: GitHub Repository 
- [x] Assignment 1: Project Site
- [x] Assignment 2: Needs Assessment
- [x] Assignment 3: Problem Formulation
- [ ] Assignment 4: Solution Development
- [ ] Assignment 5: Intellectual Properties
- [ ] Assignment 6: Abstraction and Modeling
- [ ] Assignment 7: Synthesis
- [ ] Assignment 8.1 and 9.1: Ethical Issues
- [ ] Assignment 8.2 and 9.2: Product Liability
- [ ] Assignment 8.3 and 9.3: Social Impacts
- [ ] Assignment 10: Design Analysis
- [ ] Assignment 11.1: Design Diagrams
- [ ] Assignment 11.2: Gantt Chart
- [ ] Assignment 11.3: Senior Design Plan

## Take Me To: 
[Lab 1](https://github.com/Justin-Frederickson/CPE-322-A/blob/main/README.md#lab-1---ghdl-and-gtkwave)
[Lab 2](https://github.com/Justin-Frederickson/CPE-322-A/blob/main/README.md#lab-2-command-line)
[Lab 3](https://github.com/Justin-Frederickson/CPE-322-A/blob/main/README.md#lab-3-python)
[Lab 4](https://github.com/Justin-Frederickson/CPE-322-A/blob/main/README.md#lab-4-django-and-flask)

***Week 1 Class:***
[Slides](https://docs.google.com/presentation/d/1EON8wVCtc3M37qrlbpdFvbo2FVSsxpGTJ8VCOo5dSWI/edit)
- This class was used to introduce the introductory material for the course and set expectations for the rest of the semester.
  - Do Assignment 0 in Canvas.

***Week 2 Class:***
[Slides](https://docs.google.com/presentation/d/1Uh1TXoYzjnceXi6R4fjWkOPfbCHY4uNWmRdT_rICJ2c/edit#slide=id.p4)
- This class was used to identify some of the attributes that an engineer should possess to be successful and describe the stages of the engineering design process used to develop innovative solutions to technical problems.
  - Do Assignment 1 in Canvas.
  - Do Lab 1 and publish into GitHub (Either learn VHDL or Verilog).
  
## Lab 1 - GHDL and GTKWave
- For this lab, I needed to install GHDL and GTKWave and perform different examples.
  - This was performed in [Ubuntu](https://ubuntu.com/)
  - [Link to Lab](https://github.com/kevinwlu/dsd/tree/master/ghdl)
  
### Half-Adder Example Code:
```sh
$ ghdl -a ha.vhdl
$ ghdl -a ha_tb.vhdl
$ ghdl -e ha_tb
$ ghdl -r ha_tb --vcd=ha.vcd
ha_tb.vhdl:47:5:@5ns:(assertion error): Reached end of test
$ export DISPLAY=:0
$ gtkwave ha.vcd
```  
![half adder](https://user-images.githubusercontent.com/112715031/215637050-99fff18b-db58-4818-96e1-9f6105d51d07.JPG)

### D Flip Flop Example Code:
```sh
$ ghdl -a dff.vhdl
$ ghdl -a dff_tb.vhdl
$ ghdl -e dff_tb
$ ghdl -r dff_tb --vcd=dff.vcd
$ export DISPLAY =:0
$ gtkwave dff.vcd
```
![flip flop gtk](https://user-images.githubusercontent.com/112715031/215637314-429526d2-4dd4-4ef8-bcc6-df8d55c6983e.JPG)

### 4-to-1 Multiplexer
```sh
$ ghdl -a mux.vhdl
$ ghdl -a mux_tb.vhdl
$ ghdl -e mux_tb
$ ghdl -r mux_tb --vcd=mux.vcd
$ export DISPLAY=:0
$ gtkwave mux.vcd
```
![4 to 1 multi](https://user-images.githubusercontent.com/112715031/215922535-51b057cb-b620-4328-a0d8-d7ac483074b9.JPG)

### Issues That Were Ran Into: 
- In order to run GTKWave, an X-server is needed, which Windows does not have automatically. 
  - Which would cause this error when trying to run GTKWave without an X-server:
  
  ![half adder code 1](https://user-images.githubusercontent.com/112715031/215638323-9c1197e6-af68-486e-b0d7-b60c34973afa.JPG)

- [Xming](https://sourceforge.net/projects/xming/) was downloaded in order to have a working X-server.
  - In order to start the server after downloading Xming, use Xlaunch and click "Next" until you reach a screen as shown. Click "Finish" to start server.
  
  ![xming](https://user-images.githubusercontent.com/112715031/215922972-daf50887-d050-4316-92ca-d9ec0e2ddb2e.JPG)
  
  - You can check within task manager to make sure that the server is running: 
  
  ![xming in task](https://user-images.githubusercontent.com/112715031/215923937-9673e731-f8eb-4e1e-a4a6-4e106b4e2c9d.JPG)

  - This server running explains the $ export DISPLAY=:0 line of code. This enables the user to run commands that need an X-server. The X-server simply creates the display that GTKWave would produce. 
    - [Thank you to these people for helping me out](https://stackoverflow.com/questions/65844764/could-not-initialize-gtk-is-display-env-var-xhost-set-on-debian-wsl#:~:text=The%20error%20is%20due%20to,that%20require%20an%20X%20server.)

***Week 3 Class:***
[Slides](https://docs.google.com/presentation/d/1Q7mT4uKBsrwoN9vUQ16G_DVsxvoeXVz9X-wufzpt1m4/edit#slide=id.p4)
- This class went over design proposals and focused on what makes a good design proposal.
  - Do Assignment 2
  - Do Lab 2

## Lab 2: Command Line ##
- We were given different processes to execute in a Terminal for this lab.
  - This was performed in [Ubuntu](https://ubuntu.com/)
```sh
$ hostname 
$ env
```
![hostname env](https://user-images.githubusercontent.com/112715031/217091959-fe2697c5-d6cb-46d4-be5b-09ac82f98746.JPG)

```sh
$ ps
$ pwd 
$ git clone https://github.com/kevinwlu/iot.git
$ cd iot
$ ls
$ cd
```
![pspwdgitclonecdiotcd](https://user-images.githubusercontent.com/112715031/217092181-0b03d8cf-bb87-4307-a035-c691eb87d51d.JPG)

```sh
$ df
$ mkdir demo
$ cd demo
$ nano file
$ cat file
$ cp file file1
$ mv file file2
$rm file2
```
![nanocat file](https://user-images.githubusercontent.com/112715031/217093010-66ba9bd3-86f9-4160-9c44-bca7c7d48d32.JPG)

```sh
$ clear
```
![clear](https://user-images.githubusercontent.com/112715031/217093097-8b30a686-3ec9-4439-accb-90468336c568.JPG)

```sh
$ man uname 
```
![man uname](https://user-images.githubusercontent.com/112715031/217093445-791ca549-a24c-4efd-a7d3-a23b61ab633d.JPG)

```sh
$ uname -a
$ ifconfig
```
![uname a ifconfig (2)](https://user-images.githubusercontent.com/112715031/217094080-2eba964f-fcf6-4d09-aeba-da86cfa7531d.jpg)

```sh
$ ping localhost
$ netstat
```
![ping and net (2)](https://user-images.githubusercontent.com/112715031/217094333-d9e02ff8-966b-427e-9cd9-e36304617dbc.jpg)

***Week 4 Class:***
[Slides](https://docs.google.com/presentation/d/1xiEvUE-jEBfzjii-egaJDa2-X8TgDXZcqa2o6Ssakto/edit#slide=id.p4)
- This class went over problem statements and honed in on how to analyze a problem and convey that for our Design Project. 
  - Do Assignment 3
  - Do Lab 3

## Lab 3: Python ##
- We were given different processes to execute using Python.
  - This was performed in [Ubuntu](https://ubuntu.com/)
  
First of all, pip, jdcal, astral, and geopy needed to be installed:
```sh
$ sudo apt install python3-pip
$ sudo pip3 install jdcal
$ sudo pip3 install astral
$ sudo pip3 install geopy
```
![pipo](https://user-images.githubusercontent.com/112715031/218526931-220299a3-fe59-48ce-a406-177b5d9578f1.JPG)
![installingpip](https://user-images.githubusercontent.com/112715031/218526946-541f945c-0044-40c9-950d-38a74c923df8.JPG)

```sh
$ cd ~/iot
$ cd *3
$ python3 julian.py
$ python3 date_example.py
$ python3 datetime_example.py
$ python3 time_example.py
```
![iottotime](https://user-images.githubusercontent.com/112715031/218527243-b4495fa9-0d54-4128-853c-581978706735.jpg)

```sh
$ python3 sun.py 'New York'
$ python3 moon.py
$ python3 coordinates.py 'SC Williams Library'
$ python3 address.py '40.74480675, -74.02532862031404'
```
![suntoaddress](https://user-images.githubusercontent.com/112715031/218527387-cf0cafbd-4819-4aba-8569-a077a67b63b6.JPG)

```sh
$ python3 cpu.py
$ python3 battery.py
$ python3 documentstats.py document.txt
```
![cputodoc](https://user-images.githubusercontent.com/112715031/218527502-da68303b-e6ca-4d9e-b97f-3ec644e552a4.JPG)

### Issues That Were Ran Into: ###
- When executing specifically $ python3 sun.py 'New York', this error would appear:
![error pytz](https://user-images.githubusercontent.com/112715031/218528359-376e0c99-74a8-476f-8add-cf4c816371c5.JPG)

- As well, when executing $ python3 cpu.py and $ python3 battery.py, this error would appear:
![psutil error](https://user-images.githubusercontent.com/112715031/218528619-eab5530d-3e82-488f-b4ec-8d0016ce30e4.JPG)

- These issues were solved by installing pytz and psutil, respectively.
![installpytz](https://user-images.githubusercontent.com/112715031/218529015-3267b670-b11a-4229-a588-f6eae034b4a7.JPG)
![installpsutil](https://user-images.githubusercontent.com/112715031/218529033-677b203a-9135-4865-ae5d-07ef5f9c4f30.JPG)

***Week 5 Class:***
[Slides](https://docs.google.com/presentation/d/1BQ9d0ZyjfMNBwducPZR1NMWj0qJrTKf6XpInYHuRyhw/edit#slide=id.p4)
 - In this class
  - Do Lab 4
  - Do Assignment 4
  
 ## Lab 4: Django and Flask ##
 - For this lab, we were tasked with installing, Django, Django REST Framework, and Task.
 - We would run each individual server and record our processes.
  - Django and Django REST Framework could not be ran, and I will explain why in the respective seciton.
  
### Django and Django REST Framework ###
 - Installing Django and Django REST framework:
 ```sh
$ pip3 -V
$ pip3 list
$ sudo pip3 install -U setuptools
```
![v to setup](https://user-images.githubusercontent.com/112715031/220395391-8ffabb65-94bc-4b7b-be58-5a91a6df27a9.JPG)
```sh
$ sudo pip3 install -U django
$ sudo pip3 install -U djangorestframework
$ sudo pip3 install -U django-filter
$ sudo pip3 install -U markdown
$ sudo pip3 install -U requests
```
![django to requests](https://user-images.githubusercontent.com/112715031/220395588-d2672515-f3cb-423a-9dc7-288ce1c41a64.JPG)
- Install MariaDB Server
```sh
$ sudo apt install mariadb-server mariadb-client
$ sudo apt install python3-mysqldb
```
![mariatomysqldb](https://user-images.githubusercontent.com/112715031/220396303-c136c258-ba42-4e4b-ab81-71c8653a0dce.JPG)
#### Where Errors Start To Pile Up: ####
- Error performing:
```sh
$ sudo apt install python3-mysqldb
```
- Error shows mysql and mariadb are not found, however previous picture shows they were installed correctly.
![mysql error](https://user-images.githubusercontent.com/112715031/220396781-d38fdde1-c956-4b45-a10b-d94c9d9787cc.JPG)
- Used this command to try and remedy the situation, however error still persisted. 
```sh
$ sudo apt install mysql-server mysqlclient
```
![mysqlinstall for secure](https://user-images.githubusercontent.com/112715031/220397240-ae51ad86-a0dc-479a-a01c-ed9a516a3632.JPG)
- Using the mysql_secure_installation command proved to not run either. The password could not be made out, and even pressing enter for no password would provide a similar error.
- Doing research on the error, I needed to make sure the SQL server is even running, and running a command to check shows that it is not. 
- I believe this section of the Lab is not possible for me without a Raspberry Pi. The Raspberry Pi would be running this SQL server, and seeing how the instructions are made out for this section to be done on a Raspberry Pi and my peers having success with this section on their own Raspberry Pi confirms my thoughts. 
```sh
$ sudo mysql_secure_installation
$ sudo systemct1 status mysql
```
![thislabnotworkinglol](https://user-images.githubusercontent.com/112715031/220398511-0ee37209-e249-4179-8d26-40c820690516.JPG)

### Flask ###
- After using the cd command to get into the lesson4 Github folder, Flask needed to be installed. 
- After Installation, the command to run the server could be made and the output coould be seen via a browser (http://127.0.0.1:5000/)
- It also does not mention using a Raspberry Pi for this section, which helps confirm my thoughts about the last section as well. 
![flask](https://user-images.githubusercontent.com/112715031/220399301-4a171c49-65f0-44ef-831d-7d7130b13270.JPG)
![flaskhelloworld](https://user-images.githubusercontent.com/112715031/220399312-b892bf95-a5b4-4cce-9901-3e0c1771cb60.JPG)

***Week 6 Class:***
[Slides](https://docs.google.com/presentation/d/1iCgARa2jhI0NOApFmR5njWCQ7CySHaB73SidghybsQ0/edit)





