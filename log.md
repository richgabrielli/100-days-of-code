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
