Overview
========

<table>
  <tr>
    <td align="center">
        CI status
    </td>
    <td align="center">
        <a href="https://github.com/asherikov/sharf/actions/workflows/main.yaml">
        <img src="https://github.com/asherikov/sharf/actions/workflows/main.yaml/badge.svg" alt="Build Status">
        </a>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td align="center">
        Ubuntu package
    </td>
    <td align="center">
        22.04 (jammy)
    </td>
    <td align="center">
        24.04 (noble)
    </td>
  </tr>
  <tr>
    <td align="center">
        amd64
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fjammy;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fjammy;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fnoble;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fnoble;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
  </tr>
  <tr>
    <td align="center">
        arm64
    </td>
    <td align="center">
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--cross-arm64--all/latest/a=arm64;xc=main;d=ubuntu%252Fnoble;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--cross-arm64--all/latest/a=arm64;d=ubuntu%252Fnoble;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
  </tr>
</table>

A collection of utility packages for ROS/robotics projects. Refer to
<http://www.sherikov.net/sharf/> for more information.

Package Overview
================

This repository contains several utility packages designed for robotics and ROS
applications:

### `ariles`
A proxy ROS1/ROS2 package for Ariles serialization/configuration library, which
supports multiple data formats including YAML, JSON, ROS parameters, ROS2
parameters, Octave script output, and name-value pairs. It provides a flexible
way to handle configuration and serialization in robotics applications.

### `cdinit`
A ROS-compatible CMake wrapper for the dinit service manager, designed to
replace or complement traditional launching mechanisms like `roslaunch`,
`ros2launch`, `tmux`, and `screen`. It offers service management with startup
ordering, runtime dependencies, and advanced failure handling, suitable for
robotics applications requiring robust launch management.

### `intrometry`
A telemetry collection utility that addresses the same problem as
`pal_statistics` and `data_tamer` but in a different way. It uses the `ariles`
serialization library and keeps track of updated data instead of taking global
snapshots. Features multiple backends including ROS2 topic publishing and MCAP
file writing.

### `thread_supervisor`
A simple C++17 thread supervisor that automatically restarts failed or finished
threads.

### `graphite_to_mcap`
A system statistics collection utility that accepts data in Graphite format and
logs it to MCAP files. It's designed to work with tools like `collectd` for
system monitoring, with output compatible with `PlotJuggler` for data analysis
and visualization.

### `pjmsg_mcap_wrapper`
A logging library that writes `plotjuggler_msgs` to MCAP files without ROS
dependencies. It incorporates `FastCDR` serializer, `MCAP` library, and
pregenerated `plotjuggler_msgs` data structures, providing a complete solution
for data logging without exposing its dependencies.

Packages
========

Dependency graph
----------------

[![](pkg_dependency_graph.svg)](pkg_dependency_graph.svg)

Doxygen documentation
---------------------

