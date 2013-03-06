---
layout: project
title: Hypertest
group: projects
tabify : h2
project :
  name : Hypertest
  tagline : "Inspired by QALiber and Selenium, and wanting to learn WPF/C# I started out this visual scripting project to automate some web testing using drag and drop opertaions. The project is still in the initial stages and is in the process of migration to Wide."
  source : https://github.com/chandramouleswaran/Hypertest
  website : https://github.com/chandramouleswaran/Hypertest
  tagGroups :
    -
      name : platforms
      tags : 
        -
          {name : WPF, why : "Hypertest runs as a Windows application. WPF is the best technology to create Windows application."}
        -
          {name : .NET, why : "The best technology for Windows. Java was another option!"}
    -
      name : languages
      tags :
        -
          {name : C#, why : "Easier to use and popular among .NET developers. Also, Selenium Webdrive was written using C# (I know not a valid reason :P)" }
    -
      name : frameworks
      tags :
        -
          {name : Wide, why : "Quickest way to create a IDE. Still under development."}
        - 
          {name : Selenium, why : "Best web testing framework supporting different browsers."}
---

## Overview

### Hypertest

Hypertest is an application used to automate web testing using Selenium using visual scripting operations such as drag and drop to create tests to make life easier for non-programming folks. Currently, the project is being migrated to Wide.

### Screenshots
<img src="http://i47.tinypic.com/2ii7mad.png" width="700px" />


## Features

### Stuff that works

- Variables, visual scripting
- Performing simple actions on elements (Click/Send keys)
- Complex searching within elements
- Simple expression evaluation
- Storing element's properties as variables
- Taking screen shots at the end of a test step
- Easy to create new test cases by extending the abstract classes
- Different browsers (Chrome, Firefox, IE)

### Plans for future

- Complex inputs (Dragging/dropping, Ctrl + Click etc)
- Partial screenshots
- Image comparison
- OCR over an area and analyze text
- Better organization of tests in the tests pane
- Plans to have different types of scenario - currently there is only web scenario. This can be extended to test an app (WPF UIA Based)
- Create/reuse existing property grid in test case whenever possible
- Create a runner service? This way runner can be installed in a remote system and the scenario can be serialized and sent to the system for execution
- Any new ideas/suggestion??

## Documentation

Here is a quick walk through of how to use the Hypertest app.

<img src="http://i49.tinypic.com/axbo0o.png" width="700px" />

- Create a new scenario with some suitable settings. You can also define some variables that is specific for a scenario.

<img src="http://i50.tinypic.com/2isghlk.png" width="700px" />

- Drag an drop tests from the tests pane available on the right hand side of the window. If its not there, use "Ctrl + T" to bring it up.

<img src="http://i49.tinypic.com/x3d921.png" width="300px" />

- The most common test case is the web test case. Using this test cases you can
    
    a. Search for an element based on the following

    ![Search](http://i45.tinypic.com/n54f87.png)

    b. You can also search within an element if you have stored the element to a variable and use it in the next test case as a parent element.

    ![Parent](http://i50.tinypic.com/166gjv6.png)

    c. Take screen shots at the end of a test case

    <img src="http://i47.tinypic.com/2ii7mad.png" width="700px" />

- The results are available in the form of an XML. The plan is to also be able to open the result in the app whenever needed.

For a developer - You can create your own version of the test case. All you need to do is to inherit the TestCase class for generic tests or WebTestCase for a web test case. In your project's post build events, copy the DLL and move it to Hypertest's target dir/Test/Your.DLL.

Please contact me if you need any more details.