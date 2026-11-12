## Project Overview

This project is a personal audio-processing pipeline inspired by a simple yet bittersweet motivation: not being able to make it to Metallica's concert at the Las Vegas Sphere in person.

Curious about how to recreate some of that immersive concert experience at home, I started experimenting with spatial audio processing using my home theater system (soundbar, subwoofer, and two rear surround speakers).

The goal is to explore how audio processing and spatial positioning can bring a sense of the Sphere's immersive sound experience into a home theater environment.

The project currently features two versions, each exploring a different approach with its own strengths and limitations.

### Version 1: Spatial Routing & Visualization
1. **Acoustic Perspective & Spatial Feel:**
   - *Limitation:* The original stereo mix influences the perceived listening perspective, making it feel as though the listener is positioned close to the drum kit. While this creates an exciting and punchy experience, it does not fully reflect the spatial perspective of a large spherical venue.
   - *Current Effect:* You could hear the guitars and vocals echoing and reflecting off distant surfaces across a vast dome.
2. **Missing Height Channels:** Currently tailored for standard surround layouts without dedicated overhead (Atmos) height channels. *(Tested using Metallica's "One" and Tool's "Jambi".)*
3. **`spk_viz` Integration:** For those without a full 7.1 home theater setup at hand, you can use the companion [`spk_viz`](https://github.com/sharonHS127/spk_viz) project. You can import the original stereo track or the 7.1 output processed by `sphere_sim` to render a top-down animated preview of how the audio channels distribute across your speakers.

### Version 2: Source Separation Approach
1. **Demucs Integration:** Integrated Meta's **Demucs** source separation model to isolate individual instruments and vocals, allowing each stem to be processed and spatially positioned independently.
2. **Current Challenge:** Although the separation works, the low-end frequency response on the Bass track ends up sounding somewhat muddy and diffused.

---

Please feel free to try it out, play around with it, and let me know your thoughts! Fingers crossed I'll be able to make it to the concert next year. Thank you! :)
