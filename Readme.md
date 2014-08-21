
# NYC Node.js Talk - August 27, 2014

> This is the GitHub repository with examples, notes, and slides
for the talk here <http://meetup.com/nyc-node-js/events/199334592/>.

## Rapid MVP's with Node, Igloo, & Eskimo

> Nick will be speaking about best practices for building an
MVP and even micro projects rapidly in 30-60 days, and sometimes
even just a weekend.  Nick will first discuss the problem: Node.js
frameworks, and what to watch out for that slows you down.  We will
then explore share existing solutions and what is missing from them.
Finally, we will show off Eskimo and Igloo, and also tips and tricks
used to ship quickly with high quality.  We will dive into examples
that used and proved this stack, tips, and tools by showcasing a variety
of Clevertech MVP's in the FinTech, E-commerce and mobile arenas, which
were each very unique, but all used Igloo. This is all about hacking
something for a pre-MVP version, to get it above and beyond MVP ready.

## Outline

* Background: What do I do and have done?  What is Clevertech?  What do we do at CT?
* Focus: What are the Node.js frameworks/boilerplates available today for MVP's?
* Problems: What causes an MVP to take forever? What are all the things that can go wrong with an MVP?
  - Not having fun (no whimsys, nothing admirably tech or biz wise)
  - Lack of experience (simply not having enough practice)
  - Not knowing what package to use (e.g. outdated projects, broken builds, )
  - Bugs (and not knowing how to find or solve them -- rubber duck debugging)
  - Scope creep (e.g. letting a client keep adding features, not building essential features first, losing focus on stupid features like how I cloned Amazon's multi-order shipping address for Teelaunch before Teelaunch was even launched; wasted 3 weeks of time; but it was cool feature I can say I had built...)
  - Not using best practice (e.g. bad NPM versions in package.json)
  - Not using DRY practices (e.g. not modularizing components)
  - Database queries (e.g. writing raw SQL, not using an ORM like knex/bookshelf or mongoose)
  - Front-end HTML markup and CSS stylesheets taking too long (e.g. not using LESS and repeating yourself, not using mixins)
  - Not knowing where to start with a project (e.g. should I get the front-end or back-end done first? mockups? wireframes? how detailed should it be?)
  - Production (e.g. not having your code set to run differently in production, not having an automated process; constantly having to SSH in and git pull then restart the service)
  - Performance and optimization (e.g. assets are uncompressed, unminified, images aren't optimized, sprites aren't used)
  - Deployment (e.g. what are the various ways I can deploy my code?  git hook? github hook? travis-ci? jenkins? travis-ci webhook? what if I'm behind a VPN?)
  - Code Quality (e.g. how can I help ensure my team commits solid working code, using the right libraries, all writing similarly)
  - Code Standards (e.g. how can I help ensure my team maintains a set JSHint config, a set editor config, etc)
  - Code P2P Reviews (e.g. what is too much or too little? how do you handle bad code? how do you handle good code?  what slows down or speeds up?)
  - Debugging (e.g. not knowing what tools to use for debugging, not knowing how to use node-debugger, not knowing where to put console.log statements, not increasing log limit to Infinity in development, not having stage environment to test prod data with)
  - Alerts (e.g. not getting alerts when you should, like when a server goes down or when a user experiences a weird problem, or when transactions fail, or emails fail, etc)
  - Uptime (e.g. how can I maintain zero-downtime on deployments?  what happens when a user experiences an error and the entire server crashes for all other users?)
  - Setup and Services (e.g. not knowing how to set up your Mongo, Redis, PostgreSQL, MySQL boxes, not knowing how to set up hosting, not knowing how to manage DNS records)
  - Not having a secure server (e.g. not enforcing SSH only access, not locking it down, not enforcing fail2ban, iptables, etc)
  - Not practicing secure code standards (e.g. putting keys and passwords in a repository, not using a VPN when connecting over a coffee shop network -- not using IPSec)
  - Not running tests (e.g. mocha, chai, gulp)
  - Not having a build process (e.g. gulp or grunt)
  - Not running load tests (e.g. arete, wrk, ab)
  - Not shipping quick enough (e.g. not being consistent, odd hours, not sleeping enough, not thinking clearly, wasting time with business bs, either focus on product or focus on sales - you can't do everything, you need a team)
  - Not using a good editor/IDE (e.g. using Textmate or an old version of Sublime, learning vim -- helps with muscle memory and speed)
  - Not using plugins in your editor (e.g. not using JSHint built into your editor)
  - Not having good music to listen to while coding (e.g. Spotify, Pandora, RDIO, SKY.FM, DI.FM, Clementine)
  - Not knowing how to design a simple RESTful API for an MVP
  - Not knowing how to design a simple websocket API for an MVP
  - Not knowing how to document an API
  - Not knowing how to get customers and sales (e.g. growth hack)
  - Getting burned out (e.g. not having hobbies, taking breaks, focusing on work mode vs. play mode; subpar/mediocre vs top notch)
  - Client expectations (what is too much, too little?)
  - Not knowing how to do asset building (e.g. not knowing about concatenation, minification, uglification, etc -- resulting in slow perf -- not knowing of CDN)
* Solutions: Existing solutions to these common problems?
* Boilerplates/Frameworks: What's missing or should be missing from them for MVP's?  (show a scale and chart comparing the various frameworks)
  - Sails
  - Locomotive
  - Talk about how they go against Node/npm ways of modularizing and staying as lean as possible
  - Minimalism
  - Speed/performance
  - MVC/dependency injection
  - Production vs development
  - Not fast enough for MVP-style rapid dev aka "beast mode" (ref xmen)
* Intro: Introducing Eskimo and Igloo
  - Background behind it
    - Expressling
    - Lots of facepalms
    - Lots of failed projects that were all built similarly
    - How I artificially inflated # of stars? (humor)
    - Knowing that the only way to build faster is to share knowledge
  - What is it?
  - What deps does it have?
  - What's the Eskimo CLI about?
  - What deps does Igloo export by default?
  - Past timeline of versions of both Igloo/Eskimo
  - What was released today?
  - When should I use it?
  - How should I use it?
  - How do I stay up to date?
  - What if I have a problem?
  - How can I help contribute?
  - Future roadmap?
* Comparison: How does it compare to the other frameworks mentioned? (show the scale again but a new column with Igloo)
* Stats: Anonymous data collected on Eskimo/Igloo so far?
* Example Usage: How has Igloo/Eskimo been used?
  - Teelaunch (backend for shipping stuff; exited co)
  - GetProve (api and website)
  - Wakeup.io (website)
  - Song.st (api/music with Spotify/Last.fm - released today?)
  - Market Prophit (api/dev portal/documentation)
  - Seedfeed (api/website/ios app)
  - OurHarvest (e-commerce website)
  - Internal tools at Clevertech (hire, time)
* Common Examples: Does Eskimo have XYZ built-in?  (no, it has nothing, but it has examples that you can copy/paste and learn from)
  - Instead of just giving everything (e.g. login/auth/sessions/db/admin panel/abc feature/xyz feature) we simply give the core and nothing more
  - We document examples in the /examples folder on GitHub for you to learn from and adapt, and even add your own examples to
  - Forced to learn what the different modules do and what their individual API's are like (you absorb the methods and it becomes natural)
  - If a component is deemed core, then it will get added to igloo's boot folder for consumption as a dependency
* Q&A session
  - Jared Hanson with regard to cyclic dependencies and Electrolyte:
    > No, cyclic dependencies are not currently supported &ndash; as a rule, when those occurs, it suggests that one of them should be decomposed further, so the relations can be in only one direction."
