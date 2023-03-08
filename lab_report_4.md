# Week 7 Lab Tasks Review

## Steps Summary
1. Setup Delete any existing forks of the repository you have on your account
2. Setup Fork the repository
3. The real deal Start the timer!
4. Log into ieng6
5. Clone your fork of the repository from your Github account
6. Run the tests, demonstrating that they fail
7. Edit the code file to fix the failing test
8. Run the tests, demonstrating that they now succeed
9. Commit and push the resulting change to your Github account (you can pick any commit message!)

## Reproduce the steps

**Attention**: Skip step 1 if you do not have a lab7 repository on your github account

### Step 1: 
- Go to the repository lab7 on your github account
- Click "Settings"
- Scroll down and click "Delete this repository" under Danger Zone
![image](https://user-images.githubusercontent.com/117802747/221001220-210fc858-b76e-4830-88cd-fbd9bd94967e.png)
- A warning will appear, type `<your account name> /lab7` in the box
- Click "I understand the consequences, delete this repository" to delete
  
![image](https://user-images.githubusercontent.com/117802747/221002361-ec2ed15d-2791-49a6-a948-e19c243cc3fc.png)

### Step 2
- Open https://github.com/ucsd-cse15l-w23/lab7 on your browser
- Click "Fork" on the top right corner of the page
- Click "Create Fork"
![image](https://user-images.githubusercontent.com/117802747/221005278-4406ed03-4f40-492e-a18f-53d6c3f929bd.png)

### Step 3
- The timer is about to begin!

### Step 4
- Open VSCode and a new terminal
- Press `<Ctrl-R>` and enter `"ieng"`, through searching the previous command containing "ieng", the ssh command I have previously entered so many times will automatically appear
 
![image](https://user-images.githubusercontent.com/117802747/221006312-8091390e-8918-4014-bd1c-69a680106a7d.png)
- Press `<Enter>`,and we have successfully logged into our account!

### Step 5
- Go to your github repository lab7 
- Click the Code button
- Select SSH and copy the strings below 
 
![image](https://user-images.githubusercontent.com/117802747/221007913-1e5f8ab4-7206-42d5-af8f-69775b05797f.png)
- Go back to VSCode, enter `"git clone"` and then do `<Ctrl-V>` to paste, then press `<Enter>` 
 
![image](https://user-images.githubusercontent.com/117802747/221008625-46ba3342-e234-4a22-a7f2-e854207c4484.png)

### Step 6
- Go to the folder lab7 by enter `"cd lab7"`
- Run the compile and execute commands, which demonstrate the failure
  - `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` 
  - `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`
 
![image](https://user-images.githubusercontent.com/117802747/221009768-f4dbb94a-6d6f-4dd0-9d7b-05f01ff4526f.png)

### Step 7
- To edit the file, enter `"nano ListExamples.java"`
 
![image](https://user-images.githubusercontent.com/117802747/221012408-8a1689b7-8975-4900-ae7c-c86ef19ab855.png)

- Press `<down>` 42 times and `<right>` 11 times or make your cursor reach the "1" at the end of "index1" in the third line of the last while loop in the code 
- Press `<delete>` and enter `"2"`
- Press `<Ctrl-O>` and `<Enter>` to save the change
- Press `<Ctrl-X>` to exit

![image](https://user-images.githubusercontent.com/117802747/221012163-2105d115-af06-4e1a-8c42-9545b3e99ae8.png)

### Step 8
Since the command was 3 up in the history, I used up arrow to access it.
- Press `<up>` 3 times to obtain the compile command, then press `<Enter>`. 
- Press `<up>` 3 times again to obtain the execute command, then press `<Enter>`.

![image](https://user-images.githubusercontent.com/117802747/221013477-9bdf8759-fb6f-4c3c-9141-642a075c51bc.png)

### Step 9
- Enter the following commands to commit and push the change to Github account
  - `git add ListExamples.java`
  - `git commit -m "Updated"`
  - `git push origin main`

![image](https://user-images.githubusercontent.com/117802747/221014265-6b9aa49c-1b2c-4968-9075-4d7b2a69ec21.png)
