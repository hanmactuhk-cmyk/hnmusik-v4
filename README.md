
# HNStudio Musik AI v4

This version establishes the intended production architecture:
- Separate microphone and music paths.
- Stereo Mix/system loopback is independent from the internal SFX bus.
- Master, microphone and music volume are independent.
- HNStudio effects and external VST3 rack are separate layers.
- VST3 plugins are processed in the actual audio callback in rack order.
- VST bypass is real.
- Audio I/O and guide dialogs are included.

Important engineering note:
Windows system loopback capture, production-grade pitch correction/Auto-Key, and robust low-latency VST3 hosting require the native audio engine to be completed and tested against the target interfaces. The project uses JUCE's VST3 hosting APIs and is intended to be built on Windows with CMake.
