# 100 Days Of Code - Log

### Day 0: December 4, 2017

**Today's Progress**: Planning on what my 100 days will look like.

**Thoughts:** I will be on Day 0 until I have a framework. What do I want to learn and how? Tutorials or Project or both?

My best time to think is while running. During my 5 mile run today during lunch, I was thinking of project ideas and came up with:
* Phase 1 - Swift iOS app that interfaces HealthKit
* Phase 2 - Build OpenSource API on GitHub for for HealthKit access.
* Phase 3 - Way to use Vapor for backend?

No clue how long this will take, but will add more if needed.

Studied HealthKit framework for two hours. Very complex...

### Day 1: December 5, 2017

**Today's Plan**:
* Mock up a quick prototype to pull some data characteristic and sample (weight) data out of HealthKit
* Design app front end - Not part of 100 hours.

**Today's Progress**:
* Pulled weights out of HealthKit. Nothing pretty, but data is back and in an array.

![Image of Prototype / Proof of Concept](https://richgabrielli.github.io/images/HealthKit-Proto.jpg)

**Thoughts:**:
HealthKit is complicated and privacy is a really big deal, which is a good thing. This is going to be fun!

### Day 2: December 6, 2017

**Today's Plan**:
* Take raw HealthKit data and manipulate it to a TableView
* Include a column for BMI calculation
* Design app front end - Not part of 100 hours.

**Today's Progress**:
* Accomplished the plan. Did not do any design work.

![HealtkKit Data Presentation in TableView](https://richgabrielli.github.io/images/HealthKit-Proto3.jpg)

**Thoughts:**:
* Tomorrows goal is to pull out exercise related data.

### Day 3: December 7, 2017

**Today's Plan**:
* Pull workout data from HealthKit.
* Design app front end - Not part of 100 hours.

**Today's Progress**:
* Accomplished the plan. Pulled the .Running Workouts.
* Did not do any design work.
* Learned that a lot of the sample type data that is part of the workout (heart rate, VO2 max, etc), it not stored with the workout. Workout has basic info (which I have accessed), but need to pull ancillary data by using the workout as the predicate...

![HealtkKit Workout  TableView](https://richgabrielli.github.io/images/HealthKit-Proto3.1.jpg)

**Thoughts:**:
* Tomorrows goal is to pull out exercise related data.

### Day 4: December 8, 2017

**Today's Plan**:
* Pull workout related data from HealthKit.
* Design app front end - Not part of 100 hours.

**Today's Progress**:
* Pulled all the heart rate data for al of the .Running Workouts.
* Performed the statistical predicate for the average heart rates for each workout.
* Became much more familiar with the completion handlers (closures) for asynchronous data access.
* Did not do any design work.

![HealtkKit Workout  TableView with Avg Heart Rate](https://richgabrielli.github.io/images/HealthKit-Proto4.jpg)

**Thoughts:**:
* Tomorrow's goals: clean up all the proof of concept code and refactor to Swift best practices. Also, create and implement a workout data model.

### Day 5: December 9, 2017

**Today's Progress**:
* Refactored proof of concept code using HealthKit best practices and MVC model.
* Focused on the M of MVC. Built a Profile model to hold the users profile data (height, sex, etc)

**Thoughts:**:
* Continue model work. Completing Profile and start an Exercise model. May be an opportunity to create a base class (Exercise) and use inheritance for the subs (Swim, Bike Run)?

### Day 6: December 10, 2017

**Today's Progress**:
* Focused on the M of MVC. Started to build / understand an Exercise Class for HealthKit.

**Thoughts:**:
* Pro: HealthKit has a tremendous amount of data capabilities and flexibility...Con: HealthKit has a tremendous amount of data capabilities and flexibility!

### Day 7: December 11, 2017

**Today's Progress**:
* Focused on the M of MVC. Completed exercise model that I am going to use and all the init.

### Day 8: December 12, 2017

**Today's Progress**:
* Made all changes to Proof of Concept incorporating the Exercise model.
* Streamlined HeartRate average in model. Changed predicate from workout to workout.startdate and workout.enddate.
* Tried to get VO2Max out using the same type of Statistical Query. No Luck. Should be straight forward: same as HR, but with Type .vo2max

### Day 9: December 13, 2017

**Today's Progress**:
* Continued to try and get VO2Max out. No Luck at all. No errors, just nil results. Should be straight forward. Not a lot online. Watched Apple talk introducing vo2max, but nothing.
* Refactored sample function to allow passing a sample type and returning the value. Much more efficient.

### Day 10: December 14, 2017

**Today's Progress**:
* Continued to try and get VO2Max out. Banging my head up against the wall!!!
* Posted a question on iOS Slack.

### Day 11: December 15, 2017

**Today's Progress**:
* Continued to try and get VO2Max out. Banging my head up against the wall!!!
* No responses on iOS Slack.
* Gave up... While brushing my teeth before bed a light bulb went off. Fired up my Mac and voila!!! VO2Max EVERYWHERE!!!
* Resolution: VERY simple fix: VO2Max was not authorized as a valid parameter. I will never forget that again.

### Day 12 - 16: December 16 - 29, 2017

**Today's Progress:**
* First: Where have I been the past 15 days? Son's knee surgery, holiday stuff, life... I worked a total of 5 hours during this time on the proof of concept. For all intents and purpose the POC is done:
* Reading data from HealthKit
* Built Weight / BMI history screen.
* Write weight and BMI (calculated) data to HealthKit.

* I could keep going on the POC, with cleanup and refactoring, but i am ready to move onto to the app and build it for real. This includes a pretty design and tight code.

**Lessons Learned:**
* First: Where have I been the past 15 days? Son's knee surgery, holiday
* Ability to read / write data from / to HealthKit
* Design HealthKit class.
* Design HealthKit data model for profile.
