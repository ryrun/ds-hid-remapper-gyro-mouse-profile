# DualSense Gyro Mouse Profile

This repository contains a HID Remapper profile for turning a Sony DualSense
controller into a gyro mouse setup.

The goal is to make a DualSense feel closer to a mouse-and-keyboard style FPS
layout, with gyro aiming for mouse movement and stick-based directional input.
In spirit, it is trying to recreate the feel of the FPS WASD profile from
Alpakka by Input Labs, but on a DualSense. You can think of it as a kind of
"Dualpakka" approach, a community term also used in posts such as:
https://www.reddit.com/r/GyroGaming/comments/1jx147j/my_dualpakka/

At the moment, the exported JSON profile is based on the DualSense Edge. The
main logic can be adapted further, but the current custom usages and profile
layout were built around that device first.

## What It Does

- maps gyro movement to mouse movement
- activates gyro when the touchpad is touched
- uses expression-based logic for gyro shaping and stick classification
- includes stick-driven directional outputs inspired by Alpakka-style controls

## Current State

This is an experimental profile setup rather than a polished end-user release.
It is a working base for testing, tuning, and iterating on a DualSense gyro
mouse layout.

Some parts are already organized into reusable expression files:

- [expression_1_gyro.txt](./expressions/expression_1_gyro.txt)
- [expression_2_left_sticks_4dir_inner_outer.txt](./expressions/expression_2_left_sticks_4dir_inner_outer.txt)
- [expression_3_right_stick_8dir.txt](./expressions/expression_3_right_stick_8dir.txt)

The current exported profile file is:

- [ds-edge-hid-remapper-config.json](./profiles/ds-edge-hid-remapper-config.json)

## Inspiration

This work is inspired by the Alpakka firmware and control ideas from Input
Labs:

- Alpakka overview: https://inputlabs.io/alpakka
- Alpakka profiles: https://inputlabs.io/alpakka/manual/profiles
- Alpakka FAQ, including touch-activated gyro behavior: https://inputlabs.io/alpakka/manual/faq
- Community examples of the "Dualpakka" idea:
  https://www.reddit.com/r/GyroGaming/comments/1jx147j/my_dualpakka/
  https://www.reddit.com/r/GyroGaming/comments/1p67nhh/taking_the_dualpakka_one_step_further/

The intention is not to copy it one-to-one, but to bring a similar control
philosophy to the DualSense through HID Remapper.

## Notes

- the current JSON profile targets the DualSense Edge first
- some logic may also work on the regular DualSense with adjusted device IDs
- tuning values such as sensitivity, deadzones, and stick thresholds are still
  meant to be adjusted to personal preference

## Purpose

This repository is mainly meant as a practical profile project:

- to experiment with gyro-to-mouse remapping on DualSense
- to document the related HID Remapper expressions
- to move toward a comfortable FPS-style controller layout with touch-activated
  gyro aiming
