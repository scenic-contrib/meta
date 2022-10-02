Attendees:
- Boyd Multerer
- Jason Axelson
- Chris Ertel
- Jason Johnson
- Alex McLain
- Ed Bond
- Luke Taylor


Agenda
* The possibility of creating a Scenic Core Team
  * Boyd’s attention is spread too thin
  * Boyd cares tremendously about design
  * We’ll need discussions about what good design looks like for Scenic
  * Boyd is especially interested in the remoting driver
  * Discussion of community needs vs Kry10 needs
    * Boyd’s inner conflict
      * Google Fuschia Scenic
    * What does Kry10 need from Scenic?
      * Scenic sweet spot: simple but functional control surfaces
      * Latency tolerant
      * Work identically across a variety of systems and drivers (i.e. canvas)
      * Remoting
      * Large number of people that know and use Scenic
      * Not a game engine (doesn’t match latency goals)
      * Not Really fancy animation engines
        * Especially in Scenic core
    * Discussion
      * “Animation callbacks PR”
        * Ask, can it be done in an addon/library?
        * Push back on communication between scenes and drivers
        * Script API is the Low Level Protocol
        * Maintaining the push/pull relationship between viewport/driver is important
      * There’s a bunch of deps that make up Phoenix
        * Something similar could be done for Scenic
      * Integration testing around viewport layer
      * Someone could create a non opengl renderer (i.e. vulkan)
         * What requires Kry10 sign-off
    * script format
    * Viewport
    * Large amounts of optional code in core scenic that isn’t used in most projects
      * Instead this can be in a scenic/some_lib
      * I.e. scenic.layout
    * drivers pull/scene push model
    * Every script api needs a way to draw it using pure web canvas
      * Difficulty: the scenic part that works with the web canvas isn’t released currently
      * Could also work if one call is replaced with 2-3 canvas calls
* The structure of a Scenic core team
  * GitHub’s CODEOWNERS?
    * Yes!
    * Don’t allow touching of viewports, etc.
  * Scenic Core Team and Scenic Contrib
    * Worth it to have both?
    * Have overlap
    * Scenic Contrib very open, but also very messy
    * Top-level namespace separation Scenic.x vs ScenicContrib.x
    * Have someone from Kry10 on Scenic Core Team (probably ed or ihor)
    * Pull vs push for getting things into core
      * Alex likes pull, less burden on maintainers
  * Hex permissions?
    * Let CI deal with Hex
    * Let individuals have permissions to hex
* How a Scenic Core Team could work with Boyd
  * Core can make and merge “most” PRs
  * PRs that touch viewport, script, etc. would require boyd or Kry10 signoff
  * Discussion locations
    * Periodic meetings
    * Have public minutes
    * Slack disappears
    * Create Scenic core team meta repo similar to https://github.com/scenic-contrib/meta
      * Ed volunteering to make these easier to access via a web page
      * People can comment via PRs
  * Style for community
    * Automated tooling
      * Sobelow, credo, inch, etc
      * Scenic used to have travis, it was dropped when travis changed their policies
      * Scenic contrib will be more loose, scenic core will be more tight
      * Use GitHub actions
  * Alex’s code review philosophy
    * Competing desires
      * Want low friction
    * Give the external contributor the option to let a core team member finish up the work
      * Help get their code in
* 0.12 is looking like 1.0
  * What is the set of criteria for 1.0?
* How to make Scenic more approachable and appear/be more lively/marketing
  * Neil is new marketer at Kry10, leverage him
    * Was chief marketing officer at Docker
    * Focused on developer communities
  * Include a code reloader
    * scenic/live_reloader (move from https://github.com/axelson/scenic_live_reload/)
  * Contributing guide in the core repo
  * Add debugability improvements
    * Add screenshots
  * Screenshots
    * Tracking here: https://github.com/ScenicFramework/scenic_driver_local/issues/9
    * Helps with regression testing
  * Documentation of wire format of scripts
  * Documentation is spotty
  * scenic.new.example looks amateur
    * Make it look like an application
  * Boyd to do whiteboard session on zoom going through scenic code?
    * After Nov 15th Boyd can do it
    * YouTube series!
      * Need to create a youtube channel?
        * Host on Nerves youtube channel?
  * Two pieces of code
    * Local driver should work on windows
    * Local driver on RPI4 is really slow
  * Create content showing how to use scenic
    * Especially on desktop
  * Promote scenic content that people are creating in the community
  * Get into Lars newsletter
    * Ask him to create a separate scenic newsletter?
  * Get on ThinkingElixir podcast
    * Boyd?
  * Activity on GitHub
  * Have example fairly featured scenic applications
    * Matrix frontend?
* Schedule and format for future meetings
  * Once a month

Actions:
* Invite Ed Gurgel & Ihor Kuz to both scenic channels
* Invite Ed Gurgel & Ihor Kuz to the next chat and neil
* Boyd to write down good design principles
  * We have to bug boyd to do that
  * Low power
  * Less code running at runtime
* Ask Neil about scenic/kry10 youtube channel
* In a future meeting/session we want to hash out
  * Who does what
  * List of priorities
