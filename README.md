# Swerve 2024 code
1740's swerve test repository for the FRC 2024 season. I am using this as a basis for the code structure of our actual 2024 codebase. To make changes to the repo, follow the [Github Setup in VSCode](#github-vscode-setup-tutorial). 
### Robot Physical Specifications
* size w l h
* camera positions
* Swerve specifications
* general position and idea GroundIntake
* general position and idea Note Pusher
* general position and idea Climber

### Subsystems
#### Climber
* num of NEOs
* how it works

#### GroundIntake
* num of NEOs
* how it works

#### Note Pusher
* num of NEOs
* how it works (is it belts or wheels)

#### Path Information
* Name: function and position

### Software Todo List (sorted by priority)
`People`
- [ ] Cordinate the software team and see who wants to help with software
- [ ] Inform software team of structure and git and PID
- [ ] Make sure they all have a solid understanding of the principles the code runs on ([see last year's repo](#last-year-repo))
- [ ] Make sure everyone has a solid understanding of java
- [ ] Cordinate tasks
- [ ] Assign some sort of laptop system

`General Software`
- [ ] Update codebase to 2024.2 when full release is out so we aren't on version "2024.1.1-beta-2"! This involves changing: 
* Many SparkMAX declarations to Spark
* The version of the RoboRio so builds will succeed. (This is what is currently preventing update now)
- [ ] Finish readme [Robot Physical Specifications](#robot-physical-specifications)
- [ ] Consider Advantage kit and/or scope data logging for the season [Scope](https://github.com/Mechanical-Advantage/AdvantageScope) [Kit](https://github.com/Mechanical-Advantage/AdvantageKit)

`Shuffleboard`
- [ ] Set up the shuffleboard base code, (not the indivudal methods that use it) based off last years example
- [ ] Add logging to drive subsystem to see wheel angles and robot position
- [ ] Add logging for note subsystems
- [ ] Add climber logging

`Swerve`
- [ ] Find out why turning motors were turning seemingly randomly and fix it
- [ ] Fix the one random wheel that didn't turn correctly
- [ ] Turn on field relitive control
- [ ] Add pathplanning for autos
- [ ] Finish the system functionality
- [ ] Tune the system so it works well
- [ ] If apriltag vision pose esimation should take precedence in getPose, update it to get the pos with the limelight if able

`Controls`
- [ ] Create a better controller scheme than last year to set up controls (addControlerFunction(func(), a)) ? (opt.)
- [ ] Create control ideas for the driver and co driver (talk to Abby and Co-Driver)
- [ ] Implement controls
- [ ] Make sure control feel is good and everything makes sense
- [ ] Different control selection from shuffleboard
- [ ] Controller rumble would be cool, could provide feedback on time left in match??

`Vision`
* Concurent work on limelight and lamelight
- [x] Import old code
- [x] Setup and update [limelight](https://docs.limelightvision.io/docs/docs-limelight/getting-started/summary)
- [ ] Calibrate the limelight with the online tool
- [ ] Check and fix imported limelight subsystem
- [ ] Incorperate limelight table with shuffleboard
- [ ] Get current limelight tag id and adjust co-driver controls based off it.

* Concurent work on limelight and lamelight
- [ ] Import old code
- [x] Grab the lamelight from last years robot
- [ ] Set up lamelight (Photon vision) ([see last year's repo](#last-years-repo))
- [ ] Incorperate lamelight table with shuffleboard
- [ ] Set up lamelight and calibrate it

`Climber`
- [ ] Actually figure out what the mechanics entail and how it works
- [ ] Find out how many motors it is
- [ ] Create stub code for testing
- [ ] See [Shuffleboard](#Shuffleboard)

`Note pusher`
- [ ] Figure out what this is called and rename it here
- [ ] Actually figure out what the mechanics entail and how it works
- [ ] See how the flap works
- [ ] Create stub code for testing
- [ ] See [Shuffleboard](#Shuffleboard)

`Ground Intake`
- [ ] See how the ground intake works
- [ ] Create stub code
- [ ] Create subsystem
- [ ] See [Shuffleboard](#Shuffleboard)

### Last Year's Repo
* :warning: This is intended as a place of reference to see the general structure, not to copy code without understanding it
* [2023 Souce Code](https://github.com/crephoto/CommandBased_2023)

### Important Devolopment Resources
This is the main resource we use besides googling things, this contains most, if not all the answers you need
* [Wpilib Documentation](https://docs.wpilib.org/en/stable/docs/zero-to-robot/introduction.html)
* [Java Wpilib Api](https://github.wpilib.org/allwpilib/docs/release/java/index.html)
* [Limelight Vision Documentation](https://docs.limelightvision.io/docs/docs-limelight/getting-started/summary)
* [The Most Important Resource](https://www.google.com)
* If you need any further help or explainations, feel free to talk to me, or any of the software mentors.


### Github VSCode Setup Tutorial 
This is a guide for setting up Github with VSCode
* Create a [Github account](https://github.com)
* Sign into the VSCode with Github via the person logo in the bottom left above the wheel
* Fork/Clone the repository 
* Click on the source fork on the bottom left
* In the popup, click Create New Branch From
* Select your master/main branch to copy from
* Name it working
* :warning: If you are editing code on your main branch, you could break your git so edit on your working branch
* Now you are on working branch and you can edit code, you only have to create it once
* See [Using Git](#using-git)

### Using Git
#### Pushing Code
* Now that you have setup your github you can edit code on your working branch
* Make sure your changes work and make sure it builds and deploys before commiting
* After you finish the changes you now should look to the left panel and click the third git source control icon
* Hit Commit and if you haven't saved, hit Save all and Commit Changes
* Hit push (this moves your changes to main)
* Click on the lower left source control and switch to main
* Push your changes to the repository
* If there are merge conflicts don't touch anything and ask someone who knows, it can be easily resolved but you can mess it up really bad
* Make sure sync your changes with the repo
* Switch back to working and sync changes
#### Pulling Code
* Ideally this should be done every time you open your code
* If it has been a long time since you have worked it's a good idea to pull so you don't get a lot of merge conflicts
* To pull code, make sure you have to pending changes (if you do, see [Pushing Code](#pushing-code))
* Change to your main branch 
* Sync changes
* Change back to working
* Sync changes again on working

[Additional Info](https://code.visualstudio.com/docs/sourcecontrol/overview)