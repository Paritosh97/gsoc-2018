

# GearVR and Daydream Support

## About Me

My name is Paritosh and I am currently pursuing a Bachelor of Technology in Computer Science in SRM Institute of Science and Technology. My major field of interest is Game Development and Virtual Reality.

## About the Project

My project for GSoC is adding Gear VR and Google VR support to [Godot Engine](https://github.com/godotengine/godot). The goals are,

 - Creating a GDNative module for Oculus mobile devices([Gear VR](https://www.oculus.com/gear-vr/) and [Oculus Go](https://www.oculus.com/go/))
 - Adding [Google VR](https://vr.google.com/)(Cardboard and Daydream) support in Godot Core

## The Challenges

 - So the biggest challenge I faced was the lack of a GLES 2 renderer in Godot. Thus, I wasn't able to test out any of the 3D scenes on my [Adreno](https://github.com/godotengine/godot/issues/12816) devices. This was later fixed by [karroffel](https://github.com/karroffel) by [adding](https://github.com/godotengine/godot/pull/20512) GLES 2 3D renderer. Fortunately, [Bastiaan](https://github.com/BastiaanOlij)(my GSoC Mentor) had a Note 4 running on a Mali GPU and we were able to test the Gear VR module on it. This resulted in a relatively slow workflow.
 - Apart from that, another major issue faced was the lack of Android support for the GDNative API. Sure, there were some [additions](https://github.com/godotengine/godot/pull/19591) made by me and Bastiaan when it came to the addition of some JNI calls in GDNative API. But still, not a lot of people have experimented with GDNative and Android. The Google VR GDNative Module never initialized while the Gear VR did. These uncertainties increased more and more as we went into depth.

 
## What is done
 
-   Understanding the existing GDNative APIs and modules
-   Understanding Oculus' VrApi
-   Adding GDNative Android API to core
-   Implementing Gear VR GDNative module
-   Compiling Gear VR GDNative module
-   Initialize VrApi on the Device
-   Understanding the Google VR Android SDK
-   Writing boilerplate for Google VR

## What remains

 - Succesful stereo rendering to the viewport for GearVR
 - VrApi Input API
 - Succesful stereo rendering and tracking for GoogleVR
 - Merge GoogleVR Code to Godot Core
 - VrApi Input API integration
 - Google VR Controller API integration
 
## The Code

 - [Gear VR GDNative Module](https://github.com/GodotVR/godot_gearvr)
 - [Google VR Android Module](https://github.com/Paritosh97/godot_googlevr)

## GSoC Experience

Working at Godot has been great. I will continue contributing to Godot after GSoC. The guys at IRC have been very helpful even before GSoC began. [Bastiaan](https://github.com/BastiaanOlij) with his exquisite knowledge in VR has been a great mentor and helped me a lot. I plan to pursue higher studies in the field and GSoC and Godot have helped me a lot to get me ready for it.

## Useful Links

 - [GSoC Proposal](https://storage.googleapis.com/summerofcode-prod.appspot.com/gsoc/core_project/doc/5468988994224128_1522087817_Technical_Proposal.pdf?Expires=1533768052&GoogleAccessId=summerofcode-prod@appspot.gserviceaccount.com&Signature=pdppYy8Nvq5GRZXz%2byB6AJFQ6r1Ui%2bsGZN//SzNny0o76T1QnAfIrcdp8yFmXw5gY2l21UtvH88vA%2bRwwDxTPtEJQIg0F2vqY6r%2bMkbFEv9g/d8XCNCAe6MHQZGhHnhlJZ3evS7ZwJ9eITJeq3xfD84xvMRVp1MEvS1SV5fOY5ZUnXjCS6/lRJXFTnNhWZK4uuLCYInrbfqJwxRGJddn6zO6D5w5txnZm%2bTj4hkNxrdc05ioy%2brG2993/AbotKM%2bnjng4TlOEAiLeSUEFd2Ukg0r833qpYfLOoCrbQ/uCfOaIICKdfl9wGBzEp55Vn5BW%2bgOoVDYmW8mugJeD0OqTg==)
 - [Progress Report #1](https://godotengine.org/article/gsoc-2018-progress-report-1#gearvr-daydream)
