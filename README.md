# smart-cooker-whistle-counter
# Smart Cooker Whistle Counter

A smart kitchen solution designed to detect and count pressure cooker whistles automatically, helping users avoid overcooking, gas wastage, and cooking mistakes.

## Overview

In many households, especially in Indian kitchens, cooking depends heavily on counting the number of pressure cooker whistles. People often forget the count, get distracted, or leave the kitchen, which may lead to burnt food, wasted gas, and in some cases safety concerns.

Smart Cooker Whistle Counter solves this problem by using a sound sensor and microcontroller to detect each whistle, count them, and alert the user when the desired number is reached.

This project is low-cost, practical, and works with existing pressure cookers without requiring users to buy a new appliance.

## Problem Statement

Counting cooker whistles manually is a common everyday challenge. It is easy to lose track of time and whistle count, especially while multitasking. This often results in:
- Overcooked or burnt food
- Gas wastage
- Unsafe cooking conditions
- Difficulty for elderly users and busy families

## Solution

The system listens for the pressure cooker whistle sound, counts the number of whistles, and triggers alerts when the target count is reached.

Features include:
- Whistle detection using sound sensor
- Whistle count tracking using ESP32
- Buzzer alert
- Mobile notification support (optional)
- OLED display for live count
- Automatic gas shutoff feature (optional)
- Works with any standard pressure cooker

## Features

- Automatic whistle detection
- Count-based alert system
- Buzzer and mobile notifications
- Optional gas-off mechanism using servo motor
- Works with regular existing pressure cookers
- Affordable and easy to build
- Suitable for daily home use
- Future scope for recipe-based presets

## Hardware Components

- ESP32 Microcontroller
- Sound Sensor Module
- Buzzer
- OLED Display (optional)
- Servo Motor (optional for gas shutoff)
- Battery / Power Supply
- Heat-resistant casing
- Connecting wires and breadboard / PCB

## System Workflow

1. The user sets the desired number of whistles.
2. The sound sensor listens for the whistle sound.
3. The ESP32 detects and counts each whistle.
4. When the target count is reached, the system triggers:
   - buzzer alarm
   - display notification
   - optional phone alert
   - optional gas shutoff

## Project Architecture

```text
Pressure Cooker Sound
        |
        v
Sound Sensor
        |
        v
ESP32 Controller
        |
   +----+----------------------+
   |                            |
   v                            v
Whistle Count Logic          Alerts / Output
   - Display                   - Buzzer
   - Notification              - Servo Motor
   - Data Logging              - Mobile Alert
