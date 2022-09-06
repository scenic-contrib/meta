Attendees:
- Eric Rauer
- Ben Wheatley
- Chris Ertel
- Jason Johnson
- Alex McLain
- Ed Bond
- Jason Axelson

Location: ElixirConf 2022 Lunch

Governance
- Are we aligned with Scenic's general direction?
- Do we want to support our own driver?
  - Ideally not

JasonA put forth some short term goals:
- Release 0.11
- Move scenic's code from boydm/scenic to the ScenicFramework organization
- Create guides to get started with Scenic

Ideas:
- Split Scenic into layers
  - Boyd owns the lower levels
  - community owns upper levels

Discussion about why do people want to use Scenic
- Scenic is good for the embedded use case
- "Acceptable for 2d use cases"
- Decent choice for UIs?
- Cooler to not use browser
- Ed wants to use it on desktop, but not production use case
- Provides fast/good feedback loop for Desktop

Scenic will always support embedded
Scenic will not have native OS chrome, we should accept that

Ideas:
- Tailwind UI like component library for Scenic?
- Community livebook for Scenic
- hype-up video like what Lars made for Nerves
- Try toucan for pairing?

What we want:
- Jason Johnson
  - Layouts and better font support
  - polishing and approachability
    - We should do a LiveBook
    - fly.io hosted livebook
- Alex McLain
  - Be able to create a UI that doesn't suck (IOT use case)
    - IOT UIs universally suck
  - Hardware availability for Scenic
  - Integration testing / end-to-end testing with Scenic
    - Ensure a button activates the right hardware components
    - Ensure the correct thing is displayed on the screen
- Ed Bond
  - Developer experience for getting started
  - cross-compiling drivers
    - here are common things that will go wrong
      - target cross compile chain requires deeper knowledge
      - When you [build](https://github.com/boydm/scenic_driver_glfw) with a target OS architecture, which drivers are needed where and why. 
      - When you have that driver as a nested depedency, it can't easily build for targets like RISC processors 
- Jason Axelson
  - Get 0.11 released and create some guides
  - specs right now are functions which makes then hard to inspect
- Eric Rauer
  - livebook for scenic
  - rich interactive guide
- Ben Wheatley
  - custom components
    - need a guide
    - creating your own button is a large amount of effort, lots of staring at Scenic code
- Chris Ertel
  - No spec for how to talk to a driver
  - Would be nice to have a debug driver that barfed the scene graph
    - return it as JSON
  - updating components is weird

Discussions:
- Chris is working on a plotting library
- not a pure 2d scene graph
- more processes than not
- updating components is weird
- Having a nice pulsing button is a great example of the type of polish that Alex wants
- Has anyone used stencils in Scenic?
  - A: no
- How do you write tests for code that uses Scenic?
- Canvas driver available?
  - A: not right now

Livebook
- Might be hard to transition out of livebook to an actual Scenic application
  - can have examples of this in the livebook itself
- maybe example with livebook and some example apps

Governance:
- Meet once a month
  - take meeting notes
- discarded communication options
  - slack
    - lose history
  - discord
    - walled garden
- github discussions

Open questions:
- What is our goal for Scenic?
