![8272-Stevens-logo](https://user-images.githubusercontent.com/112715031/215599379-08253fee-1a1b-40b8-bf1e-6b9886d92b06.svg)
![Alt Text](https://media.giphy.com/media/Y0zTJ7VrKo9P2/giphy.gif)

# CPE-322-A: Meet Monday 10:00-11:50 AM in Babbio 104
## Engineering Design 6
### Justin Frederickson - Project Group 7

<sub>In this class, I want to better my coding and technical skills. I am excited to partake in projects during this course and learn from my peers and hopefully teach them something as well.</sub>

[Assignment Canvas Page](https://sit.instructure.com/courses/64902/assignments)
- [x] Assignment 0: GitHub Repository 
- [x] Assignment 1: Project Site
- [ ] Assignment 2: Needs Assessment
- [ ] Assignment 3: Problem Formulation
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

### Obstacles That Were Ran Into: 
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
- We were given different processes to execute in a Terminal for this lab
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





