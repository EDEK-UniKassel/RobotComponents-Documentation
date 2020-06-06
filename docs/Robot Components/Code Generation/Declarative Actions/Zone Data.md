---
layout: default
title: Zone Data
nav_order: 3
parent: Declarative Actions
grand_parent: Code Generation Components
has_toc: false
---

# **{{page.title}}**

## **Description**

[**Declarative Action**]({{ site.baseurl }}{% link docs/Robot Components/Code Generation/Declarative Actions/index.md %})**:** Defines the zone data for a [Move]({{ site.baseurl }}{% link docs/Robot Components/Code Generation/Instructive Actions/Move.md %}) or [Absolute Joint Movement]({{ site.baseurl }}{% link docs/Robot Components/Code Generation/Instructive Actions/Absolute Joint Movement.md %}) component. The Zone data is used to specify how (precise) a position is to be terminated. 

## **Input Parameters**

**Name (N):** The zone data variable name. Each zone data name needs to be unique. The first letter shouldn’t be a number. Don’t use special characters.

**Fine Point (FP):** A boolean that defines whether the movement is to terminate as a stop point (fine point) or as a fly-by point. 

**Path Zone TCP (pzTCP):** The size (the radius) of the TCP zone in mm. 

**Path Zone Orientation (pzORI):** The zone size (the radius) for the tool reorientation. The size is defined as the distance of the TCP from the programmed point in mm.

**Path Zone External Axes (pzEA):** The zone size (the radius) for external axes. The size is defined as the distance of the TCP from the programmed point in mm.

**Zone Orientation (zORI):** The zone size for the tool reorientation in degrees. If the robot is holding the work object, this means an angle of rotation for the work object.

**Zone External Linear Axes (zELA):** The zone size for linear external axes in mm.

**Zone External Rotational Axes (zERA):** The zone size for rotating external axes in degrees.

## **Output Parameters**

**Zone Data (ZD):** Contains the Zone Data instructions as action for a robot movement instruction.

## **Usage**

[**Code Generation**]({{ site.baseurl }}{% link docs/Robot Components/Code Generation/index.md %})**:** Plug the Zone Data output of this component into the Zone Data input of the [Code Generation: Move]({{ site.baseurl }}{% link docs/Robot Components/Code Generation/Instructive Actions/Move.md %}) or [Code Generation: Absolute Joint Movement]({{ site.baseurl }}{% link docs/Robot Components/Code Generation/Instructive Actions/Absolute Joint Movement.md %}) component to set the precision of the movement instruction. This will also add a zonedata declaration to the RAPID Program module.