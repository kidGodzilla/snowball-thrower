# Pokemon Scarlet / Violet Infinite Money Ace Tournament Grinder

A fork of a fork of a fork of a fork, modified to grind the Ace Tournament in a specific location in Pokemon Scarlet / Violet. Assumes you have a strong Pokemon in position 1 that can one-shot everyone and survive for hours (Google Inifite money builds).

See previous projects for some more detailed information / setup process.

---

LUFA has been included as a git submodule, so cloning the repo like this:

```
git clone --recursive git@github.com:bertrandom/snowball-thrower.git
```

will put LUFA in the right directory.

Now you should be ready to rock. Open a terminal window in the `snowball-thrower` directory, type `make`, and hit enter to compile. If all goes well, the printout in the terminal will let you know it finished the build! Follow the directions on flashing `Joystick.hex` onto your Teensy, which can be found page where you downloaded the Teensy Loader application.

### Building

1. Install avr-gcc 
2. Install LUFA dependency
3. Run `make`
4. Run `./teensy_loader_cli --mcu=atmega32u4 -wv Joystick.hex`

#### Thanks

Thanks to https://github.com/bertrandom/snowball-thrower for the updated information which modifies the original script to throw snowballs in Zelda. This C Source is much easier to start from, and has a nice object interface for creating new command sequences.

Thanks to Shiny Quagsire for his [Splatoon post printer](https://github.com/shinyquagsire23/Switch-Fightstick) and progmem for his [original discovery](https://github.com/progmem/Switch-Fightstick).

Thanks to [exsilium](https://github.com/bertrandom/snowball-thrower/pull/1) for improving the command structure, optimizing the waiting times, and handling the failure scenarios. It can now run indefinitely!
