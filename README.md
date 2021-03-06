# Rapid PbD
[![Build Status](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__rapid_pbd__ubuntu_trusty_amd64__binary)](http://build.ros.org/job/Ibin_uT64__rapid_pbd__ubuntu_trusty_amd64__binary/)

Rapid PbD is a programming by demonstration (PbD) system for the PR2, Fetch, and Baxter robots.
The goal of the system is to provide an easy way to program manipulation actions that can be used in other applications.

## Getting started
- See the [wiki](https://github.com/jstnhuang/rapid_pbd/wiki)

## Program model
Users use the Rapid PbD interface to create *programs*.
A program is represented using the `rapid_pbd_msgs/Program` msg.
The system provides an actionlib interface for running programs.

A program consists of a sequence of *steps*, and each step consists of one or more *actions*.
There can be different types of actions, including moving the arm, moving the head, and detecting tabletop objects.
The actions of a step are run in parallel, but the steps run in sequence.
For example, in one step, you can point the head down and move the robot's arms to the side, and in the next step, you can detect tabletop objects.
