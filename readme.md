# [Patcher Page](https://scrxtchy.github.io/GearsetSorter14/)

Another barebones page that provides useful functionality

This page works by rolling over each gearset block to add them to a list, and then uses the list as a reference to determine which order they should be saved in.
I haven't looked too much into the data structure, but each gearset's data block starts with it's `0` to `100` value, giving 101 unique gear slots, followed by it's name, terminating with `0`. Inclusive of the order number, there's 448 bits for each gearset, but we don't move the number at all when processing the data

Gearsets are saved with an XOR value of `0x73`, we use this in the code to provide readable text for each gearset on the page