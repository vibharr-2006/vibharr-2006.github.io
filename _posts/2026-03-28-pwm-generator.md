---
layout: post
title: Generating PWM 
date: 2026-03-05 
description: Purpose of this series
tags: formatting links
categories: sample-posts
---

## Introduction

<p>As you know, the aim was to build a class-d Amplifier. But I have broken this project into modules: </p>

<ul>
<li>Generating PWM signal from input</li>
<li>Passing through a gate driver (built from scratch)</li>
<li>Power switching stage (using MOSFETs)</li>
<li>LC low pass filter to reconstruct the audio signal</li>
</ul>

<p>So lets test the first module</p>

## Triangular Wave Generator

<p>The audio signal is compared with a triangular wave using a comparator (LM393) which as a result produces a PWM wave. So first lets rig up a circuit that can generate a triangular wave.
The components used:
</p>

<ol>
<li>LM741 (op-amp) (x2)</li>
<li>10K ohm (x5)</li>
<li>100K ohm (x1)</li>
<li>1 uF capacitor</li>
<li>33 nF capacitor</li>
</ol>

<p>To generate triangular wave, we need to input a square wave through an integrator. A square wave is built using a schmitt trigger + RC circuit.</p>

