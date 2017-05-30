# ATEM Macros - Getting started

Note: Change `mixEffectBlockIndex="0"` to reflect your ME.

# Basic Control
### Cut
`<Op id="CutTransition" mixEffectBlockIndex="0"/>`
### Auto
`<Op id="AutoTransition" mixEffectBlockIndex="0"/>`
### Program
`<Op id="ProgramInput" mixEffectBlockIndex="0" input="Camera5"/>`
### Preview
`<Op id="PreviewInput" mixEffectBlockIndex="0" input="Camera7"/>`

# Down and Upstream keys
Note: Change `keyIndex="0"` to reflect the keyer that you wish to turn on/off.
### Downstream Key ON
`<Op id="DownstreamKeyOnAir" keyIndex="0" onAir="True"/>`
### Downstream Key OFF
`<Op id="DownstreamKeyOnAir" keyIndex="0" onAir="False"/>`
### Upstream Key ON
`<Op id="KeyOnAir" mixEffectBlockIndex="0" keyIndex="0" onAir="True"/>`
### Upstream Key OFF
`<Op id="KeyOnAir" mixEffectBlockIndex="0" keyIndex="0" onAir="False"/>`

# Macro settings
### Macro Sleep
`<Op id="MacroSleep" frames="26"/>`<br />
Note: Change `frames="26"` to set your wait duration.
### Macro User Wait
`<Op id="MacroUserWait"/>`

# Advanced
### Custom auto transition
`<Op id="TransitionPosition" mixEffectBlockIndex="0" position="0.0"/>`<br />
`<Op id="MacroSleep" frames="2"/>`<br />
`<Op id="TransitionPosition" mixEffectBlockIndex="0" position="0.25"/>`<br />
`<Op id="MacroSleep" frames="2"/>`<br />
`<Op id="TransitionPosition" mixEffectBlockIndex="0" position="0.5"/>`<br />
`<Op id="MacroSleep" frames="2"/>`<br />
`<Op id="TransitionPosition" mixEffectBlockIndex="0" position="0.75"/>`<br />
`<Op id="MacroSleep" frames="2"/>`<br />
`<Op id="TransitionPosition" mixEffectBlockIndex="0" position="1"/>`<br />
Note: The `position="1"` variable will allow you to enter any number between 1.0 and 0.0. The more steps, the smoother the transition.

### Custom audio fade
`<Op id="AudioMixerMasterOutGain" gain="32768"/>`<br />
`<Op id="MacroSleep" frames="2"/>`<br />
repeat <br />
Note: `gain="32768"` is '0db' and `gain="0"` is '-inf' on the master audio control. The MacroSleep frames will allow you to set a smooth fade.