| **Package** | Dependencies | Dependents |
| ----------- | :----------: | :--------: |
| [ariles2_core_ws](./ariles2_core_ws/index.html) | [graph](./ariles2_core_ws/pkg_dependency_graph.svg) | [graph](./ariles2_core_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_graphviz_ws](./ariles2_graphviz_ws/index.html) | [graph](./ariles2_graphviz_ws/pkg_dependency_graph.svg) | [graph](./ariles2_graphviz_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_namevalue2_ws](./ariles2_namevalue2_ws/index.html) | [graph](./ariles2_namevalue2_ws/pkg_dependency_graph.svg) | [graph](./ariles2_namevalue2_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_octave_ws](./ariles2_octave_ws/index.html) | [graph](./ariles2_octave_ws/pkg_dependency_graph.svg) | [graph](./ariles2_octave_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_pugixml_ws](./ariles2_pugixml_ws/index.html) | [graph](./ariles2_pugixml_ws/pkg_dependency_graph.svg) | [graph](./ariles2_pugixml_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_rapidjson_ws](./ariles2_rapidjson_ws/index.html) | [graph](./ariles2_rapidjson_ws/pkg_dependency_graph.svg) | [graph](./ariles2_rapidjson_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_ros2param_ws](./ariles2_ros2param_ws/index.html) | [graph](./ariles2_ros2param_ws/pkg_dependency_graph.svg) | [graph](./ariles2_ros2param_ws/pkg_reverse_dependency_graph.svg) |
| [ariles2_yamlcpp_ws](./ariles2_yamlcpp_ws/index.html) | [graph](./ariles2_yamlcpp_ws/pkg_dependency_graph.svg) | [graph](./ariles2_yamlcpp_ws/pkg_reverse_dependency_graph.svg) |
| [cdinit](./cdinit/index.html) | [graph](./cdinit/pkg_dependency_graph.svg) | [graph](./cdinit/pkg_reverse_dependency_graph.svg) |
| [cdinit_ros2](./cdinit_ros2/index.html) | [graph](./cdinit_ros2/pkg_dependency_graph.svg) | [graph](./cdinit_ros2/pkg_reverse_dependency_graph.svg) |
| [graphite_to_mcap](./graphite_to_mcap/index.html) | [graph](./graphite_to_mcap/pkg_dependency_graph.svg) | [graph](./graphite_to_mcap/pkg_reverse_dependency_graph.svg) |
| [intrometry_frontend](./intrometry_frontend/index.html) | [graph](./intrometry_frontend/pkg_dependency_graph.svg) | [graph](./intrometry_frontend/pkg_reverse_dependency_graph.svg) |
| [intrometry_pjmsg_mcap](./intrometry_pjmsg_mcap/index.html) | [graph](./intrometry_pjmsg_mcap/pkg_dependency_graph.svg) | [graph](./intrometry_pjmsg_mcap/pkg_reverse_dependency_graph.svg) |
| [intrometry_pjmsg_topic](./intrometry_pjmsg_topic/index.html) | [graph](./intrometry_pjmsg_topic/pkg_dependency_graph.svg) | [graph](./intrometry_pjmsg_topic/pkg_reverse_dependency_graph.svg) |
| [intrometry_tests](./intrometry_tests/index.html) | [graph](./intrometry_tests/pkg_dependency_graph.svg) | [graph](./intrometry_tests/pkg_reverse_dependency_graph.svg) |
| [pjmsg_mcap_wrapper](./pjmsg_mcap_wrapper/index.html) | [graph](./pjmsg_mcap_wrapper/pkg_dependency_graph.svg) | [graph](./pjmsg_mcap_wrapper/pkg_reverse_dependency_graph.svg) |
| [thread_supervisor](./thread_supervisor/index.html) | [graph](./thread_supervisor/pkg_dependency_graph.svg) | [graph](./thread_supervisor/pkg_reverse_dependency_graph.svg) |

Total number of packages: 
17

Workspace status
-----
:::{.wide}
```
tags/0.2.3-0-g3ad3af3
WSH: >>> status: git sources ---
Flags: H - version hash mismatch, M - uncommited changes
name               version  actual version           HM repository
----               -------  --------------           -- ----------
ariles             pkg_ws_2 tags/ws-2.5.2-0-ge2c1a11    https://github.com/asherikov/ariles.git
cdinit             master   heads/master-0-g9504974     https://github.com/asherikov/cdinit.git
graphite_to_mcap   main     heads/main-0-gf0ad58c       https://github.com/asherikov/graphite_to_mcap.git
intrometry         main     heads/main-0-gb53b80d       https://github.com/asherikov/intrometry.git
pjmsg_mcap_wrapper main     heads/main-0-gc89d9cd       https://github.com/asherikov/pjmsg_mcap_wrapper.git
thread_supervisor  master   tags/1.2.3-0-g2d740f6       https://github.com/asherikov/thread_supervisor.git

WSH:  <<< status: git sources ---
```
:::


Useful links
============

- [ROS online status](https://status.openrobotics.org/)
- [ROSDEP packages](https://github.com/ros/rosdistro/blob/master/rosdep/base.yaml)

ROS1
----
- [C++ API](http://docs.ros.org/en/noetic/api/roscpp/html/)
- [catkin API](https://docs.ros.org/en/noetic/api/catkin/html/dev_guide/generated_cmake_api.html)

ROS2
----
- [C++ API](https://docs.ros2.org/latest/api/rclcpp/namespacerclcpp.html)
- [ament](https://docs.ros.org/en/foxy/How-To-Guides/Ament-CMake-Documentation.html)
