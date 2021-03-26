---
layout: page
title: 'Implementation'
---

### Are Containers the right solution for you? 

At a high level, let's just do a pulse check and see if containers are the answer to all your problems. Have you looked at [Link to section about Keep, Retire, Repurchase]? If you have decided you want to keep your app, let's keep going and see how this could help you. 

After you've decided to keep you app, you need to decide how much modernization you want to do. Want is not the same as can. You might want to modernize your app, and it's too old. Hardware is gone, coders don't know it. Within the next decade many of your on premise solutions of the past will become obosolete, and we will not be able to find coders with the skill set to fix your hardwared. 

Another key consieration is: how much work do I want to invest? Containers are a great solution if you don't have the ability or resources to totally overhaul your app. With a container solution you'll have the ability to modernize your app enough to move it to the cloud and have access to cloud capabilities. It will not be cloud native, but it's a step in the right direction. Containers are also a great way to start your modernization, and they you can come back to the containerized app at a future date to see if you want to enhance its cloud capabilties. 

Before you jump to starting a containerization process, please check if there is a SAAS out there that can do the same services as your app. If you have very limited users for your app it might cost less to retire the app and replace it with a SAAS productt. 

Choosing to containerize your app as a moderization pattern is a holistic process. We have to look at what we want to do, what we need, our effort level and what is available. We want to make sure containers is the right solution. 

\### Project status


[ ] Do you want to keep your application
[ ] Do you want this done fast?
[ ] Is your investment availablity Low cost/Low effort?
[ ] Is your app out of date?
[ ] Have you looked for any SAAS application out there that could do what your app does? 
[ ] Do you have hardware sourcing limitations?

Some times older applications have outdated technologies, licencing agreement that limit it's re-architecture and still you need to move it to the cloud to take advantage of some of the cloud capabilies, like scaling. 

Have you looked at what is available for modernization. Is there anything else out there that can do what your app can do? An already built SAAS?
- - -
 <head>
    <!-- Load jQuery -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
    <!-- Load Chart.js -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.8.0/Chart.bundle.min.js"></script>
    <!-- Load PapaParse to read csv files -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.1.0/papaparse.min.js"></script>
  </head>

  <body>
    <canvas id="container" style="width:100%; height:400px;"></canvas>

<link rel=href>
    <p style="font-family: Helvetica; color: #333; padding: 1em 2em; font-size: 12px">
      Source: www.idc.com Gary Chen June 2019 | Sponsored by: Amazon Web Services 
      <br>
      <a href="https://github.com/HandsOnDataViz/chartjs-bar">View data and code</a>,
      created by <a href="https://handsondataviz.org/">HandsOnDataViz</a>
      with <a href="https://www.chartjs.org/">Chart.js</a>
    </p>
    <script src="/js/script.js"></script>
  </body>
  
- - -

### Application migration

Containers make it easy to package your entire application and move it to the cloud without needing to make any code changes. If you want to keep your app, there isn't a prebuilt solution and you don't have the resources, or reasons to rebuild it. This would be a good solution.  

- - - 

|  What they can do for you                    | What they won't do         |
| --------------------------                   | -------------------------- |
|  can move your app to the cloud              | does not pay your technical debt  |
|  give you portability                        | does not fix an underlying poor infrastructure|
|  allow your app to use cloud elasticity (scalability) | doesn't make app cloud native |
|  allows your developers to innovate          | if your app is broken it will still be broken |
|  achieve greater efficiency                  | liscence dependencies - might prevent use |
|  allow you to attract innovative developers  | hardward dependencies - might prevent use |
|  aligns w/workforce trends.                  | technology dependencies - some tech is too old |
|  more efficiencieny development technologies | tech managed by gui (excel, ms axis) |
|  reduce tools your dev teams need            |                            |
|  can still sit on prem                       |                            |

<br>