# G-code sequence plasma cut enhancer

The following application enhances an existing laser cutting g-code sequence, such that on each On signal, z-axis movements are incorporated, facilitating a plasma torch cutting scope.

More specifically the input sequence is enhanced by pre-pending and appending code and by wrapping the On and Off commands with additional. The pre-pending commands set the X,Y,Z axis at current position as the zero position. The appending commands, add a return to home command, allowing the reproducibility of experiments.

The Off signal is replaced by an Off signal and a z-axis movement raising the head for clear path movement. The on signal is replaced by lowering the head, followed by an On signal, followed by a slight raise of the head. The on / spark signal happens at the lowest point, aiding the spark to happen and consequent movements happen at a slight raised position state to prolong the life of consumables and to give time for the piercing to happen.

end app > plasma-cut-g-code-convert.html
