ConstraintLayout performance comparison
===============================

This app is an example test set that compares how the different ViewGroups
(ConstraintLayout vs traditional layouts) affects the UI performance.

Introduction
------------

This app runs the measure/layout passes with the layout using
ConstraintLayout and using traditional layouts (RelativeLayout and LinearLayout),
both of them result in the same appearance but how the UI components are built is 
different.

![LayoutCodelab-UI](/art/layout-codelab.png)

While running the measure/layout passes, the performance of UI is measured 
by using [Systrace](https://developer.android.com/studio/profile/systrace-commandline.html) and 
[OnFrameMetricsAvailableListener](https://developer.android.com/reference/android/view/Window.OnFrameMetricsAvailableListener.html)

Pre-requisites
--------------

You need to know:
- Review the XML file to know how each layout is built
  - [Layout using ConstraintLayout](/app/src/main/res/layout/activity_constraintlayout.xml)
  - [Layout using traditional layouts](/app/src/main/res/layout/activity_traditional.xml)

How to run the tests
---------------

1. Download the code.
2. Open the terminal at the downloaded directory.
3. Run the following shell script `./run.sh <device_id>`
  - The script is going to generate two html files as a result of running Systrace.
    Each represents the performance result for the layout with ConstraintLayout and with
    traditional.

(Optional)
- The app also logs the measurement result using OnFrameMetricsAvailableListener, but it isn't
  exported to any external files. You can check those stats as well.

License
-------

Copyright 2017 Google, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
