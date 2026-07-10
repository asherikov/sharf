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
        amd64
    </td>
    <td align="center">
        arm64
    </td>
  </tr>
  <tr>
    <td align="center">
        22.04 (jammy)
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fjammy;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fjammy;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
    <td align="center">
    </td>
  </tr>
  <tr>
    <td align="center">
        24.04 (noble)
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fnoble;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fnoble;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--cross-arm64--all/latest/a=arm64;xc=main;d=ubuntu%252Fnoble;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--cross-arm64--all/latest/a=arm64;d=ubuntu%252Fnoble;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
  </tr>
  <tr>
    <td align="center">
        26.04 (resolute)
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fresolute;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--reldebug--all/latest/a=amd64;d=ubuntu%252Fresolute;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
        </a>
    </td>
    <td align="center">
        <a href="https://cloudsmith.io/~asherikov-aV7/repos/all/packages/detail/deb/sharf--cross-arm64--all/latest/a=arm64;xc=main;d=ubuntu%252Fresolute;t=binary/">
        <img src="https://api-prd.cloudsmith.io/v1/badges/version/asherikov-aV7/all/deb/sharf--cross-arm64--all/latest/a=arm64;d=ubuntu%252Fresolute;t=binary/?render=true&show_latest=true" alt="Latest version of 'sharf' @ Cloudsmith">
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

`ariles`
--------
A proxy ROS1/ROS2 package for Ariles serialization/configuration library, which
supports multiple data formats including YAML, JSON, ROS parameters, ROS2
parameters, Octave script output, and name-value pairs. It provides a flexible
way to handle configuration and serialization in robotics applications.

`cdinit`
--------
A ROS-compatible CMake wrapper for the dinit service manager, designed to
replace or complement traditional launching mechanisms like `roslaunch`,
`ros2launch`, `tmux`, and `screen`. It offers service management with startup
ordering, runtime dependencies, and advanced failure handling, suitable for
robotics applications requiring robust launch management.

`intrometry`
------------
A telemetry collection utility that addresses the same problem as
`pal_statistics` and `data_tamer` but in a different way. It uses the `ariles`
serialization library and keeps track of updated data instead of taking global
snapshots. Features multiple backends including ROS2 topic publishing and MCAP
file writing.

`thread_supervisor`
-------------------
A simple C++17 thread supervisor that automatically restarts failed or finished
threads.

`graphite_to_mcap`
------------------
A system statistics collection utility that accepts data in Graphite format and
logs it to MCAP files. It's designed to work with tools like `collectd` for
system monitoring, with output compatible with `PlotJuggler` for data analysis
and visualization.

`pjmsg_mcap_wrapper`
--------------------
A logging library that writes `plotjuggler_msgs` to MCAP files without ROS
dependencies. It incorporates `FastCDR` serializer, `MCAP` library, and
pregenerated `plotjuggler_msgs` data structures, providing a complete solution
for data logging without exposing its dependencies.
