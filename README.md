# Word Play

CEEM audio-triggered word machine for Windows x64 VST3 hosts. It measures each guitar note and speaks a random American English word after the note ends.

The built-in bank has 72 words, spoken by the American English Windows Zira voice. Notes under 250 ms choose the short-word group, 250–700 ms choose medium words, and notes over 700 ms choose longer words. Each group contains 24 words, with no immediate repeat within a group.

Insert Word Play on a guitar track before distortion, select your audio input and enable monitoring. Play clearly separated notes. Threshold controls detection, Input adjusts sensitivity, Speech sets the word volume, and Guitar blends the original guitar back in. It waits for 40 ms of quiet to determine that a note has ended. Clicks shorter than 40 ms are ignored. Stereo input uses the left channel for detection. Mono input is supported.

Words play at their natural speaking pitch. A new triggered word fades out the previous word. Settings store with the project.

Extract the complete Word Play.vst3 bundle into your VST3 folder and rescan in REAPER.

Build using Visual Studio C++ tools and CMake.

    cmake -S . -B build -A x64
    cmake --build build --config Release --target WordPlay_VST3
