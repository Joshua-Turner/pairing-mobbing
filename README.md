# Pairing/Mobbing

**A repo to hold useful information and findings on pairing/mobbing. The following will be a general outline of some practices for Pair Programming / Mobbing and findings from some of my sessions.**

# Table of Contents

- [Benefits](#benefits)
- [Some best practices](#some-best-practices)
- [Some differences between Pairing and Mobbing](#some-differences-between-pairing-and-mobbing)
- [Things to avoid](#things-to-avoid)
- [Challenges](#challenges)
- [Remote Tooling](#remote-tooling)
- [Useful links](#useful-links)

**Pair programming** - Two developers working on a task together either remotely with tooling or on the same device. This is often more intense than mobbing but can be extremely effective.

**Mobbing** - Similar to pair programming except with 3 or more people. This is usually done to tackle larger or complex cases as well as spreading knowledge throughout the whole team.

Both pair and mobbing have the same roles which will be filled by the participants. That is drivers and navigators.

- Driver - This individual will be the only one writing code. The driver should alternate at defined intervals (like every 25mins for example). The driver is mostly focused on implementing the idea, code, solution that the navigator(s) suggest. They should trust the navigator.
- Navigator - Navigators will explore their ideas and guide the driver.
- Observer - Everyone in a mob who is not currently a driver or navigator.
  > Mob behaviours change and adapt as groups become more familiar with each other and the process. Nothing here is set in stone but should serve as a starting point.

## Benefits

### Knowledge sharing

As the roles facilitate getting stuck into the code, asking questions and exploring ideas, it's much easier for each member to spread their knowledge and learn from each other.

### Increased learning speed

By allowing each member to explore their ideas without being told exactly what to do it increases the rate at which you learn. Not only technical skills but a shared context of the problem and area of the system.

### Higher quality code

Just by having the code pass through multiple people you'll naturally end up with higher quality code.

Someone said it nicely along the lines of:

> "When working alone the best of you and the worst of you goes into the code. With Pairing/Mobbing however the best of each member goes into the code and the worst of each member doesn't"

### In process code review

This type of code review is much more thorough than a Pull Request (PR) model or asynchronous external code review.

It also enables other Extreme Programming (XP) practices like Trunk Based Development (TBD).

### Increases focus

By rotating the roles frequently it becomes easier to maintain a state of high focus.

### Better communication

The nature of the roles and rotation fosters communication with the whole team. Someone will always be talking and often the best discussions are brought to light.

### Team connectivity

Being able to communicate better, focus and gain a shared context makes it easier to bond. You're all working towards a common goal and by resolving issues together it really feels like a team effort.

## Some best practices

### Set an agenda for the session

- Ideally each session will have a goal(s) to achieve.
- This will help keep focus and provide a metric for the sessions productivity.
- These goals can be high level and can be added to during the session.
  - For example let's say we have a main goal to 'Refactor X method'.
  - During this process the team highlight an affected area like a poorly named variable to come back to later.
  - This can be added as a sub-goal and then whenever a navigator wants to focus on this area it won't be lost.
- It's worth going over the story/task and recapping a previous session so you're all aligned on what needs to be done.

### Ensure all participants can clearly see the screen

- Everyone should be able to see the screen (where code is written) at all times.
- When in person it's good to use a second larger monitor or even a projector.
- When remote it's always helpful to share the drivers screen even if using pairing tools.

### Treat each team member with respect

- These practices can only be effective when everyone feels comfortable and safe.
- Respect that everyone is an individual with different levels of knowledge, technical proficiency, way of learning, environment etc.
- All these things are amazing resources as the team can approach a problem from many different angles.

### Decreased dependencies

- In the pairing model, stories still require both parties to complete the work. However if one of those people is not available there is still someone left with context available.
- In a mob if a member is absent then the team is impacted much less as there are still multiple members with context on the problem able to continue the work.

### Roles

**Just rough guidelines which can and will change between teams and members**

#### Driver

- Focus on writing code and the immediate task at hand
- Don't be afraid to ask questions if you don't understand something

#### Navigator

- Keep high level objectives in mind
- Make notes about things to come back to later

#### Observers

- Feel free to make suggestions but ensure that this is in a respectful manner
- Use the time to think and research issues relating to the session goals
- Be present and support if the navigator gets stuck

### Rotate drivers regularly

- Ideally you'll rotate the driver at set intervals which gives everyone a chance to experience the roles and learning benefits that come with them.
- Can do this every 25mins for example like the pomodoro method. Note that this should be adapted to the needs of the group.
- Be sure to use a timer to stay on top of the rotations. See tooling below for some remote options. When in person it could even be an egg timer or alarm on someone's phone or watch.

### Take regular short breaks

- Be sure to take breaks little and often perhaps using the 20-20 rule or something like Pomodoro.
- For example take 3-4 5-10 minute short breaks and then a longer 15-30 min one.
- When a single member takes a break in a mob they lose some context for anything done whilst they were away. To mitigate this cost they could return to the mob as the driver to pick up the context again.

### Don't rush / Focus on creating quality code

- Don't be afraid to pursue high quality code whether it's the formatting or the approach.
- By running through the mobs best practices this will occur naturally.

### Use a whiteboard

- Highly recommend using some shared board or note space. This is good for exploring concepts, noting down agenda, goals and things to come back to
- Could also appoint a facilitator to handle these notes and even rotate that responsibility.

### Retros

- An optional retrospective could be held on the pairing/mobbing sessions to identify improvements and what went well.
- This could be done separately at the end of a session or even included in a sprint retro.
- This is a very useful practice when implementing pairing/mobbing for the first time or in a new team.

### Optimal mob size

- Varies from team to team and depends on the members, the task and environment.
- A popular size is 4 people, however you can also be effective with many more members.

## Some differences between Pairing and Mobbing

_**Taken from one of the [links](https://www.youtube.com/watch?v=eLLOOmS-7pY&t=3541s&ab_channel=SmartBear) below:**_

- Pairing is intense. Mobbing allows for more downtime.
- Pairing improves code. Mobbing improves it even more.
- Pairing improves predictability. Mobbing improves it even more.
- Pairing requires some planning. Mobbing requires much less.
  - This is referring to optimising the pair for efficiency vs learning. With pairing this is harder to do and often sacrifices learning for efficiency. In mobbing it's easier to include a member with knowledge and spread this so planning becomes incrementally more streamlined.
- Pairing requires some coordination. Mobbing requires much less.
- Pairing is sometimes more efficient than mobbing but when?
  - It's easier to identify the times where mobbing is more effective in an overview than pairing
- Mobbing could be considered an XP practice.

## Things to avoid

### Drifting away

If there is a distraction (phone call, slack message, someone at door) then be transparent and let your pair/mob know. This keeps everyone connected.

### Micromanagement

Navigators always telling the driver exactly what to do as opposed to the highest level of understanding.

### Five second rule

Where a navigator notices the driver makes a typo or something and immediately calls it out. Instead you should wait a little bit for them to notice before commenting.

### Pairing 8 hours a day

Extended sessions can be extremely intense and draining. There are also plenty of other working commitments in a day to attend to such as; checking and responding to emails/slack messages, attending other meetings and self care time.

## Challenges

- Pairing can be exhausting
- Intense collaboration can be hard
- Interruptions by meetings
- Different Skill levels
- Power Dynamics
- Pairing with lots of Unknowns
- No time for yourself
- Rotations lead to context switching
- Pairing requires vulnerability

## Remote Tooling

### IDE/Editors

- Any editor with simple screen sharing! 🌟
  - This is the easiest and most cost effective way to mob remotely.
  - Just have the driver share their screen, commit when times up, rotate, new driver pulls and shares screen
- VSCode Live Share
  - Great free tool for collaborating with shared editors and terminals remotely
  - Allows for sharing in browser or ID
- CodeTogether
  - Another collaboration tool with extensions for VSCode, IntelliJ and more
  - Has a free usage plan where you have 60 min sessions
- Teletype
  - Similar to Live Share but for Atom
  - Also allows for sharing in browser or IDE

### Timers

- MobTime 🌟
  - Useful browser based mob timer to help stay on top of goals and rotations
- Live Share Pomodoro
  - A VSCode mob timer
- Mobster
  - A downloadable application for running mobs

### Communication

- Slack huddles
- Google Meet
- Teams
- Zoom

### Whiteboard

- MIRO 🌟
  - The online collaborative whiteboard platform that enables distributed teams to work effectively together
  - Absolutely the best tool I've used so far
  - Highly optimised and searchable
- Freeform
  - Integrated whiteboard app for macos (similar to Miro)
- Jamboard
  - A digital whiteboard that lets you collaborate in real time

## Useful links

- [A live mobbing session](https://www.youtube.com/watch?v=AaYZqJdSVD4)
  - Shows many of the benefits of mobbing right away
  - Particularly like around 16:45 where navigator focuses on magic numbers and during the changes they learn more about the system
  - 20:10 where the navigator chooses a name for a number and says it will be temporary until he thinks of a better one. Then another
  - member of the mob offers a suggestion and a short productive discussion occurs
  - Throughout the session you see navigators continue on the path of their predecessor or completely focus on something else
  - Love how often they rerun tests
- [Part 2 of the live mobbing session](https://www.youtube.com/watch?v=4v_uEZQ9ec4)
  - This is the second session of the above where they have different mobbers carrying on with the same file from last time
- [In-depth article on strong pairing](https://martinfowler.com/articles/on-pair-programming.html#:~:text=Strong%2DStyle%20Pairing,-This%20is%20a&text=The%20rule%3A%20%22For%20an%20idea,codebase%2C%20...).)
- [Shorter article on strong pairing](https://llewellynfalco.blogspot.com/2014/06/llewellyns-strong-style-pairing.html)
- [Article on remote mobbing](https://www.remotemobprogramming.org/)
- [Great talk about mobbing with Q&A](https://www.youtube.com/watch?v=eLLOOmS-7pY&t=3541s)
  - Compares Pairing and Mobbing
- [A year's worth of learnings from adopting mob programming](https://www.farfetchtechblog.com/en/blog/post/a-year-s-worth-of-learnings-from-adopting-mob-programming/)
