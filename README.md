MadLab Miners
=============

This repository is for planning and code related to the Minecraft/Minetest group at MadLab.

Next Meeting:  14th June 2015 -- The Manchester Day Parade
===========================

Outline Plan
------------

We have the Manchester Day Parade coming up on Sunday 14th June.  We have space in the Manchester Library on the day.  The CoderDojo on the 10th of May is the last one before the parade.  The plan for 10th May is to try out some of the things that we will do on the parade day.

### Probably Achievable Things
* Build a float to go into the parade
* Capture the float in some way that it can be added to the server which is displaying all the floats (e.g. https://github.com/Uberi/Minetest-WorldEdit )
* Implement a server that shows all the floats in the parade -- project up on to the wall

To-do List
----------

2. Implement the client world/code that will have a defined area in which to build your float, have a button to save your float out some how, finally reset the world so that the next person can build a float
3. Implement the server to display all the floats and some how animate them going past
4. Implement the code to add the saved floats into the parade
5. Implement some code to handle what happens when you get too many floats in the parade


Done List
----------
1. Add the WorldEdit mod to the CoderDojo game pack



Float Creation Client
---------------------

The float creation client is a stand-alone PC running Minetest with the parade game pack installed.  The PC is expected to be running Linux (probably Mint).  The cycle for the usage of the float creating client is as follows:

1. New user arrives as the PC and is presented with a well defined cuboid (30W x 15D x 30H) within which they have to create their float
2. The user builds their float in Minetest within the bounds of the defined area
3. When they are happy with their creation they press a button to say they want to add their float to the parade
4. The button triggers Minetest lua code to save out their float the a well-known folder using Worldedit
5. The building area cuboid is reset to empty ready for the next user
6. (The client does NOT have the responsibility for getting the float added to the server.  A separate monitor process will be watching the well-known folder and will add the new float to the parade world.)









Lua Tutorial
------------

Sources of Lua information:

* [Lua Tutorial on GitHub](https://github.com/Jeija/minetest-modding-tutorial)
* [Lua Tutorial on Minetest dev wiki](http://dev.minetest.net/Intro)
